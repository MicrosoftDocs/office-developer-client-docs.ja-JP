---
title: Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- known issues [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9cdbb10ea68723bd7e1cd9289e8592a7cc087c46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798887"
---
# <a name="known-issues-in-excel-xll-development"></a><span data-ttu-id="03a0c-104">Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��</span><span class="sxs-lookup"><span data-stu-id="03a0c-104">Known Issues in Excel XLL Development</span></span>

 <span data-ttu-id="03a0c-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03a0c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="03a0c-106">���̃g�s�b�N�ł́AMicrosoft Excel �ł� XLL �J���ő�������\���̂�����m�̖��ɂ��Đ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="03a0c-106">This topic describes known issues in Microsoft Excel that you might encounter in XLL development.</span></span>
  
## <a name="unregistering-xll-commands-and-functions"></a><span data-ttu-id="03a0c-107">XLL �̃R�}���h����ъ֐���o�^�������</span><span class="sxs-lookup"><span data-stu-id="03a0c-107">Unregistering XLL Commands and Functions</span></span>

<span data-ttu-id="03a0c-108">登録すると、XLL 関数やコマンド、Excel は、リソースの新しい名前を作成し、その名前を持つ DLL 関数への参照を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-108">When an XLL registers a function or command, Excel creates a new name for the resource and associates a reference to the DLL function with that name.</span></span> <span data-ttu-id="03a0c-109">名前は、4 番目の引数では、 *pxFunctionText* 、 [xlfRegister](xlfregister-form-1.md)関数から取得されます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-109">The name is taken from the fourth argument,  *pxFunctionText*  , of the [xlfRegister](xlfregister-form-1.md) function.</span></span> <span data-ttu-id="03a0c-110">この名前がワークシート名を管理するための標準のダイアログ ボックスから非表示にします。</span><span class="sxs-lookup"><span data-stu-id="03a0c-110">This name is hidden from the normal dialog boxes for managing worksheet names.</span></span> <span data-ttu-id="03a0c-111">関数やコマンドの登録を解除するには、 [xlfSetName](xlfsetname.md)関数を使用して、名前を渡すことが、定義が渡されていない名前を削除してください。</span><span class="sxs-lookup"><span data-stu-id="03a0c-111">To unregister a function or command, you must delete the name by using the [xlfSetName](xlfsetname.md) function, passing the name but not passing a definition.</span></span> <span data-ttu-id="03a0c-112">ただし、バグによりこの関数ウィザードの一覧から名前を削除します。</span><span class="sxs-lookup"><span data-stu-id="03a0c-112">However, a bug prevents this from removing the name from the Function Wizard lists.</span></span> 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a><span data-ttu-id="03a0c-113">�֐��E�B�U�[�h�ɂ���������̐��������̐؂�̂�</span><span class="sxs-lookup"><span data-stu-id="03a0c-113">Argument Description String Truncation in the Function Wizard</span></span>

<span data-ttu-id="03a0c-114">*PxArgumentHelp1*パラメーターと**xlfRegister**関数の後続のすべてのパラメーターは、XLL 関数の引数に対応するオプションの文字列です。</span><span class="sxs-lookup"><span data-stu-id="03a0c-114">The  *pxArgumentHelp1*  parameter and all subsequent parameters of the **xlfRegister** function are optional strings that correspond to the arguments of the XLL function.</span></span> <span data-ttu-id="03a0c-115">関数ウィザードには、これらの引数の作成] ダイアログ ボックスでヘルプを提供するが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-115">The Function Wizard displays these to provide help in the argument construction dialog box.</span></span> <span data-ttu-id="03a0c-116">Excel では、ダイアログ ボックスで表示する場合の 1 つまたは 2 つの文字で最後の引数に対応する文字列が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-116">Sometimes Excel truncates the string that corresponds to the final argument by one or two characters when displaying it in the dialog box.</span></span> <span data-ttu-id="03a0c-117">最終的な文字列の末尾に 1 つまたは 2 つのスペースを追加することによってこれを回避できます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-117">You can avoid this by adding one or two spaces to the end of the final string.</span></span> 
  
## <a name="binary-name-scope-limitation"></a><span data-ttu-id="03a0c-118">�o�C�i�����̃X�R�[�v����</span><span class="sxs-lookup"><span data-stu-id="03a0c-118">Binary Name Scope Limitation</span></span>

<span data-ttu-id="03a0c-p103">バイナリ名とそのデータは、作成された時点でアクティブだったワークシートが再度アクティブになったときにのみ取得できます。ワークシート関数では、ワークブック内のワークシートをアクティブにすることはできないため (コマンドでのみ可能)、バイナリ名の適用は非常に制限されています。特定のワークシートからのみ呼び出されるコマンドがあれば、バイナリ名を使用してコマンドに関するデータを格納することもできます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-p103">Binary names and their data can be retrieved only when the worksheet that was active at the time they were created is again active. Because worksheet functions cannot activate worksheets within a workbook (only commands can do this), applications of binary names are very limited. If you have a command that is only invoked from a particular worksheet, for example, you could use a binary name to store command-related data.</span></span>
  
## <a name="xlset-and-workbooks-with-array-formulas"></a><span data-ttu-id="03a0c-122">xlSet �Ɣz�񐔎���܂ރ��[�N�u�b�N</span><span class="sxs-lookup"><span data-stu-id="03a0c-122">xlSet and Workbooks with Array Formulas</span></span>

<span data-ttu-id="03a0c-123">Excel 2003 およびそれ以前のバージョンでは、 [xlSet 関数](xlset.md)ではない、アクティブなワークシート、作業中のワークシートと同じ範囲が配列数式を含むワークシート上の範囲に値を代入しようとする場合を失敗します。</span><span class="sxs-lookup"><span data-stu-id="03a0c-123">In Excel 2003 and earlier versions, the [xlSet function](xlset.md) fails if you try to assign values to a range on a worksheet that is not the active worksheet, where the equivalent range on the active sheet contains an array formula.</span></span> <span data-ttu-id="03a0c-124">この例では、「配列の一部を変更することはできません」メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03a0c-124">In this case, Excel displays the message "You cannot change part of an array."</span></span> <span data-ttu-id="03a0c-125">これは、Excel 2007 で修正されました。</span><span class="sxs-lookup"><span data-stu-id="03a0c-125">This was fixed in Excel 2007.</span></span> 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a><span data-ttu-id="03a0c-126">�f�[�^ �e�[�u���ŏz�Q�Ƃ��\\</span><span class="sxs-lookup"><span data-stu-id="03a0c-126">Circular References are Tolerated in Data Tables</span></span>

<span data-ttu-id="03a0c-p105">Excel �ł͌��݁A�f�[�^ �e�[�u���̃x�[�X�ƂȂ�v�Z�ɂ����āA���e�[�u����̒l��Q�Ƃ��Ă���ꍇ�ł�G���[�ɂȂ�܂���B���̂悤�ȃV�i���I�͂܂�Ȃ��Ƃł����A�f�[�^ �e�[�u���̒l��v�Z���鐔���̍쐬��ύX�ɂ͒��ӂ��K�v�ł��B</span><span class="sxs-lookup"><span data-stu-id="03a0c-p105">Excel currently does not raise an error if the calculation that a data table is based on refers to something in the table itself. As unlikely as this scenario might be, you should be careful when you are creating or modifying formulas that are used to calculate data table values.</span></span>
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a><span data-ttu-id="03a0c-129">���� XLOPER12 �� XLOPER �ɕϊ�����</span><span class="sxs-lookup"><span data-stu-id="03a0c-129">Converting an Integer XLOPER12 to an XLOPER</span></span>

<span data-ttu-id="03a0c-p106">�����^ **xltypeInt** �́A **XLOPER12** �f�[�^�^�ł� 32 �r�b�g�̕����t�������ł����A **XLOPER** �f�[�^�^�ł� 16 �r�b�g�����t�������ł��邽�߁A���� **XLOPER12** �̒l�̒��ɂ́A���� **XLOPER** �Ɋ܂߂��Ȃ���̂����蓾�܂��BExcel ����ł��̃f�[�^�^��ϊ�����ꍇ�́A�f�[�^�^�𕂓������_ **xltypeNum** **XLOPER** �ɕϊ����Ă��̖�������܂��B</span><span class="sxs-lookup"><span data-stu-id="03a0c-p106">Because the integer type **xltypeInt** is a 32-bit signed integer in the **XLOPER12** data type, but it is only a 16-bit signed integer in the **XLOPER** data type, it is possible that some integer **XLOPER12** values cannot be contained in an integer **XLOPER**. Where Excel converts this type internally, it gets around this problem by converting the type to a floating-point **xltypeNum** **XLOPER**.</span></span>
  
<span data-ttu-id="03a0c-p107">�t���[�����[�N�֐� [XLOper12ToXLOper](xloper12toxloper.md) �́A���̓���𔽉f���āAExcel ����̓���ƈ�v����悤�ɂ��܂��B���̊֐���Ăяo���ہA�Ԃ� **XLOPER** ����� **xltypeInt** �ł���Ƒz�肵�Ȃ��ł��������B **my_xloper** �^�� **xltypeNum** �̏ꍇ�� **my_xloper.val.w** ��ǂݏo���ƁAfalse �̒l���Ԃ�܂��B</span><span class="sxs-lookup"><span data-stu-id="03a0c-p107">The Framework [XLOper12ToXLOper](xloper12toxloper.md) function mirrors this behavior to be consistent with Excel internally. When you call this function, you should not assume that the returned **XLOPER** will always be **xltypeInt**; reading **my_xloper.val.w** gives a false value if the **my_xloper** type is **xltypeNum**.</span></span>
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a><span data-ttu-id="03a0c-134">������C���v���[�X�ŕύX���� XLOPER �܂��� XLOPER12 ��Ԃ�</span><span class="sxs-lookup"><span data-stu-id="03a0c-134">Returning XLOPER or XLOPER12 by Modifying Arguments in Place</span></span>

<span data-ttu-id="03a0c-p108">Excel �ł͈�����C���v���[�X�ŕύX���āA **XLOPER** �܂��� **XLOPER12** ��Ԃ��悤�Ɋ֐���o�^���邱�Ƃ��ł��܂��B�������A **XLOPER**/ **XLOPER12** ��������������|�C���g���Ă���A���̃|�C���^�� DLL �֐��̖߂�l�ŏ㏑�������ƁAExcel �̓����� ���[�N�ɂȂ��鋰�ꂪ����܂��BExcel �ŃG���[�͕\������܂��񂪁A���ʓI�ɃN���b�V�����鋰�ꂪ����܂��B�܂��ADLL �Ŗ߂�l�p�̃����������蓖�Ă��Ă���ꍇ�AExcel �͂��̃������������悤�Ƃ��邽�߁A�����ɃA�v���P�[�V�������N���b�V�����鋰�ꂪ����܂��B���̂��߁A **XLOPER**/ **XLOPER12** �����̓C���v���[�X�ŕύX���Ȃ��ł��������B **XLOPER** ������ **XLOPER12** �����͂��ׂāA�K���ǂݎ���p�Ƃ��Ĉ����Ă��������B</span><span class="sxs-lookup"><span data-stu-id="03a0c-p108">Excel permits the registration of functions that return an **XLOPER** or **XLOPER12** by modifying an argument in place. However, if an **XLOPER**/ **XLOPER12** argument points to memory, and the pointer is then overwritten by the return value of the DLL function, Excel can leak memory. Excel does not display an error, but it might eventually crash. Also, if the DLL allocated memory for the return value, Excel might try to free that memory, which could cause an immediate application crash. Therefore, you should not modify **XLOPER**/ **XLOPER12** arguments in place. All **XLOPER** or **XLOPER12** arguments should be treated as strictly read-only.</span></span> 
  
<span data-ttu-id="03a0c-141">�ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="03a0c-141">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03a0c-142">�֘A����</span><span class="sxs-lookup"><span data-stu-id="03a0c-142">See also</span></span>



[<span data-ttu-id="03a0c-143">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="03a0c-143">XLOper12ToXLOper</span></span>](xloper12toxloper.md)


[<span data-ttu-id="03a0c-144">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="03a0c-144">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="03a0c-145">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="03a0c-145">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
  
[<span data-ttu-id="03a0c-146">Excel �̃������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="03a0c-146">Memory Management in Excel</span></span>](memory-management-in-excel.md)

