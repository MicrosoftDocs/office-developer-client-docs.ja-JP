---
title: Excel ���[�N�V�[�g�Ǝ��̕]��
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 543ff7fcbc88253dafd7fc6e7000bf9657d8c258
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798854"
---
# <a name="excel-worksheet-and-expression-evaluation"></a><span data-ttu-id="45c5b-104">Excel ���[�N�V�[�g�Ǝ��̕]��</span><span class="sxs-lookup"><span data-stu-id="45c5b-104">Excel Worksheet and Expression Evaluation</span></span>

 <span data-ttu-id="45c5b-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="45c5b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="45c5b-106">Microsoft Excel ���[�N�V�[�g�̃Z���̓�e�́A���� 4 �̊�{�I�ȃf�[�^�^�̂����ꂩ�ɕ]������܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-106">Microsoft Excel worksheet cell contents are evaluated into one of four basic data types:</span></span>
  
- <span data-ttu-id="45c5b-107">**Numbers**</span><span class="sxs-lookup"><span data-stu-id="45c5b-107">**Numbers**</span></span>
    
- <span data-ttu-id="45c5b-108">**Boolean TRUE** �܂��� **FALSE**</span><span class="sxs-lookup"><span data-stu-id="45c5b-108">**Boolean TRUE** or **FALSE**</span></span>
    
- <span data-ttu-id="45c5b-109">**Strings**</span><span class="sxs-lookup"><span data-stu-id="45c5b-109">**Strings**</span></span>
    
- <span data-ttu-id="45c5b-110">**エラー**</span><span class="sxs-lookup"><span data-stu-id="45c5b-110">**Errors**</span></span>
    
<span data-ttu-id="45c5b-111">�֐��̈����Ƃ��āA�܂��͔z�񐔎���̕����̃Z���ɂ܂�����l�Ƃ��āA�����̃f�[�^�^�̍����z��𐔎��ɓ��͂��邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-111">Mixed-type arrays of these types can also be entered into formulas as arguments to functions or as values spanning more than one cell in an array formula.</span></span>
  
<span data-ttu-id="45c5b-p101">���[�U�[ (�܂��̓R�}���h �}�N��) ���Z���ɕ��������͂���ƁAExcel �͓��͂̉�߂���݁A��߂ł��Ȃ��ꍇ�ɂ̓G���[ ���b�Z�[�W��\�����܂��B���͒l��������̃v���t�B�b�N�X (�P����p��) �Ŏn�܂��Ă���ꍇ�́AExcel �́A���ׂĂ̓��͕�������̂܂ܕύX�����ɃZ���ɔz�u���܂��B(������̃v���t�B�b�N�X�͕\������܂���B)���͒l���A **=** �A **+** �A **-** �̂����ꂩ�Ŏn�܂�ꍇ�AExcel �͓��͒l�𐔎��Ƃ��ĉ�߂��悤�Ƃ��܂��B�\�����������Ȃ��ꍇ��]������~�����ꍇ�́A�G���[���\������A�Z���͕ҏW���[�h�ɂȂ�܂��B����ȊO�̏ꍇ�AExcel �͉��Z�q����ъ֐����Ƃ��̈����̎��ʁA�ϊ��A�]������݂܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p101">When a user (or a command macro) enters something into a cell, Excel tries to interpret the input and displays an error message if it cannot. If the input starts with a string prefix (a single quotation mark) Excel places all the input characters in the cell as provided, with no modification. (The string prefix is not displayed.) If the input begins with **=**, **+**, or **-**, Excel tries to interpret the input as a formula. If the syntax is incorrect or evaluation is stopped, an error is displayed, and the cell is put in edit mode. Otherwise, Excel tries to identify, convert, and evaluate operators and function names and their arguments.</span></span> 
  
<span data-ttu-id="45c5b-p102">���Z�q���K�p�����O�ɁA�I�y�����h�͍�����E�ɕ]������܂��B�֐��́A�D�揇�ʂ̍������Z�q�Ɠ���q�̈�ԓ���̉��Z�q����]������܂��B�֐��̈�����I�y�����h���A�\�������f�[�^�^�ɕϊ��ł��Ȃ��ꍇ�A�]���͎��s���A **#VALUE!** �G���[�ɂȂ�܂��B�g�[�N�� (���e�����l�ł͂Ȃ�) ���֐������\`���A���x���Ƃ��ĔF������Ȃ��ꍇ�A�]���͎��s���A **#NAME?** �G���[�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p102">Operands are evaluated from left to right before the operator is applied. Functions are evaluated starting with the highest-precedence operators and innermost (most nested). If function arguments or operands cannot be converted to the types expected, evaluation fails and results in a **#VALUE!** error. When a token (that is not a literal value) is not recognized as a function or defined name or label, evaluation fails and results in a **#NAME?** error.</span></span> 
  
<span data-ttu-id="45c5b-p103">���͒l����L�̂�����ł�n�܂��Ă��Ȃ��ꍇ�́A���t�A�����A�ʉ݁A�p�[�Z���e�[�W�A���l�ȂǁA���m�̓��̓p�^�[���ɏƂ炵�ă\`�F�b�N���A�����ɉ����ĉ�߂���܂��B����́A���P�[���ŗL�̕��@�ōs���܂��B��L�̂�����̕��@�ł��߂ł��Ȃ��ꍇ�́A������Ƃ��ĔF����������A�Z���̓�e�͕ύX����܂���B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p103">If the input does not start with any of these things, Excel checks against known patterns of input such as dates, times, currency amounts, percentages, or numbers, and interprets accordingly. This is done in a locale-specific way. If none of these interpretations makes sense, Excel reverts to considering the input as a string and places it in the cell unchanged.</span></span>
  
<span data-ttu-id="45c5b-p104">Excel �͑��̃f�[�^�^��T�|�[�g���Ă���A���̒��ōł�悭�m���Ă���̂́A�͈͎Q�Ƃł��B�Q�ƈ�����Ƃ�Ȃ����Z�q��֐��̈�����]��������A�܂��̓Z���̐�����ɂ��鎮��Q�Ƃɏk�߂��肷��ƁA�Q�Ƃ͎Q�Ɛ�Z���̒l�ɕϊ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p104">Excel supports other data types, the most visible of which is a range reference. Excel converts references to the values of the referred-to cells when evaluating arguments for operators and functions that do not take reference arguments, or when the expression in a cell formula reduces to a reference.</span></span>
  
<span data-ttu-id="45c5b-p105">Excel �ł́AXLM �֐� **EVALUATE** �܂��͂���ɑ������� C API�֐� **xlfEvaluate** ��g���āA�L���ȕ������A���[�N�V�[�g�p�̊�{�I�� 4 �̃f�[�^�^�̂����ꂩ�ɏk�߂�@�\�����J����Ă��܂��B���ł���̊֐���g�p����ƁADLL �R�[�h��̖��O�t���͈͂�ȒP�ɕ]�����邱�Ƃ��ł��܂��B���̊֐��́A�G���[���b�Z�[�W��\��������A�Z���̕ҏW��\�ɂ����肷��̂ł͂Ȃ��A���̕]�����ł��Ȃ��ꍇ�� **#VALUE!** �G���[��Ԃ��Ƃ����_�ŁA�O�q�̓���Ƃ͈قȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p105">Excel exposes the ability to reduce any valid character string to one of the basic four worksheet data types with the XLM function **EVALUATE** and its C API equivalent **xlfEvaluate**. This function provides, among other things, a simple way to evaluate named ranges in DLL code. This function differs from the behavior described earlier only in that instead of displaying error messages or enabling cell editing, it returns a **#VALUE!** error if the expression evaluation fails.</span></span> 
  
## <a name="numbers"></a><span data-ttu-id="45c5b-131">���l</span><span class="sxs-lookup"><span data-stu-id="45c5b-131">Numbers</span></span>

<span data-ttu-id="45c5b-p106">Excel �̃��[�N�V�[�g�ԍ��͂��ׂāA8 �o�C�g�̔{���x���������_ (���ׂĂ̐�����܂�) �œ���I�ɕ\����܂��B�������AExcel �ɂ����邱���̐��l�̎����́A�ȉ��̕\�Ɏ����悤�ɁAIEEE �K�i�Ɋ��S�ɂ͏������Ă��܂���B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p106">All worksheet numbers in Excel are represented internally as 8-byte double-precision floating point, including all integers. However, the implementation of these numbers in Excel is not fully IEEE compliant, as shown in the following table.</span></span>
  
|<span data-ttu-id="45c5b-134">**�^**</span><span class="sxs-lookup"><span data-stu-id="45c5b-134">**Type**</span></span>|<span data-ttu-id="45c5b-135">**�ő�**</span><span class="sxs-lookup"><span data-stu-id="45c5b-135">**Maximum**</span></span>|<span data-ttu-id="45c5b-136">**�ŏ�**</span><span class="sxs-lookup"><span data-stu-id="45c5b-136">**Minimum**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45c5b-137">IEEE 8 �o�C�g�̔{���x���������_�^</span><span class="sxs-lookup"><span data-stu-id="45c5b-137">IEEE 8-byte double</span></span>  <br/> |<span data-ttu-id="45c5b-138">1.7976931348623157E+308</span><span class="sxs-lookup"><span data-stu-id="45c5b-138">1.7976931348623157E+308</span></span>  <br/> |<span data-ttu-id="45c5b-139">2.2250738585072014E-308</span><span class="sxs-lookup"><span data-stu-id="45c5b-139">2.2250738585072014E-308</span></span>  <br/> |
|<span data-ttu-id="45c5b-140">���[�N�V�[�g (�֐��܂��͓\��t���l�ɂ���ĕԂ����)</span><span class="sxs-lookup"><span data-stu-id="45c5b-140">Worksheet (returned by function or paste value)</span></span>  <br/> |<span data-ttu-id="45c5b-141">1.7976931348623157E+308</span><span class="sxs-lookup"><span data-stu-id="45c5b-141">1.7976931348623157E+308</span></span>  <br/> |<span data-ttu-id="45c5b-142">2.22507385850721E-308</span><span class="sxs-lookup"><span data-stu-id="45c5b-142">2.22507385850721E-308</span></span>  <br/> |
|<span data-ttu-id="45c5b-143">���[�N�V�[�g (�葀�����)</span><span class="sxs-lookup"><span data-stu-id="45c5b-143">Worksheet (manual input)</span></span>  <br/> |<span data-ttu-id="45c5b-144">9.99999999999999E+307</span><span class="sxs-lookup"><span data-stu-id="45c5b-144">9.99999999999999E+307</span></span>  <br/> |<span data-ttu-id="45c5b-145">2.22507385850721E-308</span><span class="sxs-lookup"><span data-stu-id="45c5b-145">2.22507385850721E-308</span></span>  <br/> |
   
<span data-ttu-id="45c5b-146">IEEE �񐳋K���� ( 2.2250738585072009E?308 ���� 4.9406564584124654E?324 �͈̔͂̐��l) �́AExcel ���[�N�V�[�g�ł̓T�|�[�g����Ă��܂��񂪁AVBA �̔{���x���������_�^�ł̓T�|�[�g����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-146">IEEE subnormal numbers (that is, numbers in the range 2.2250738585072009E-308 to 4.9406564584124654E-324) are not supported in Excel worksheets but are supported by VBA Doubles.</span></span>
  
<span data-ttu-id="45c5b-147">DLL 関数では、無限大、または、無効な二重の +/-IEEE が返された場合 Excel 変換する **#NUM!** です。</span><span class="sxs-lookup"><span data-stu-id="45c5b-147">If a DLL function returns IEEE +/- infinity or an invalid double, Excel converts it to **#NUM!**.</span></span> <span data-ttu-id="45c5b-148">Subnormal すべて Excel で最小の正の標準よりも小さい数値が正の 0 に変換されます。</span><span class="sxs-lookup"><span data-stu-id="45c5b-148">All subnormal numbers and numbers smaller than the minimum positive normal in Excel are converted to positive zero.</span></span> <span data-ttu-id="45c5b-149">IEEE 負の 0 がサポートされている、つまり、DLL 関数によって返されることができ、として表示されます **-0**です。</span><span class="sxs-lookup"><span data-stu-id="45c5b-149">IEEE negative zero is supported, that is, it can be returned by a DLL function and is displayed as **-0**.</span></span> <span data-ttu-id="45c5b-150">(、**\<** 演算子が負のゼロをチェックしませんので **= A1\<0** A1 には、負のゼロが含まれている場合に**TRUE**に評価された)。</span><span class="sxs-lookup"><span data-stu-id="45c5b-150">(The **\<** operator does not check for negative zero, and so **=A1\<0** evaluates to **TRUE** if A1 contains negative zero).</span></span> 
  
<span data-ttu-id="45c5b-p108">���t�Ǝ����Ȃǂ̈ꕔ�̐��l�����́A��L��������͈͂ɐ�������Ă��邱�Ƃɒ��ӂ��Ă��������B�������Z�͎��ۂɂ͕��������_���Z�ł���A�ɒ[�ȏꍇ�́A���m�ɂ͐����̌��ʂɂȂ�ꍇ�ɔ񐮐��̌��ʂ����炷�ꍇ������܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p108">Note that certain number formats have narrower limits than these, for example, dates and times. Integer division is, in fact, floating point division and might, in extreme cases, yield a non-integer result where the precise result should be an integer.</span></span>
  
## <a name="long-unicode-strings"></a><span data-ttu-id="45c5b-153">���� Unicode ������</span><span class="sxs-lookup"><span data-stu-id="45c5b-153">Long Unicode Strings</span></span>

<span data-ttu-id="45c5b-p109">���݁AExcel ��ɕ\������Ă��镶����͂��ׂāA�����̃o�[�W�����ɂ����āA����I�� Unicode ������Ƃ��Ċi�[����܂��B���[�N�V�[�g�Ŏg�p���� Unicode ������ł́A�C�ӂ̗L���� Unicode ������ő� 32,767 (2<sup>15</sup>?- 1) �����܂ނ��Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p109">All strings the user sees in Excel have for many versions now been stored internally as Unicode strings. Unicode worksheet strings can be up to 32,767 (2<sup>15</sup> - 1) characters in length and can contain any valid Unicode character.</span></span> 
  
<span data-ttu-id="45c5b-p110">C API ���ŏ��ɓ������ꂽ�Ƃ��A���[�N�V�[�g�̕�����́A���� 255 �����̃o�C�g��ɐ�������Ă��܂������AC API �ł�A�����̐��������f����܂��BExcel 2007 �ł́AC API �́A���� Unicode �����������ł���悤�ɍX�V����Ă��܂��B�܂�ADLL �֐����K�؂ȕ��@�œo�^����Ă���΁AUnicode �̈�����󂯎������AUnicode �������Ԃ����肷�邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p110">When the C API was first introduced, worksheet strings were byte strings limited in length to 255 characters, and the C API reflected these limitations. With Excel 2007, the C API is updated to handle Excel long Unicode strings. This means that DLL functions registered in the right way can accept Unicode arguments and return Unicode strings.</span></span>
  
> [!NOTE]
> <span data-ttu-id="45c5b-159">�o�C�g��́A���ʌ݊����̂��߂� C API �Ŋ��S�ɃT�|�[�g����Ă��܂����A����܂łǂ��� 255 �����ɐ�������Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-159">Byte strings are still fully supported in the C API for backward compatibility; however they still have the same 255-character limit.</span></span> 
  
## <a name="returning-errors"></a><span data-ttu-id="45c5b-160">�G���[</span><span class="sxs-lookup"><span data-stu-id="45c5b-160">Returning Errors</span></span>

<span data-ttu-id="45c5b-p111">�֐��܂��͉��Z�q�̈�����K�؂Ȍ^�ɕϊ��ł��Ȃ��ꍇ�A���邢�͊֐��܂��͒�\`�ς݂̖��O���F������Ȃ��ꍇ�AExcel �̓Z����G���[�ɕ]�����܂��B�����̃V�i���I�͂�������L�Ő�����Ă��܂��B�g�ݍ��݃��[�N�V�[�g�֐��Ɖ��Z�q�����s�����ꍇ�A���[�U�[�ɃG���[�̎�ނ�ʒm����G���[��\������܂��B����̃A�h�C���֐��� Excel �̓���Ɛ�������G���[��Ԃ��悤�ɂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p111">Excel evaluates cells to errors where it cannot convert function or operator arguments to the correct type, or if it does not recognize a function or defined name. Both of these scenarios were described earlier. When the built-in worksheet functions and operators fail, they also result in errors that inform the user of the type of failure. You should have your own add-in functions return errors that are consistent with the behavior in Excel.</span></span>
  
### <a name="null"></a><span data-ttu-id="45c5b-165">#NULL!</span><span class="sxs-lookup"><span data-stu-id="45c5b-165">#NULL!</span></span>

<span data-ttu-id="45c5b-p112">**#NULL!** �G���[�́A�������� XLM ���֐��ɂ���ĕԂ���܂��B���Ƃ��΁A�v�����^�[���C���X�g�[������Ă��Ȃ��ꍇ�ɁA **GET.DOCUMENT(78)** ��Ăяo�����A�܂��͈��� 78 �œ����� C API �֐� **xlfGetDocument** ��Ăяo���ƁA���̃G���[���Ԃ���邱�ƂɂȂ�܂��B�܂��A��L�G���[�͋�̕����񂪕]�������ꍇ�Ȃǂɂ�A�ꕔ�̊֐��ŕԂ����\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p112">The **#NULL!** error is returned by some XLM information functions. For example, calling **GET.DOCUMENT(78)**, or the equivalent C API function **xlfGetDocument** with argument 78, when there are no printers installed results in this error being returned. It can also be returned by some functions when, for example, they evaluate an empty string.</span></span> 
  
<span data-ttu-id="45c5b-170">���̂�����̃G���[��K�؂ł͂Ȃ��Ɗ�����ꍇ��A�A�h�C���֐����炱�̃G���[��Ԃ��Ƃ悢�ł��傤�B</span><span class="sxs-lookup"><span data-stu-id="45c5b-170">You might want to return this error from your add-in function when none of the other errors seems appropriate.</span></span>
  
### <a name="div0"></a><span data-ttu-id="45c5b-171">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="45c5b-171">#DIV/0!</span></span>

<span data-ttu-id="45c5b-p113">���ꂪ 0 �ɕ]������邩�A�܂��͐��l�������� 0 �ȊO�̐��l�ŕ\���Ȃ��ꍇ�ɂ́AExcel �̏��Z���Z�q�� **#DIV/0!** �G���[��Ԃ��܂��B��\`��A���Z���֌W����ꕔ�̊֐��ł���̃G���[���Ԃ����ꍇ������܂��B���Ƃ��΁A���͒l�̂��������l�ɕϊ��ł��Ȃ��ꍇ�́A **AVERAGE** �ɂ�肱�̃G���[���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p113">The Excel division operator returns the **#DIV/0!** error when the denominator evaluates to zero or a number is too small to be represented as non-zero by Excel. Some functions that by definition involve a division can also return this error. For example, **AVERAGE** returns this error if none of the inputs can be converted to numbers.</span></span> 
  
<span data-ttu-id="45c5b-176">0 �ɂ�鏜�Z�����o���ꂽ���Ƃ�����ꍇ�ɂ̂݁A�A�h�C���֐����炱�̃G���[���Ԃ����悤�ɂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="45c5b-176">You should only consider returning this error from your add-in function to indicate that a division by zero was detected.</span></span>
  
### <a name="value"></a><span data-ttu-id="45c5b-177">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="45c5b-177">#VALUE!</span></span>

<span data-ttu-id="45c5b-p114">**#VALUE!** �G���[�́A�֐��܂��͉��Z�q�̈������K�v�Ȍ^�ɕϊ��ł��Ȃ��ꍇ�ɕԂ���܂��B�ϊ��ł��Ȃ��֐��̈��� (��F  `=LN("X")`) �̏ꍇ �A�֐��R�[�h�͌Ăяo����܂���B����́A�Ǝ��̃A�h�C���֐��̍쐬��f�o�b�O��s���ۂɏd�v�ȃ|�C���g�ł��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p114">Excel returns the **#VALUE!** error if a function or operator argument cannot be converted to the required type. In the case of function arguments that cannot be converted, for example  `=LN("X")`, Excel does not call the function code. This is an important point to remember when writing and debugging your own add-in functions.</span></span> 
  
<span data-ttu-id="45c5b-p115">�������̊֐��ł́A�֐��R�[�h��ň�����ϊ��ł��Ȃ��ꍇ�ɂ��̃G���[���Ԃ���܂��B���Ƃ��΁A `DATEVALUE("30-Feb-2007")` �͐������^�̈����ł���ɂ������炸�A���̃G���[�𔺂��Ď��s���܂��B���̏ꍇ�A���̊֐��ɂ���Ċ֐��R�[�h�����G���[���Ԃ���܂��B�l�̌^��͈͂����e�͈͂ł����Ă�A�֐��ɂ���Ă͂��̃G���[���Ԃ���܂��B���Ƃ��΁A  `FIND("a","xyz")` �͂��̃G���[��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p115">Some functions return this error if an argument cannot be converted within the function code. For example,  `DATEVALUE("30-Feb-2007")` fails with this error despite the argument being of the right type. In this case, it is the function that is returning the error from within its code. Some functions return this error even though the value types and ranges are allowable, for example  `FIND("a","xyz")` returns this error.</span></span> 
  
<span data-ttu-id="45c5b-p116">������������^�ł��邱�Ƃ�A�������^�ɕϊ��ł��Ȃ��������ƁA�͈͊O�ł��邱�Ƃ�������߂ɁA�A�h�C���֐�����G���[��Ԃ��悤�ɂ��Ă��������B�������A���l�̈������͈͊O�̏ꍇ�� **#NUM!** ��Ԃ��悤�������Ă��������B�͈͂�z������̃T�C�Y��\`���قȂ�ꍇ�ɂ�A���̃G���[��Ԃ��悤�������Ă��������B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p116">You should consider returning this error from your add-in function to indicate that the arguments are of the wrong type, could not be converted to the right type, or are out of range, although you should consider returning **#NUM!** for numerical arguments out of range. You should also consider returning this error when range or array arguments are the wrong shape or size.</span></span> 
  
### <a name="ref"></a><span data-ttu-id="45c5b-189">#REF!</span><span class="sxs-lookup"><span data-stu-id="45c5b-189">#REF!</span></span>

<span data-ttu-id="45c5b-p117">���ʓI�ɑ��ΎQ�Ƃ͈̔͊O�̏ꏊ�ɃR�s�[�����ƁA����� **#REF!** �G���[����������܂��B���Ƃ��΁AB2 �Z���ɐ���  `=A1` �������Ă���ꍇ�AB1 �Z���ɂ��̐�����R�s�[����ƁA���ʂ͐��� **=#REF!** �ɂȂ�܂��B���̃G���[�́A�؂���/�\��t������ŏ㏑�����ꂽ�Q�Ƃ�A���s�A���[�N�V�[�g���ƍ폜���ꂽ�Q�Ƃ������Ɋ܂܂��ꍇ�ɂ��������܂��B  `OFFSET(A1,-1,-1)` �ȂǁA�Q�Ƃ�Ԃ��������̊֐��͂��̃G���[��Ԃ��\��������܂��B���[�N�V�[�g���̒�\`�ɁA�����ƂȂ�Q�Ƃ��܂܂�Ă���ꍇ�́A���̃G���[�ɕ]������܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p117">Excel generates the **#REF!** error within an expression when it is copied to a location where the resulting relative reference goes out of bounds. For example, if the cell B2 contains the formula  `=A1`, copying this to cell B1 results in a formula **=#REF!**. This error is also generated in formulas that contain a reference that is overwritten in a cut-and-paste operation or is deleted in a row, column, or worksheet deletion. Some functions that can return references can return this error, for example,  `OFFSET(A1,-1,-1)`. Worksheet names whose definitions contain references that become invalid are evaluated to this error.</span></span>
  
<span data-ttu-id="45c5b-p118">�A�h�C���֐����Q�ƈ��������Ă��āA�Q�Ƃ������ł��邩�A�܂��͎Q�ƃG���[��ʂ����ꍇ�́A���̃G���[��Ԃ��悤�������Ă��������B[Excel �̃������Ǘ�](memory-management-in-excel.md)�� XLOPER/XLOPER12 �Z�N�V�����ł́A�Q�ƈ�����󂯎��A�Ԃ����Ƃ��ł���֐���쐬������@�ɂ��Đ�����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p118">If your add-in function takes reference arguments, you should consider returning this error if the references are invalid, or if you are passed a reference error. The section on XLOPER/XLOPER12s in [Memory Management in Excel](memory-management-in-excel.md) describes how to create functions that can accept and return reference arguments.</span></span> 
  
### <a name="name"></a><span data-ttu-id="45c5b-198">#NAME?</span><span class="sxs-lookup"><span data-stu-id="45c5b-198">#NAME?</span></span>

<span data-ttu-id="45c5b-199">Excel が生成されます、 **#NAME?** 式には、関数として認識されませんまたは名前を定義するトークンが含まれているとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="45c5b-199">Excel generates the **#NAME?** error when an expression contains a token that is not recognized as a function or defined name.</span></span> <span data-ttu-id="45c5b-200">アドインの関数が定義された名前にアクセスしようし、してが定義されていない、このエラーを返すことを検討してください。</span><span class="sxs-lookup"><span data-stu-id="45c5b-200">If your add-in function tries to access a defined name and it is not defined, you should consider returning this error.</span></span> 
  
### <a name="num"></a><span data-ttu-id="45c5b-201">#NUM!</span><span class="sxs-lookup"><span data-stu-id="45c5b-201">#NUM!</span></span>

<span data-ttu-id="45c5b-p120">**** �ȂǁA���l���͂����e�͈͊O�̏ꍇ�AExcel �̑g�ݍ��ݐ��l�֐��Ɛ��w�I�֐��̑����� `LN(0)` �G���[��Ԃ��܂��B���l���͂������܂��͔͈͊O�ł��邱�Ƃ�������߁A�A�h�C���֐����炱�̃G���[��Ԃ��悤�������Ă��������B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p120">Many of the built-in numerical and mathematical functions in Excel return the **#NUM!** error when a numerical input is out of the permitted range, for example,  `LN(0)`. You should consider returning this error from your add-in function to indicate that a numerical input was invalid or out of range.</span></span>
  
### <a name="na"></a><span data-ttu-id="45c5b-205">#N/A</span><span class="sxs-lookup"><span data-stu-id="45c5b-205">#N/A</span></span>

<span data-ttu-id="45c5b-p121">�����̏ꍇ **#N/A** �G���[�́A����Ȍ��ʂ܂��͗L���Ȍ��ʂ����p�ł��Ȃ����Ƃ�\���܂��B���Ƃ��΁A���S��v��������Ȃ������ꍇ�ɂ́A�� 3 ������ 0 �� MATCH �֐���肱�̃G���[���Ԃ���܂��B�܂��A���̃G���[�́A�֐� **NA** ��g�p���A�֐� **ISNA** �ŌʂɌ��o���āA�������邱�Ƃ�ł��܂��B���̂��߁A���̃G���[�́A�A�v���P�[�V�����ŗL�̏���͈͂�������߂Ƀ��[�N�V�[�g�ň�ʓI�Ɏg�p����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="45c5b-p121">The **#N/A** error is often returned to signify a successful or meaningful result is not available. For example, MATCH with the third argument zero returns this error if an exact match cannot be found. This error can also be generated using the function **NA** and specifically detected with the function **ISNA**. It is therefore a commonly used error in worksheets to indicate a range of application-specific conditions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45c5b-210">�֘A����</span><span class="sxs-lookup"><span data-stu-id="45c5b-210">See also</span></span>



[<span data-ttu-id="45c5b-211">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="45c5b-211">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="45c5b-212">Excel �ł� C API ��g�p�����v���O���~���O</span><span class="sxs-lookup"><span data-stu-id="45c5b-212">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
<span data-ttu-id="45c5b-213">[���O�Ƒ��̃��[�N�V�[�g�̎���]������](evaluating-names-and-other-worksheet-formula-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="45c5b-213">[Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md)</span></span>
  
[<span data-ttu-id="45c5b-214">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="45c5b-214">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

