---
title: Excel でのマルチ スレッド再計算
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798933"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="58e48-104">Excel でのマルチ スレッド再計算</span><span class="sxs-lookup"><span data-stu-id="58e48-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="58e48-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="58e48-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="58e48-p101">Microsoft Office Excel 2007 �́A���[�N�V�[�g�̃}���\`�X���b�h�Čv�Z (MTR) �g�p���� Excel �̍ŏ��̃o�[�W�����ł����B�R���s���[�^�[�̃v���Z�b�T����v���Z�b�T�̃R�A���Ɋ֌W�Ȃ��A�Čv�Z���ɍő� 1024 �̓������s�X���b�h��g�p����悤�� Excel ��\���ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p101">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets. You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="58e48-108">���ꂼ��̃X���b�h�ɂ͊֘A����I�y���[�e�B���O �V�X�e���̃I�[�o�[�w�b�h�����邽�߁A�K�v�ȏ�ɑ����̃X���b�h��g�p����悤�� Excel ��\�����Ă͂����܂���B</span><span class="sxs-lookup"><span data-stu-id="58e48-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="58e48-109">�R���s���[�^�[�ɕ����̃v���Z�b�T�܂��̓v���Z�b�T�̃R�A�����ڂ���Ă���ꍇ�́A�I�y���[�e�B���O �V�X�e�����A�œK�ȕ��@�Ńv���Z�b�T�ɃX���b�h����蓖�Ă܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="58e48-110">Excel の MTR の概要</span><span class="sxs-lookup"><span data-stu-id="58e48-110">Excel MTR overview</span></span>

<span data-ttu-id="58e48-p102">Excel �́A�v�Z�\`�F�[���̊e�����̂����A�ʁX�̃X���b�h�ŕ��s�I�ɍČv�Z�ł��镔������ʂ��悤�Ƃ��܂��B���̔��ɒP���ȃc���[ (x �� y �́Ay �� x �ɂ݈̂ˑ����Ă��邱�Ƃ�Ӗ�����) �́A���̗������Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p102">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads. The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="58e48-113">**�} 1. �ʁX�̃X���b�h�ł̓������s�v�Z**</span><span class="sxs-lookup"><span data-stu-id="58e48-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="58e48-114">![異なるスレッドで同時に計算します。](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "異なるスレッドで同時に計算します。")</span><span class="sxs-lookup"><span data-stu-id="58e48-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="58e48-115">A1 �̌v�Z���ςނƁA����̃X���b�h�ł� A2�AA3 �̏��Ɍv�Z���ł���悤�ɂȂ�A�����ɁA�������̃X���b�h�ł� B1�AC1 �̏��Ɍv�Z���ł���悤�ɂȂ�܂� (���ׂẴZ�����X���b�h �Z�[�t�ł���Ɖ��肵�Ă��܂�)�B</span><span class="sxs-lookup"><span data-stu-id="58e48-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="58e48-p103">�X���b�h �Z�[�t�ȃZ���Ƃ����p��́A�X���b�h �Z�[�t�Ȋ֐��݂̂�܂ރZ����Ӗ����܂��B�X���b�h �Z�[�t�ł��邩�ǂ����ɂẮA[Excel �ŃX���b�h �Z�[�t�ƌ��Ȃ������ (���Ȃ���Ȃ����)](#xl2007xllsdk_threadsafe)�ŏڂ���������܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p103">The term thread-safe cell means a cell that only contains thread-safe functions. What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="58e48-p104">�قƂ�ǂ̎��p�I�ȃu�b�N�ɂ́A���̗����͂邩�ɕ��G�Ȉˑ��֌W�c���[���܂܂�Ă��܂��B����ɁA�Z���̍Čv�Z�ɂ����鎞�Ԃ͌v�Z����������܂ŕs���ł���A�֐��̈����ɂ���đ啝�ɈقȂ邱�Ƃ�����܂��B�ŗǂ̌��ʂ𓾂邽�߂ɁAExcel �́A����ȏ�̍œK�����ł��Ȃ��Ȃ�܂ŁA�v�Z�̂��тɌv�Z�����̉��P����݂܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p104">Most practical workbooks contain far more complex dependency trees than this example. Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments. To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="58e48-121">Excel �́A���̍��ڂ̎��s�ɒP��̃��C�� �X���b�h��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="58e48-122">�g�ݍ��݃R�}���h</span><span class="sxs-lookup"><span data-stu-id="58e48-122">Built-in commands</span></span>
    
- <span data-ttu-id="58e48-123">XLL �R�}���h</span><span class="sxs-lookup"><span data-stu-id="58e48-123">XLL commands</span></span>
    
- <span data-ttu-id="58e48-124">XLL アドイン マネージャー インターフェイスの関数 (**xlAutoOpen**関数というように)</span><span class="sxs-lookup"><span data-stu-id="58e48-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="58e48-125">Microsoft Visual Basic for Applications (VBA) �̃��[�U�[��\`�R�}���h (�ʏ�̓}�N���ƌĂ΂�܂�)</span><span class="sxs-lookup"><span data-stu-id="58e48-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="58e48-126">VBA �̃��[�U�[��\`�֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="58e48-127">�g�ݍ��݂̃X���b�h �Z�[�t�ł͂Ȃ����[�N�V�[�g�֐� (���̃Z�N�V�����Ɉꗗ������܂�)</span><span class="sxs-lookup"><span data-stu-id="58e48-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="58e48-128">XLM マクロ シートのユーザー定義コマンドとユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="58e48-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="58e48-129">COM �A�h�C���̃R�}���h�Ɗ֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="58e48-130">����t���t�H�[�}�b�g����̊֐��Ɖ��Z�q</span><span class="sxs-lookup"><span data-stu-id="58e48-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="58e48-131">ワークシートの式で使用された定義済みの名前定義内の関数と演算子</span><span class="sxs-lookup"><span data-stu-id="58e48-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="58e48-132">�����ҏW�{�b�N�X��̎��̋����I�ȕ]�� ( **F9** �L�[��g�p)</span><span class="sxs-lookup"><span data-stu-id="58e48-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="58e48-p105">���ׂẴ��[�N�V�[�g�̐����́A�֐����X���b�h �Z�[�t���ǂ����Ɋ֌W�Ȃ��A���C�� �X���b�h�ŕ]������܂��B�������A�����̃X���b�h��g�p����悤�� Excel ��\�����Ă���ꍇ������܂��B���[�U�[�������̃X���b�h��g�p����悤�Ɏw�肷��ƁA�X���b�h �Z�[�t�̃Z���ɂ͒ǉ��̃X���b�h���g�p����܂��B���ו��U�̊ϓ_����̍������ɓK���ꍇ�́A���C�� �X���b�h��X���b�h �Z�[�t�ȃZ���Ɏg�p����܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p105">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread. When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells. Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="58e48-136">�����ł����x�������ׂ����ƂƂ��āAExcel �͈�x�ɕ����̃R�}���h����s���܂���B���̂��߁A�X���b�h ���[�J�� �������ƃN���e�B�J�� �Z�N�V�����̎g�p�ȂǁA�X���b�h �Z�[�t�Ȋ֐���L�q����Ƃ��Ɠ��l�̒��ӂ𕥂��K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="58e48-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="58e48-137">何し、は見なされませんスレッド セーフ Excel を使用して</span><span class="sxs-lookup"><span data-stu-id="58e48-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="58e48-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="58e48-138"></span></span>

<span data-ttu-id="58e48-139">Excel �ł́A���̂�̂������X���b�h �Z�[�t�ƌ��Ȃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="58e48-140">Excel �̒P�����Z�q�Ɠ񍀉��Z�q�̂��ׂ�</span><span class="sxs-lookup"><span data-stu-id="58e48-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="58e48-141">Excel 2007 �ȍ~�̑g�ݍ��݃��[�N�V�[�g�֐��̂قƂ�ǂ��ׂ� (��O�̈ꗗ��Q��)</span><span class="sxs-lookup"><span data-stu-id="58e48-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="58e48-142">�X���b�h �Z�[�t�Ƃ��Ė����I�ɓo�^����Ă��� XLL �A�h�C���֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="58e48-143">���̑g�ݍ��݃��[�N�V�[�g�֐��́A�X���b�h �Z�[�t�ł͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="58e48-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="58e48-144">**PHONETIC**</span><span class="sxs-lookup"><span data-stu-id="58e48-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="58e48-145">**CELL** ("����" �܂��� "�A�h���X" �̂ǂ��炩�̈������g�p���ꂽ�ꍇ)</span><span class="sxs-lookup"><span data-stu-id="58e48-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="58e48-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="58e48-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="58e48-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="58e48-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="58e48-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="58e48-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="58e48-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="58e48-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="58e48-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="58e48-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="58e48-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="58e48-151">**CUBESET**</span></span>
    
- <span data-ttu-id="58e48-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="58e48-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="58e48-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="58e48-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="58e48-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="58e48-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="58e48-155">**ADDRESS** (5 �Ԗڂ̃p�����[�^�[ "sheet_name" ���w�肳��Ă���ꍇ)</span><span class="sxs-lookup"><span data-stu-id="58e48-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="58e48-156">データベースのいずれかのピボット テーブルを参照する関数 (**DSUM**、 **DAVERAGE**というように)</span><span class="sxs-lookup"><span data-stu-id="58e48-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="58e48-157">**エラーです。タイプ**</span><span class="sxs-lookup"><span data-stu-id="58e48-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="58e48-158">**HYPERLINK**</span><span class="sxs-lookup"><span data-stu-id="58e48-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="58e48-159">���m�ɂ��邽�߂ɁA�X���b�h �Z�[�t�ƌ��Ȃ���Ȃ���̂�����܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="58e48-160">VBA �̃��[�U�[��\`�֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="58e48-161">COM �A�h�C���̃��[�U�[��\`�֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="58e48-162">XLM �}�N�� �V�[�g�̃��[�U�[��\`�֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="58e48-163">�����I�ɃX���b�h �Z�[�t�Ƃ��ēo�^����Ă��Ȃ� XLL �A�h�C���֐�</span><span class="sxs-lookup"><span data-stu-id="58e48-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="58e48-164">���̑���Ɗ֐��̓X���b�h �Z�[�t�Ƃ͌��Ȃ���܂���B�܂��A�X���b�h �Z�[�t�Ƃ��ēo�^���� XLL �֐�����Ăяo�����Ǝ��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="58e48-165">呼び出しを XLM 情報関数では、たとえば、 **xlfGetCell** (**取得します。セル**)。</span><span class="sxs-lookup"><span data-stu-id="58e48-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="58e48-166">**XlfSetName** (**SET.NAME**) を定義または xll ファイルの内部名を削除する場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="58e48-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="58e48-167">�X���b�h �Z�[�t�ł͂Ȃ����[�U�[��\`�֐��� **xlUDF** ��g�p�����Ăяo���B</span><span class="sxs-lookup"><span data-stu-id="58e48-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="58e48-168">式のスレッドの安全でない関数が含まれているかの定義には、スレッドの安全でない関数が含まれている定義済みの名前が含まれている[xlfEvaluate](xlfevaluate.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="58e48-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="58e48-169">�u���[�N�����N���A���� [xlAbort](xlabort.md) �֐��̌Ăяo���B</span><span class="sxs-lookup"><span data-stu-id="58e48-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="58e48-170">�v�Z����Ă��Ȃ��Z���̎Q�Ƃ̒l��擾���� [xlCoerce](xlcoerce.md) �֐��̌Ăяo���B</span><span class="sxs-lookup"><span data-stu-id="58e48-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="58e48-171">XLL ���[�N�V�[�g�֐� ( **xlcSave** �Ȃ�) �ł́AC API �R�}���h�̌Ăяo����������Ă��܂���B���̊֐����X���b�h �Z�[�t�Ƃ��ēo�^����Ă��邩�ǂ����͊֌W����܂���B</span><span class="sxs-lookup"><span data-stu-id="58e48-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="58e48-p106">�X���b�h �Z�[�t�Ƃ��Đ錾���ꂽ XLL �֐��� XLM ���֐���Ăяo���Ȃ����Ƃ�A�v�Z����Ă��Ȃ��Z����Q�Ƃł��Ȃ����Ƃ���AExcel �� �}�N�� �V�[�g�Ɠ����Ƃ��ēo�^���� XLL �֐���X���b�h �Z�[�t�Ƃ��Ă�o�^���邱�Ƃ�����܂���B���̂��߁A **xlCoerce** ��g�p���Čv�Z����Ă��Ȃ��Z���̎Q�Ƃ̒l��擾���悤�Ƃ���ƁA **xlretUncalced** �G���[�Ŏ��s���܂��BXLM ���֐��̌Ăяo���́A **xlretFailed** �G���[�Ŏ��s���܂��B���̑��̑O�q�����|�C���g�́AExcel C API �ɓ������ꂽ�G���[ �R�[�h **xlretNotThreadSafe** �Ŏ��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p106">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe. Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error. Calling an XLM information function fails with an **xlretFailed** error. The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="58e48-176">C API ��p�̃R�[���o�b�N�֐��́A���ׂăX���b�h �Z�[�t�ł��B</span><span class="sxs-lookup"><span data-stu-id="58e48-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="58e48-177">**xlCoerce** (�������A�v�Z����Ă��Ȃ��Z���̎Q�Ƃ̋����^�ϊ��͎��s���܂�)</span><span class="sxs-lookup"><span data-stu-id="58e48-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="58e48-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="58e48-178">**xlFree**</span></span>
    
- <span data-ttu-id="58e48-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="58e48-179">**xlStack**</span></span>
    
- <span data-ttu-id="58e48-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="58e48-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="58e48-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="58e48-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="58e48-182">**xlAbort** (�u���[�N�����N���A���邽�߂Ɏg�p����ꍇ������܂�)</span><span class="sxs-lookup"><span data-stu-id="58e48-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="58e48-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="58e48-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="58e48-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="58e48-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="58e48-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="58e48-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="58e48-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="58e48-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="58e48-187">�B��̗�O�� **xlSet** �֐��ł��B�����̏ꍇ�A���̊֐��̓R�}���h�Ɠ����ł��邽�߁A�ǂ̂悤�ȃ��[�N�V�[�g�֐������Ăяo���ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="58e48-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="58e48-p107">XLL ���[�N�V�[�g�֐��́A�X���b�h �Z�[�t�Ƃ��� Excel �ɓo�^�ł��܂��B����ɂ��A���̊֐������S�ɕ����̃X���b�h�œ����ɌĂяo���邱�Ƃ� Excel �ɒʒm���܂��B�������A���ꂪ�����ł��邱�Ƃ͎����Ŋm�F����K�v������܂��B�X���b�h �Z�[�t�Ƃ��ēo�^�����֐��̓��삪�X���b�h �Z�[�t�łȂ��ƁAExcel ���s����ɂȂ邱�Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p107">An XLL worksheet function can be registered with Excel as thread safe. This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case. You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="58e48-191">としてスレッド セーフな XLL 関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="58e48-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="58e48-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="58e48-192"></span></span>

<span data-ttu-id="58e48-193">�X���b�h �Z�[�t�Ȋ֐���L�q����Ƃ��ɁA�J���҂��]���K�v�̂��郋�[���͎��̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="58e48-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="58e48-194">�X���b�h �Z�[�t�ł͂Ȃ��\���̂���ʂ� DLL ��̃��\�[�X��Ăяo���Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="58e48-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="58e48-195">C API �܂��� COM ��ʂ��ăX���b�h �Z�[�t�łȂ��Ăяo����s��Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="58e48-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="58e48-196">�N���e�B�J�� �Z�N�V������g�p���āA�����̃X���b�h�œ����Ɏg�p�����\���̂��郊�\�[�X��ی삷��B</span><span class="sxs-lookup"><span data-stu-id="58e48-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="58e48-197">�X���b�h�ŗL�̃X�g���[�W�ɂ̓X���b�h ���[�J�� ��������g�p���āA�֐���̐ÓI�ϐ��̓X���b�h ���[�J���ϐ��ɒu��������B</span><span class="sxs-lookup"><span data-stu-id="58e48-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="58e48-198">Excel �ɂ́A��� 1 �̐������ۂ����܂��B�X���b�h �Z�[�t�Ȋ֐���}�N�� �V�[�g�Ɠ����Ȃ�̂Ƃ��ēo�^���邱�Ƃ͂ł��܂���B���̂��߁AXLM ���֐���Ăяo�����Ƃ�A�Čv�Z����Ă��Ȃ��Z���̒l��擾���邱�Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="58e48-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="58e48-199">メモリの競合</span><span class="sxs-lookup"><span data-stu-id="58e48-199">Memory contention</span></span>
<span data-ttu-id="58e48-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="58e48-200"></span></span>

<span data-ttu-id="58e48-201">�}���\`�X���b�h �V�X�e���́A2 �̊�{�I�Ȗ��ɑΏ�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="58e48-202">�����̃X���b�h���ǂݏ������郁�����̕ی���@�B</span><span class="sxs-lookup"><span data-stu-id="58e48-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="58e48-203">���s���̃X���b�h�Ɋ֘A�t�����ăv���C�x�[�g�ɂȂ郁�����̍쐬���@�ƃA�N�Z�X���@�B</span><span class="sxs-lookup"><span data-stu-id="58e48-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="58e48-p108">Windows �I�y���[�e�B���O �V�X�e���� Windows �\�t�g�E�F�A�J���L�b�g (SDK) �ɂ́A����痼���ɂ��ꂼ��Ή�����c�[���ł���N���e�B�J�� �Z�b�V�����ƃX���b�h ���[�J�� �X�g���[�W (TLS) API ��g�p�ł��܂��B�ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="58e48-p108">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="58e48-p109">�ŏ��̖��́A���Ƃ��΁A2 �̃��[�N�V�[�g�֐� (�܂��͓����֐��� 2 �̓������s�C���X�^���X) �� 1 �� DLL �v���W�F�N�g��̃O���[�o���ϐ��ɃA�N�Z�X���� (�܂��͕ύX�������) �K�v������ꍇ�ɔ������܂��B���̂悤�ȃO���[�o���ϐ��́A�O���[�o���ɃA�N�Z�X�ł���N���X �I�u�W�F�N�g�̃C���X�^���X��ɉB����Ă��邱�Ƃ�����_�ɒ��ӂ��K�v�ł��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p109">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project. Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="58e48-p110">2 �ڂ̖��́A���Ƃ��΁A���[�N�V�[�g�֐����֐��{�̂̃R�[�h��ŐÓI�ȕϐ��܂��̓I�u�W�F�N�g�錾���Ă���ꍇ�ɔ������܂��BC/C++ �R���p�C���́A���ׂẴX���b�h���g�p���� 1 �̃R�s�[�݂̂�쐬���܂��B���̂��߁A�֐��̈���̃C���X�^���X���l��ύX���Ă���Ƃ��ɁA�ʂ̃X���b�h�̂������̃C���X�^���X�͒l���ȑO�ɐݒ肳�ꂽ��e���Ƒz�肵�Ă���\��������Ƃ������Ƃł��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p110">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code. The C/C++ compiler only creates a single copy that all threads use. This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="58e48-211">MTR のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="58e48-211">Example applications of MTR</span></span>
<span data-ttu-id="58e48-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="58e48-212"></span></span>

<span data-ttu-id="58e48-p111">���[�N�V�[�g�֐���G�N�X�|�[�g���� XLL �́AExcel �̃}���\`�X���b�h�Čv�Z (MTR) �𗘗p�ł��܂� (�Y������֐����A�X���b�h �Z�[�t�łȂ��A�N�V��������s����K�v���Ȃ��ꍇ)�B����ɂ��AExcel �̓u�b�N��\�Ȍ���Z���ԂɍČv�Z�ł���悤�ɂȂ邽�߁A������A�v���P�[�V�����ɂƂ��Ė]�܂�����ԂɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p111">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions. This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="58e48-215">具体的には、MTR は、ユーザー定義関数 (Udf) 目的の結果を取得する外部プロセスを呼び出すこと自体を呼び出しているブックの再計算時間に大きな影響を及ぼします。</span><span class="sxs-lookup"><span data-stu-id="58e48-215">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result.</span></span> <span data-ttu-id="58e48-216">具体的には、UDF を同時に多数の要求を処理できるリモート サーバーを呼び出すと関数呼び出しを含むブックを検討してください。</span><span class="sxs-lookup"><span data-stu-id="58e48-216">In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function.</span></span> <span data-ttu-id="58e48-217">ブックの再計算がシングル スレッドの場合、各 UDF を呼び出すし、リモート サーバーにする必要があります完了次のいずれかをする前に。</span><span class="sxs-lookup"><span data-stu-id="58e48-217">If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made.</span></span> <span data-ttu-id="58e48-218">これは、一度に多数の呼び出しを処理するサーバーの能力を浪費します。</span><span class="sxs-lookup"><span data-stu-id="58e48-218">This wastes the server's ability to process many calls at once.</span></span> <span data-ttu-id="58e48-219">ブックの再計算は、マルチ スレッドは、同時にまたは連続で、Excel は複数の呼び出しをことができます。</span><span class="sxs-lookup"><span data-stu-id="58e48-219">If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="58e48-p113">�T�[�o�[�Ɠ����� (���̐��� N �Ƃ���) �̃X���b�h��g�p����悤�� Excel ���\������Ă��āA�u�b�N�̈ˑ��֌W�c���[�̃g�|���W�ɂ��̗]�n������΁A���v�̍Čv�Z���Ԃ̓V���O�� �X���b�h�̌v�Z���Ԃ� 1/N �߂��܂ŒZ�k�����\��������܂��B����́A�u�b�N����s���Ă���N���C�A���g �R���s���[�^�[���v���Z�b�T�� 1 �������ڂ��Ă���ꍇ�ɂ���Ă͂܂�\��������܂��B���ɁA�T�[�o�[�̌Ăяo���ɂ����鎞�Ԃ��A�T�[�o�[�ŌĂяo����������鎞�Ԃ���Z���ꍇ�ɓ��Ă͂܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p113">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time. This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="58e48-p114">�ǉ��̃X���b�h�ɂ́A���ꂼ��ɃI�y���[�e�B���O �V�X�e���̃I�[�o�[�w�b�h�����݂��܂��B���̂��߁A����̃u�b�N�Ɠ���̃T�[�o�[����уN���C�A���g �R���s���[�^�[�ɂ��āA���炩�̎����� Excel �ɐݒ肷��œK�ȃX���b�h���������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p114">There is operating system overhead for each additional thread. Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="58e48-p115">���Ƃ��΁AExcel ����s���Ă���V���O�� �v���Z�b�T�̃R���s���[�^�[�ƁA1,000 �̃Z����܂�ł���u�b�N�ɂ��čl���Ă݂܂��傤�B����́AUDF ��Ăяo���A���� UDF �� 1 �ȏ�̃����[�g �T�[�o�[��Ăяo���܂��B1,000 �̃Z�������݂Ɉˑ����Ă��Ȃ��Ɖ��肷��ƁAExcel �͌㑱�̌Ăяo������s���邽�߂ɌĂяo���̊�����ҋ@����K�v�͂���܂��� (���̐���́A���̗�ɉe����^���邱�ƂȂ��A������x�̊ɘa���\�ł�)�B�T�[�o�[�� 100 ���̗v���̓����������\�ŁAExcel �� 100 �X���b�h��g�p����悤�ɍ\������Ă���ƁA���s���Ԃ� 1 �X���b�h�݂̂�g�p�����ꍇ�� 1/100 �߂��ɂ܂ŒZ�k�ł��܂��BExcel ���e�X���b�h�ɃZ������蓖�Ă邽�߂ɂ�����I�[�o�[�w�b�h�ƁA�I�y���[�e�B���O �V�X�e���� 100 �X���b�h��Ǘ����邽�߂ɂ�����I�[�o�[�w�b�h�ɂ��A���ۂɂ́A����قǂ܂ł̎��ԒZ�k�ɂ͂Ȃ�܂���B�܂��A�T�[�o�[�̃X�P�[�����O���K�؂ł���A100 ���̃^�X�N�̓���������˗����Ă�ʂ̃^�X�N�̊������Ԃɑ傫�ȉe�����Ȃ��Ƃ������Ƃ�A�ÖٓI�ɉ��肵�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p115">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells. It calls a UDF, which in turn calls one or more remote servers. Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next. (Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used. The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great. There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="58e48-230">���̋Z�@���傫�ȃ����b�g�ɂȂ���p�I�A�v���P�[�V�����Ƃ��āA�����e�J�����@�ȂǁA�����ȃ^�X�N�ɕ������ĕ����̃T�[�o�[�Ɉ˗��ł��鐔�l�W��^�̃^�X�N���������܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="58e48-231">Excel Services に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="58e48-231">Excel Services considerations</span></span>
<span data-ttu-id="58e48-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="58e48-232"></span></span>

<span data-ttu-id="58e48-p116">Excel Services �́A�T�[�o�[�ł� Excel �X�v���b�h�V�[�g�̓ǂݍ��݁A�v�Z�A����у����_�����O��T�|�[�g���܂��B���[�U�[�́A�W���̃u���E�U �c�[����g�p���āA�X�v���b�h�V�[�g�ɃA�N�Z�X���đΘb�������s�ł���悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p116">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server. Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="58e48-p117">Excel Services �� UDF �́AMicrosoft .NET Framework �̃}�l�[�W �R�[�h��g�p���č쐬��, .NET �A�Z���u����ʂ��Ďg�p�\�ɂȂ�܂��BXLL �́AExcel Services �ł̓T�|�[�g����܂���B�}�l�[�W �R�[�h �T�[�o�[ UDF ���\�[�X�́AXLL ��Ăяo���Ă��̋@�\�ɃA�N�Z�X�ł��邽�߁A���[�U�[�̓T�[�o�[�œǂݍ��܂ꂽ�u�b�N�ƃN���C�A���g�œǂݍ��܂ꂽ�u�b�N�œ����@�\��g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p117">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly. XLLs are not supported by Excel Services. A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="58e48-p118">���̕��@�� XLL �̊֐���g�p�ł���悤�ɂ���ɂ́A�����Ɩ߂�l��l�C�e�B�u �f�[�^�^���� .NET Framework �}�l�[�W �f�[�^�^�ɕϊ����� XLL �֐���Ăяo�� .NET �A�Z���u���ŁA�֐�����b�v����K�v������܂��B.NET ���b�p�[�́A�A�N�Z�X�Ώۂ� XLL �֐����Ƃ� 1 �̃T�[�o�[ UDF ��G�N�X�|�[�g���܂��B�ǉ��̗v���Ƃ��āA���̕��@�ŌĂяo����� XLL �֐��̓X���b�h �Z�[�t�ł��邱�Ƃ��K�v�ł��BXLL �֐��͖{���̕��@�� Excel �ɓo�^����Ă��Ȃ����߁A���̊֐�������I�ɃX���b�h �Z�[�t�ɂ�����@���T�[�o�[�� .NET ���b�p�[�ɂ͂���܂���B����́AXLL �J���҂̐ӔC�ŕۏ؂��܂��B</span><span class="sxs-lookup"><span data-stu-id="58e48-p118">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions. The .NET wrapper would export one server UDF for each XLL function being accessed. An additional requirement is that any XLL functions called in this way must be thread safe. Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe. It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58e48-243">�֘A����</span><span class="sxs-lookup"><span data-stu-id="58e48-243">See also</span></span>

- [<span data-ttu-id="58e48-244">Excel �̍Čv�Z</span><span class="sxs-lookup"><span data-stu-id="58e48-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="58e48-245">Excel �̃������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="58e48-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- <span data-ttu-id="58e48-246">[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="58e48-246">[Accessing XLL Code in Excel](accessing-xll-code-in-excel.md)</span></span>  
- [<span data-ttu-id="58e48-247">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="58e48-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="58e48-248">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="58e48-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

