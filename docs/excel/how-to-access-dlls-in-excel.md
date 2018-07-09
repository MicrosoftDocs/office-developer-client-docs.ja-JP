---
title: Excel での Dll のアクセス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- accessing dlls [excel 2007],DLLs [Excel 2007], accessing in Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798884"
---
# <a name="access-dlls-in-excel"></a><span data-ttu-id="3df93-104">Excel での Dll のアクセス</span><span class="sxs-lookup"><span data-stu-id="3df93-104">Access DLLs in Excel</span></span>

<span data-ttu-id="3df93-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3df93-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3df93-106">Microsoft Excel �� DLL �֐���R�}���h�ɂ́A���܂��܂ȕ��@�ŃA�N�Z�X�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-106">You can access a DLL function or command in Microsoft Excel in several ways:</span></span>
  
- <span data-ttu-id="3df93-107">**Declare** �X�e�[�g�����g��g�p���āA�֐��܂��̓R�}���h���g�p�\�ł���悤�ɂȂ��Ă��� Microsoft Visual Basic for Applications (VBA) �R�[�h ���W���[����ʂ��ăA�N�Z�X����B</span><span class="sxs-lookup"><span data-stu-id="3df93-107">Through a Microsoft Visual Basic for Applications (VBA) code module in which the function or command has been made available using a **Declare** statement.</span></span> 
    
- <span data-ttu-id="3df93-108">**CALL** �֐��܂��� **REGISTER** �֐���g�p���āAXLM �}�N�� �V�[�g��ʂ��ăA�N�Z�X����B</span><span class="sxs-lookup"><span data-stu-id="3df93-108">Through an XLM macro sheet by using the **CALL** or **REGISTER** functions.</span></span> 
    
- <span data-ttu-id="3df93-109">���ڃ��[�N�V�[�g����A�܂��̓��[�U�[ �C���^�[�t�F�C�X (UI) �̃J�X�^�}�C�Y���ꂽ���ڂ���A�N�Z�X����B</span><span class="sxs-lookup"><span data-stu-id="3df93-109">Directly from the worksheet or from a customized item in the user interface (UI).</span></span>
    
<span data-ttu-id="3df93-p101">���̃h�L�������g�ł́AXLM �֐��ɂ��Ă͐�����܂���B����ȊO�� 2 �̕��@�̂����A�ǂ��炩��g�p���邱�Ƃ�����߂��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p101">This documentation does not cover XLM functions. It is recommended that you use either of the other two approaches.</span></span>
  
<span data-ttu-id="3df93-p102">���ڃ��[�N�V�[�g����A�܂��� UI �̃J�X�^�}�C�Y���ꂽ���ڂ���A�N�Z�X����ɂ́A�ŏ��Ɋ֐��܂��̓R�}���h�� Excel �ɓo�^����K�v������܂��B�R�}���h�܂��͊֐��̓o�^�̏ڍׂɂ��ẮA�u[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3df93-p102">To be accessed directly from the worksheet or from a customized item in the UI, the function or command must first be registered with Excel. For information about registering commands and functions, see [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).</span></span>
  
## <a name="calling-dll-functions-and-commands-from-vba"></a><span data-ttu-id="3df93-114">DLL の関数やコマンドを VBA から呼び出す</span><span class="sxs-lookup"><span data-stu-id="3df93-114">Calling DLL functions and commands from VBA</span></span>

<span data-ttu-id="3df93-p103">**Declare** �X�e�[�g�����g��g�p����ƁAVBA �� DLL �֐���R�}���h�ɃA�N�Z�X�ł��܂��B���̃X�e�[�g�����g�ɂ́A�R�}���h�p�̍\���Ɗ֐��p�̍\���� 1 ������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p103">You can access DLL functions and commands in VBA by using the **Declare** statement. This statement has one syntax for commands and one for functions.</span></span> 
  
- <span data-ttu-id="3df93-117">**�\�� 1 ? �R�}���h**</span><span class="sxs-lookup"><span data-stu-id="3df93-117">**Syntax 1 - commands**</span></span>
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- <span data-ttu-id="3df93-118">**�\�� 2 ? �֐�**</span><span class="sxs-lookup"><span data-stu-id="3df93-118">**Syntax 2 - functions**</span></span>
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

<span data-ttu-id="3df93-p104">�ȗ��\�� **Public** �L�[���[�h�� **Private** �L�[���[�h�ł́A�C���|�[�g�����֐��̃X�R�[�v��w�肵�܂� (���ꂼ��AVisual Basic �v���W�F�N�S�́A�܂��� Visual Basic ���W���[���̂�)�Bname �� VBA �R�[�h�Ŏg�p���閼�O�ɂȂ�܂��B���̖��O�� DLL �̖��O�ƈقȂ�ꍇ�́A�ʖ��ualiasname�v�w��q��g�p����K�v������܂��B�܂��A�֐��ɂ́ADLL �ɂ���ăG�N�X�|�[�g����閼�O��t����K�v������܂��BDLL �����ԍ��ւ̎Q�Ƃ� DLL �֐��ɃA�N�Z�X����ꍇ�́A�ʖ� (�擪�� **#** ��t����������) ��w�肷��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p104">The optional **Public** and **Private** keywords specify the scope of the imported function: the entire Visual Basic project or just the Visual Basic module, respectively. The name is the name that you want to use in the VBA code. If this differs from the name in the DLL, you must use the Alias "aliasname" specifier, and you should give the name of the function as exported by the DLL. If you want to access a DLL function by reference to a DLL ordinal number, you must provide an alias name, which is the ordinal prefixed by **#**.</span></span>
  
<span data-ttu-id="3df93-p105">�R�}���h�� **void** ��Ԃ��K�v������܂��B�֐��́AVBA �� **ByVal** ��F���ł���^��Ԃ��K�v������܂��B�܂�A�������̌^ (������A�z��A���[�U�[��\`�^�A����уI�u�W�F�N�g) �͈�����C���v���[�X�ŕύX���邱�ƂŁA���ȒP�ɕԂ����Ƃ������Ƃł��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p105">Commands should return **void**. Functions should return types that VBA can recognize **ByVal**. This means that some types are more easily returned by modifying arguments in place: strings, arrays, user-defined types, and objects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3df93-p106">VBA �ł́AVisual Basic ���W���[���Ŏ����ꂽ�������X�g�Ɩ߂�l�� DLL �ŃR�[�h�����ꂽ��̂Ɠ����ł��邱�Ƃ�m�F�ł��܂���B����͎����ŐT�d�Ɋm�F����K�v������܂��B�ԈႢ������� Excel ���N���b�V������\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p106">VBA cannot check that the argument list and return stated in the Visual Basic module are the same as coded in the DLL. You should check this yourself very carefully, because a mistake could cause Excel to crash.</span></span> 
  
<span data-ttu-id="3df93-p107">�֐��܂��̓R�}���h�̈������Q�Ƃ܂��̓|�C���^�[�œn����Ȃ��ꍇ�́A **arglist** �錾�ň����̑O�� **ByVal** �L�[���[�h��t����K�v������܂��BC/C++ �֐����|�C���^�[�̈�����󂯎��ꍇ��AC++ �֐����Q�Ƃ̈�����󂯎��ꍇ�́A **ByRef** �n���ɂ���K�v������܂��B **ByRef** �L�[���[�h�́AVBA �ł͊���ł��邽�߈������X�g�ŏȗ����邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p107">When the function or command's arguments are not passed by reference or pointer, they must be preceded by the **ByVal** keyword in the **arglist** declaration. When a C/C++ function takes pointer arguments, or a C++ function takes reference arguments, they should be passed **ByRef**. The keyword **ByRef** can be omitted from argument lists because it is the default in VBA.</span></span> 
  
### <a name="argument-types-in-cc-and-vba"></a><span data-ttu-id="3df93-131">C および C++ と VBA の引数の型</span><span class="sxs-lookup"><span data-stu-id="3df93-131">Argument types in C/C++ and VBA</span></span>

<span data-ttu-id="3df93-132">C/C++ �� VBA �̈����̌^�̐錾���r����Ƃ��ɂ́A���̓_�ɒ��ӂ��K�v�ł��B</span><span class="sxs-lookup"><span data-stu-id="3df93-132">You should note the following when you compare the declarations of argument types in C/C++ and VBA.</span></span>
  
- <span data-ttu-id="3df93-133">VBA �� **String** �́AByVal �n���̏ꍇ�̓o�C�g������ BSTR �\���̂ւ̃|�C���^�[�Ƃ��ēn����܂��B **ByRef** �n���̏ꍇ�̓|�C���^�[�ւ̃|�C���^�[�Ƃ��ēn����܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-133">A VBA **String** is passed as a pointer to a byte-string BSTR structure when passed ByVal, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="3df93-134">�������i�[���Ă��� VBA �� **Variant** �́A **ByVal** �n���̏ꍇ�� Unicode ���C�h���������� BSTR �\���̂ւ̃|�C���^�[�Ƃ��ēn����܂��B **ByRef** �n���̏ꍇ�̓|�C���^�[�ւ̃|�C���^�[�Ƃ��ēn����܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-134">A VBA **Variant** that contains a string is passed as a pointer to a Unicode wide-character string BSTR structure when passed **ByVal**, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="3df93-135">VBA �� **Integer** �́AC/C++ �� signed short �Ɠ����� 16 �r�b�g�^�ł��B</span><span class="sxs-lookup"><span data-stu-id="3df93-135">The VBA **Integer** is a 16-bit type equivalent to a signed short in C/C++.</span></span> 
    
- <span data-ttu-id="3df93-136">VBA �� **Long** �́AC/C++ �� signed int �Ɠ����� 32 �r�b�g�^�ł��B</span><span class="sxs-lookup"><span data-stu-id="3df93-136">The VBA **Long** is a 32-bit type equivalent to a signed int in C/C++.</span></span> 
    
- <span data-ttu-id="3df93-137">VBA と C または C++ の両方**の種類**と**構造体**のステートメントをそれぞれ使用して、ユーザー定義データ型の定義を許可します。</span><span class="sxs-lookup"><span data-stu-id="3df93-137">Both VBA and C/C++ allow the definition of user-defined data types, using the **Type** and **struct** statements respectively.</span></span> 
    
- <span data-ttu-id="3df93-138">VBA �� C/C++ �́A�ǂ���� **Variant** �f�[�^�^��T�|�[�g���Ă��܂��BC/C++ �ɂ��ẮAWindows OLE/COM �w�b�_�[ �t�@�C����� VARIANT �Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-138">Both VBA and C/C++ support the **Variant** data type, defined for C/C++ in the Windows OLE/COM header files as VARIANT.</span></span> 
    
- <span data-ttu-id="3df93-139">VBA �̔z��� OLE �� **SafeArrays** �ł��BC/C++ �ɂ��ẮAWindows OLE/COM �w�b�_�[ �t�@�C����� **SAFEARRAY** �Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-139">VBA arrays are OLE **SafeArrays**, defined for C/C++ in the Windows OLE/COM header files as **SAFEARRAY**.</span></span>
    
- <span data-ttu-id="3df93-140">VBA �� **Currency** �f�[�^�^�́A **ByVal** �n���̏ꍇ�� Windows �w�b�_�[ �t�@�C�� wtypes.h ��Œ�\`����Ă��� **CY** �^�̍\���̂Ƃ��ēn����܂��B **ByRef** �n���̏ꍇ�� this �ւ̃|�C���^�[�Ƃ��ēn����܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-140">The VBA **Currency** data type is passed as a structure of type **CY**, defined in the Windows header file wtypes.h, when passed **ByVal**, and as a pointer to this when passed **ByRef**.</span></span>
    
<span data-ttu-id="3df93-141">VBA では、ユーザー定義データ型のデータ要素では、Visual Studio は、既定では、圧縮されている 8 バイト境界には、4 バイト境界にパックされます。</span><span class="sxs-lookup"><span data-stu-id="3df93-141">In VBA, data elements in user-defined data types are packed to 4-byte boundaries, whereas in Visual Studio, by default, they are packed to 8-byte boundaries.</span></span> <span data-ttu-id="3df93-142">C または C++ の構造体の定義を囲む必要がありますので、`#pragma pack(4) … #pragma pack()`がずれて要素を避けるためにブロックします。</span><span class="sxs-lookup"><span data-stu-id="3df93-142">Therefore you must enclose the C/C++ structure definition in a `#pragma pack(4) … #pragma pack()` block to avoid elements being misaligned.</span></span> 
  
<span data-ttu-id="3df93-143">���ɁA�����̃��[�U�[ �^�C�v��\`�̗������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-143">The following is an example of equivalent user type definitions.</span></span>
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

<span data-ttu-id="3df93-p109">VBA �́AExcel ���T�|�[�g�����������̒l�͈̔͂�T�|�[�g���邱�Ƃ�����܂��BVBA �� double �� IEEE �ɏ������Ă��āA�����_�̃��[�N�V�[�g�ł� 0 �ɐ؂�̂Ă��Ă���񐳋K������T�|�[�g���Ă��܂��BVBA �� **Date** �^�́A���̃V���A�������ꂽ���t��g�p���邱�Ƃ� 1-Jan-0100 (100 �N 1 �� 1 ��) ����O�̓��t��\���ł��܂��BExcel �ł́A�[���ȏ�̃V���A�������ꂽ���t�݂̂����e����܂��BVBA �� **Currency** �^ (64 �r�b�g�����ɃX�P�[�����O����܂�) �́A8 �o�C�g�� double �ł̓T�|�[�g����Ȃ����x������ł��邽�߃��[�N�V�[�g�ł͈�v���܂���B</span><span class="sxs-lookup"><span data-stu-id="3df93-p109">VBA supports a greater range of values in some cases than Excel supports. The VBA double is IEEE compliant, supporting subnormal numbers that are currently rounded down to zero on the worksheet. The VBA **Date** type can represent dates as early as 1-Jan-0100 using negative serialized dates. Excel only allows serialized dates greater than or equal to zero. The VBA **Currency** type—a scaled 64-bit integer—can achieve accuracy not supported in 8-byte doubles, and so is not matched in the worksheet.</span></span> 
  
<span data-ttu-id="3df93-149">Excel �́AVBA ���[�U�[��\`�֐��ɁA���Ɏ����^�̃o���A���g�݂̂�n���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-149">Excel only passes Variants of the following types to a VBA user-defined function.</span></span>
  
|<span data-ttu-id="3df93-150">**VBA �f�[�^�^**</span><span class="sxs-lookup"><span data-stu-id="3df93-150">**VBA data type**</span></span>|<span data-ttu-id="3df93-151">**C/C++ �o���A���g�^�̃r�b�g �t���O**</span><span class="sxs-lookup"><span data-stu-id="3df93-151">**C/C++ Variant type bit flags**</span></span>|<span data-ttu-id="3df93-152">**���**</span><span class="sxs-lookup"><span data-stu-id="3df93-152">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3df93-153">Double</span><span class="sxs-lookup"><span data-stu-id="3df93-153">Double</span></span>  <br/> |<span data-ttu-id="3df93-154">**VT_R8**</span><span class="sxs-lookup"><span data-stu-id="3df93-154">**VT_R8**</span></span> <br/> ||
|<span data-ttu-id="3df93-155">Boolean</span><span class="sxs-lookup"><span data-stu-id="3df93-155">Boolean</span></span>  <br/> |<span data-ttu-id="3df93-156">**VT_BOOL**</span><span class="sxs-lookup"><span data-stu-id="3df93-156">**VT_BOOL**</span></span> <br/> ||
|<span data-ttu-id="3df93-157">Date</span><span class="sxs-lookup"><span data-stu-id="3df93-157">Date</span></span>  <br/> |<span data-ttu-id="3df93-158">**VT_DATE**</span><span class="sxs-lookup"><span data-stu-id="3df93-158">**VT_DATE**</span></span> <br/> ||
|<span data-ttu-id="3df93-159">String</span><span class="sxs-lookup"><span data-stu-id="3df93-159">String</span></span>  <br/> |<span data-ttu-id="3df93-160">**VT_BSTR**</span><span class="sxs-lookup"><span data-stu-id="3df93-160">**VT_BSTR**</span></span> <br/> |<span data-ttu-id="3df93-161">OLE Bstr �o�C�g������</span><span class="sxs-lookup"><span data-stu-id="3df93-161">OLE Bstr byte string</span></span>  <br/> |
|<span data-ttu-id="3df93-162">Range</span><span class="sxs-lookup"><span data-stu-id="3df93-162">Range</span></span>  <br/> |<span data-ttu-id="3df93-163">**VT_DISPATCH**</span><span class="sxs-lookup"><span data-stu-id="3df93-163">**VT_DISPATCH**</span></span> <br/> |<span data-ttu-id="3df93-164">�͈͂ƃZ���̎Q��</span><span class="sxs-lookup"><span data-stu-id="3df93-164">Range and cell references</span></span>  <br/> |
|<span data-ttu-id="3df93-165">�z���܂ރo���A���g�^</span><span class="sxs-lookup"><span data-stu-id="3df93-165">Variant containing an array</span></span>  <br/> |<span data-ttu-id="3df93-166">**VT_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="3df93-166">**VT_ARRAY**</span></span> | <span data-ttu-id="3df93-167">**VT_VARIANT**</span><span class="sxs-lookup"><span data-stu-id="3df93-167">**VT_VARIANT**</span></span> <br/> |<span data-ttu-id="3df93-168">���e�����z��</span><span class="sxs-lookup"><span data-stu-id="3df93-168">Literal arrays</span></span>  <br/> |
|<span data-ttu-id="3df93-169">Ccy</span><span class="sxs-lookup"><span data-stu-id="3df93-169">Ccy</span></span>  <br/> |<span data-ttu-id="3df93-170">**VT_CY**</span><span class="sxs-lookup"><span data-stu-id="3df93-170">**VT_CY**</span></span> <br/> |<span data-ttu-id="3df93-171">64 �r�b�g������g�����āA�����_�ȉ� 4 ���Ɏl�̌ܓ��������x������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-171">64-bit integer scaled to permit 4 decimal places of accuracy.</span></span>  <br/> |
|<span data-ttu-id="3df93-172">�G���[��܂ރo���A���g�^</span><span class="sxs-lookup"><span data-stu-id="3df93-172">Variant containing an error</span></span>  <br/> |<span data-ttu-id="3df93-173">**VT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="3df93-173">**VT_ERROR**</span></span> <br/> ||
||<span data-ttu-id="3df93-174">**制約**</span><span class="sxs-lookup"><span data-stu-id="3df93-174">**VT_EMPTY**</span></span> <br/> |<span data-ttu-id="3df93-175">��̃Z���܂��͏ȗ����ꂽ����</span><span class="sxs-lookup"><span data-stu-id="3df93-175">Empty cells or omitted arguments</span></span>  <br/> |
   
<span data-ttu-id="3df93-p110">**VarType** ��g�p���āA�n���ꂽ VBA �o���A���g�^�̎�ނ�m�F�ł��܂��B�������A�Q�Ƃ�g�p���ČĂяo���ꂽ�Ƃ��ɔ͈͂̒l�̌^��Ԃ��֐�������܂��B **Variant** �� **Range** �Q�ƃI�u�W�F�N�g���ǂ����𔻒f����ꍇ�́A **IsObject** �֐���g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p110">You can check the type of a passed-in Variant in VBA using the **VarType**, except that the function returns the type of the range's values when called with references. To determine if a **Variant** is a **Range** reference object, you can use the **IsObject** function.</span></span> 
  
<span data-ttu-id="3df93-p111">**Value** �v���p�e�B�� **Variant** �Ɋ��蓖�Ă邱�ƂŁA **Range** ���� VBA �o���A���g�^�̔z���܂� **Variants** ��쐬�ł��܂��B���̎��_�ŗL���ł������n��ݒ�̕W���ʉ݌\`����g�p���ď���������\�[�X�͈͂Ɋ܂܂��Z���́A **Currency** �^�̔z��v�f�ɕϊ�����܂��B���t�Ƃ��ď��������ꂽ�Z���́A **Date** �̔z��v�f�ɕϊ�����܂��B�������܂�ł���Z���́A���C�h���� **BSTR** �o���A���g�ɕϊ�����܂��B�G���[��܂�ł���Z���́A **VT_ERROR** �^�� **Variants** �ɕϊ�����܂��B **Boolean** **True** �܂��� **False** ��܂�ł���Z���́A **VT_BOOL** �^�� **Variants** �ɕϊ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p111">You can create **Variants** that contain arrays of variants in VBA from a **Range** by assigning its **Value** property to a **Variant**. Any cells in the source range that are formatted using the standard currency format for the regional settings in force at the time are converted to array elements of type **Currency**. Any cells formatted as dates are converted to array elements of type **Date**. Cells containing strings are converted to wide-character **BSTR** Variants. Cells containing errors are converted to **Variants** of type **VT_ERROR**. Cells containing **Boolean** **True** or **False** are converted to **Variants** of type **VT_BOOL**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3df93-p112">**Variant** �� **True** �� ?1�A **False** �� 0 �Ƃ��Ċi�[���܂��B���t�܂��͒ʉ݋�z�Ƃ��ď���������Ă��Ȃ����l�́A **VT_R8** �^�̃o���A���g�ɕϊ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p112">The **Variant** stores **True** as -1 and **False** as 0. Numbers not formatted as dates or currency amounts are converted to Variants of type **VT_R8**.</span></span> 
  
### <a name="variant-and-string-arguments"></a><span data-ttu-id="3df93-186">バリアント型と文字列の引数</span><span class="sxs-lookup"><span data-stu-id="3df93-186">Variant and string arguments</span></span>

<span data-ttu-id="3df93-p113">Excel �́A����I�Ƀ��C�h���� Unicode ������œ��삵�Ă��܂��BVBA ���[�U�[��**** �֐��� **String** �����ł͂Ȃ� **Variant** ��󂯓����悤�ɂ���K�v������܂��B����ɂ��ADLL �֐��́A���� **Variant** BSTR ���C�h����������� VBA ����󂯓���ł���悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p113">Excel works internally with wide-character Unicode strings. When a VBA user-defined function is declared as taking a **String** argument, Excel converts the supplied string to a byte-string in a locale-specific way. If you want your function to be passed a Unicode string, your VBA user-defined function should accept a **Variant** instead of a **String** argument. Your DLL function can then accept that **Variant** BSTR wide-character string from VBA.</span></span> 
  
<span data-ttu-id="3df93-p114">DLL ���� VBA �� Unicode �������Ԃ��ꍇ�́A **Variant** �����������C���v���[�X�ŕύX����K�v������܂��B���ꂪ���삷��ɂ́AC/C++ �R�[�h��� DLL �֐��� **Variant** �ւ̃|�C���^�[��󂯎��悤�ɐ錾���āAVBA �R�[�h��ň�����  `ByRef varg As Variant` �Ƃ��Đ錾����K�v������܂��B�Â�������̃������͉������K�v������܂��B�܂��A�V����������l�� OLE Bstr ������֐��� DLL ��ɂ̂ݍ쐬����܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p114">To return Unicode strings to VBA from a DLL, you should modify a **Variant** string argument in place. For this to work, you must declare the DLL function as taking a pointer to the **Variant** and in your C/C++ code, and declare the argument in the VBA code as  `ByRef varg As Variant`. The old string memory should be released, and the new string value created by using the OLE Bstr string functions only in the DLL.</span></span>
  
<span data-ttu-id="3df93-p115">DLL ���� VBA �Ƀo�C�g�������Ԃ��ꍇ�́A�o�C�g������ BSTR ������C���v���[�X�ŕύX����K�v������܂��B���ꂪ���삷��ɂ́AC/C++ �R�[�h��� DLL �֐��� BSTR �ւ̃|�C���^�[�̃|�C���^�[��󂯎��悤�ɐ錾���āAVBA �R�[�h��ň����� ' **ByRef varg As String**' �Ƃ��Đ錾����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p115">To return a byte string to VBA from a DLL, you should modify a byte-string BSTR argument in place. For this to work, you must declare the DLL function as taking a pointer to a pointer to the BSTR and in your C/C++ code, and declare the argument in the VBA code as ' **ByRef varg As String**'.</span></span>
  
<span data-ttu-id="3df93-p116">���̂悤�ȕ��@�� VBA ����n���ꂽ������́A�������֘A�̖������邽�߂ɁAOLE BSTR ������֐���g�p���Ă̂ݏ�������K�v������܂��B���Ƃ��΁A�n���ꂽ�������㏑������O�� **SysFreeString** ��Ăяo���ă������������A **SysAllocStringByteLen** �܂��� **SysAllocStringLen** ��Ăяo���ĐV����������̗̈����蓖�Ă�K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p116">You should only handle strings that are passed in these ways from VBA using the OLE BSTR string functions to avoid memory-related problems. For example, you must call **SysFreeString** to free the memory before overwriting the passed in string, and **SysAllocStringByteLen** or **SysAllocStringLen** to allocate space for a new string.</span></span> 
  
<span data-ttu-id="3df93-p117">Excel ���[�N�V�[�g�̃G���[�́A���̕\�Ɏ���������w�肵�� **CVerr** �֐���g�p���邱�ƂŁAVBA �� **Variants** �Ƃ��č쐬�ł��܂��B�܂��A���[�N�V�[�g�̃G���[�́A **VT_ERROR** �^�� **Variants** ��g�p���āA���Ɏ����l�� **ulVal** �t�B�[���h�ɐݒ肷�邱�ƂŁADLL ���� VBA �ɕԂ����Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p117">You can create Excel worksheet errors as **Variants** in VBA by using the **CVerr** function with arguments as shown in the following table. Worksheet errors can also be returned to VBA from a DLL using **Variants** of type **VT_ERROR**, and with the following values in the **ulVal** field.</span></span> 
  
|<span data-ttu-id="3df93-200">**�G���[**</span><span class="sxs-lookup"><span data-stu-id="3df93-200">**Error**</span></span>|<span data-ttu-id="3df93-201">**�o���A���g�^�� ulVal �l**</span><span class="sxs-lookup"><span data-stu-id="3df93-201">**Variant ulVal value**</span></span>|<span data-ttu-id="3df93-202">**CVerr ����**</span><span class="sxs-lookup"><span data-stu-id="3df93-202">**CVerr argument**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3df93-203">#NULL!</span><span class="sxs-lookup"><span data-stu-id="3df93-203">#NULL!</span></span>  <br/> |<span data-ttu-id="3df93-204">2148141008</span><span class="sxs-lookup"><span data-stu-id="3df93-204">2148141008</span></span>  <br/> |<span data-ttu-id="3df93-205">2000</span><span class="sxs-lookup"><span data-stu-id="3df93-205">2000</span></span>  <br/> |
|<span data-ttu-id="3df93-206">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="3df93-206">#DIV/0!</span></span>  <br/> |<span data-ttu-id="3df93-207">2148141015</span><span class="sxs-lookup"><span data-stu-id="3df93-207">2148141015</span></span>  <br/> |<span data-ttu-id="3df93-208">2007</span><span class="sxs-lookup"><span data-stu-id="3df93-208">2007</span></span>  <br/> |
|<span data-ttu-id="3df93-209">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3df93-209">#VALUE!</span></span>  <br/> |<span data-ttu-id="3df93-210">2148141023</span><span class="sxs-lookup"><span data-stu-id="3df93-210">2148141023</span></span>  <br/> |<span data-ttu-id="3df93-211">2015</span><span class="sxs-lookup"><span data-stu-id="3df93-211">2015</span></span>  <br/> |
|<span data-ttu-id="3df93-212">#REF!</span><span class="sxs-lookup"><span data-stu-id="3df93-212">#REF!</span></span>  <br/> |<span data-ttu-id="3df93-213">2148141031</span><span class="sxs-lookup"><span data-stu-id="3df93-213">2148141031</span></span>  <br/> |<span data-ttu-id="3df93-214">2023</span><span class="sxs-lookup"><span data-stu-id="3df93-214">2023</span></span>  <br/> |
|<span data-ttu-id="3df93-215">#NAME?</span><span class="sxs-lookup"><span data-stu-id="3df93-215">#NAME?</span></span>  <br/> |<span data-ttu-id="3df93-216">2148141037</span><span class="sxs-lookup"><span data-stu-id="3df93-216">2148141037</span></span>  <br/> |<span data-ttu-id="3df93-217">2029</span><span class="sxs-lookup"><span data-stu-id="3df93-217">2029</span></span>  <br/> |
|<span data-ttu-id="3df93-218">#NUM!</span><span class="sxs-lookup"><span data-stu-id="3df93-218">#NUM!</span></span>  <br/> |<span data-ttu-id="3df93-219">2148141044</span><span class="sxs-lookup"><span data-stu-id="3df93-219">2148141044</span></span>  <br/> |<span data-ttu-id="3df93-220">2036</span><span class="sxs-lookup"><span data-stu-id="3df93-220">2036</span></span>  <br/> |
|<span data-ttu-id="3df93-221">#N/A</span><span class="sxs-lookup"><span data-stu-id="3df93-221">#N/A</span></span>  <br/> |<span data-ttu-id="3df93-222">2148141050</span><span class="sxs-lookup"><span data-stu-id="3df93-222">2148141050</span></span>  <br/> |<span data-ttu-id="3df93-223">2042</span><span class="sxs-lookup"><span data-stu-id="3df93-223">2042</span></span>  <br/> |
   
<span data-ttu-id="3df93-224">����̃o���A���g�^�� **ulVal** �l�́A **CVerr** �����̒l�� 16 �i���� x800A0000 ���������̂Ɠ����ɂȂ�_�ɒ��ڂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3df93-224">Note that the Variant **ulVal** value given is equivalent to the **CVerr** argument value plus x800A0000 hexadecimal.</span></span> 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a><span data-ttu-id="3df93-225">ワークシートから直接、DLL 関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="3df93-225">Calling DLL functions directly from the worksheet</span></span>

<span data-ttu-id="3df93-p118">���Ƃ��΁A�C���^�[�t�F�C�X�Ƃ��� VBA �܂��� XLM ��g�p���邱�ƂȂ��A���[�N�V�[�g���� Win32 DLL �̊֐��ɃA�N�Z�X���邱�Ƃ͂ł��܂���B�܂��A���̊֐��̈����Ɩ߂�l�̌^�ɂ��Ď��O�� Excel �ɒm�点�Ă����K�v�����܂��B�����s���v���Z�X��A�o�^�ƌĂт܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p118">You cannot access Win32 DLL functions from the worksheet without, for example, using VBA or XLM as interfaces, or without letting Excel know about the function, its arguments, and its return type in advance. The process of doing this is called registration.</span></span>
  
<span data-ttu-id="3df93-228">���Ɏ����悤�ȕ��@�ŁA���[�N�V�[�g���� DLL �̊֐��ɃA�N�Z�X�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-228">The ways in which the functions of a DLL can be accessed in the worksheet are as follows:</span></span>
  
- <span data-ttu-id="3df93-229">�O�q�����悤�� VBA �Ŋ֐���錾���āA���̊֐��� VBA ���[�U�[��\`�֐��ŃA�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-229">Declare the function in VBA as described previously and access it via a VBA user-defined function.</span></span>
    
- <span data-ttu-id="3df93-230">XLM �}�N�� �V�[�g�� CALL ��g�p���邱�Ƃ� DLL �֐���Ăяo���āAXLM ���[�U�[��\`�֐�����A�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-230">Call the DLL function using CALL on an XLM macro sheet, and access it via an XLM user-defined function.</span></span>
    
- <span data-ttu-id="3df93-231">XLM �R�}���h�܂��� VBA �R�}���h��g�p���� XLM �� **REGISTER** �֐���Ăяo���܂��B����ɂ��A�֐������[�N�V�[�g �Z���ɓ��͂��ꂽ�Ƃ��ɁA���̊֐���F�����邽�߂� Excel ���K�v�Ƃ������񋟂��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-231">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information that Excel needs to recognize the function when it is entered into a worksheet cell.</span></span> 
    
- <span data-ttu-id="3df93-232">DLL �� XLL �ɕϊ����āAXLL ��L��������Ƃ��� C API �� **xlfRegister** �֐���g�p���Ċ֐���o�^���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-232">Turn the DLL into an XLL and register the function using the C API **xlfRegister** function when the XLL is activated.</span></span> 
    
<span data-ttu-id="3df93-p119">4 �Ԗڂ̃A�v���[�\`�͎��Ȋ����^�ł���A�֐���o�^����R�[�h�Ɗ֐��̃R�[�h�́A�ǂ��������R�[�h �v���W�F�N�g�Ɋ܂܂�Ă��܂��B�A�h�C���ɕύX������Ă�AXLM �V�[�g�� VBA �R�[�h�ɕύX�������K�v�͂���܂���BC API �̋@�\��ێ������܂ܓK�؂ɊǗ����ꂽ���@�ł����s���ɂ́ADLL �� XLL �ɕϊ����āA���̌��ʂ̃A�h�C����A�h�C�� �}�l�[�W���[�œǂݍ��ޕK�v������܂��B����ɂ��A�A�h�C�����ǂݍ��܂��� (�܂��͗L����������)�ADLL �Ō��J���Ă�֐��� Excel ����Ăяo����悤�ɂȂ�AXLL �Ɋ܂܂�邷�ׂĂ̊֐���o�^���āA���̑��� DLL �̏���������s�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p119">The fourth approach is self-contained: the code that registers the functions and the function code are both contained in the same code project. Making changes to the add-in does not involve making changes to an XLM sheet or to a VBA code module. To do this in a well-managed way while still staying within the capabilities of the C API, you must turn your DLL into an XLL and load the resulting add-in by using the Add-in Manager. This enables Excel to call a function that your DLL exposes when the add-in is loaded or activated, from which you can register all of the functions your XLL contains, and carry out any other DLL initialization.</span></span>
  
## <a name="calling-dll-commands-directly-from-excel"></a><span data-ttu-id="3df93-237">Excel から直接 DLL のコマンドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="3df93-237">Calling DLL commands directly from Excel</span></span>

<span data-ttu-id="3df93-238">Win32 DLL �R�}���h�́AVBA �Ȃǂ̃C���^�[�t�F�C�X�����݂��Ȃ��ꍇ��A���O�ɃR�}���h���o�^����Ă��Ȃ��ꍇ�́AExcel �̃_�C�A���O �{�b�N�X�⃁�j���[���璼�ڃA�N�Z�X���邱�Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="3df93-238">Win32 DLL commands are not accessible directly from Excel dialog boxes and menus without there being an interface, such as VBA, or without the commands being registered in advance.</span></span>
  
<span data-ttu-id="3df93-239">���Ɏ����悤�ȕ��@�� DLL �̃R�}���h�ɃA�N�Z�X�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-239">The ways in which you can access the commands of a DLL are as follows:</span></span>
  
- <span data-ttu-id="3df93-240">�O�q�����悤�� VBA �ŃR�}���h��錾���āAVBA �}�N������A�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-240">Declare the command in VBA as described previously and access it via a VBA macro.</span></span>
    
- <span data-ttu-id="3df93-241">XLM �}�N�� �V�[�g�� **CALL** ��g�p���邱�Ƃ� DLL �R�}���h��Ăяo���āAXLM �}�N������A�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-241">Call the DLL command using **CALL** on an XLM macro sheet, and access it via an XLM macro.</span></span> 
    
- <span data-ttu-id="3df93-242">XLM �R�}���h�܂��� VBA �R�}���h��g�p���� XLM �� **REGISTER** �֐���Ăяo���܂��B����ɂ��A�}�N�� �R�}���h�̖��O����҂���_�C�A���O �{�b�N�X�ɃR�}���h�����͂��ꂽ�Ƃ��ɁA���̃R�}���h��F�����邽�߂� Excel ���K�v�Ƃ����񂪒񋟂���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-242">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information Excel needs to recognize the command when it is entered into a dialog box that expects the name of a macro command.</span></span> 
    
- <span data-ttu-id="3df93-243">DLL �� XLL �ɕϊ����āAC API �� **xlfRegister** �֐���g�p���ăR�}���h��o�^���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-243">Turn the DLL into an XLL and register the command using the C API **xlfRegister** function.</span></span> 
    
<span data-ttu-id="3df93-p120">DLL �֐��Ɋւ��đO�q�����悤�ɁA4 �Ԗڂ̃A�v���[�\`���ł���Ȋ����I�ł���A�o�^�̃R�[�h��R�}���h�̃R�[�h�ɋ߂Â����܂��B�����s���ɂ́ADLL �� XLL �ɕϊ����A���̌��ʂ̃A�h�C����A�h�C�� �}�l�[�W���[�Ń��[�h����K�v������܂��B���̕��@�ŃR�}���h��o�^����ƁA�R�}���h����[�U�[ �C���^�[�t�F�C�X�̗v�f�ɉ����邱�Ƃ�ł��܂� (�J�X�^�� ���j���[�Ȃ�)�B�܂��A����̃L�[�{�[�h����Ȃǂ̃C�x���g�ŃR�}���h��Ăяo���C�x���g �g���b�v��ݒ肷�邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p120">As discussed earlier in the context of DLL functions, the fourth approach is the most self-contained, keeping the registration code close to the command code. To do this, you must turn your DLL into an XLL and load the resulting add-in using the Add-in Manager. Registering commands in this way also lets you attach the command to an element of the user interface, such as a custom menu, or to set up an event trap that calls the command on a given keystroke or other event.</span></span>
  
<span data-ttu-id="3df93-247">Exce �ɓo�^���ꂽ���ׂĂ� XLL �R�}���h�ɂ��āAExcel �ł́A���̌\`���ɂȂ��Ă���ƌ��Ȃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-247">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> <span data-ttu-id="3df93-p121">Excel �͖߂�l�𖳎����܂��B�������AXLM �}�N�� �V�[�g����Ăяo���ꂽ��̂�����܂� (���̏ꍇ�A�߂�l�� **TRUE** �܂��� **FALSE** �ɕϊ�����܂�)�B���̂��߁A�R�}���h������Ɏ��s���ꂽ�ꍇ�� 1 ��Ԃ��K�v������܂��B�܂��A�R�}���h�����s������A���[�U�[�ɂ���Ď������ꂽ�肵���ꍇ�� 0 ��Ԃ��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p121">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span> 
  
## <a name="dll-memory-and-multiple-dll-instances"></a><span data-ttu-id="3df93-250">DLL のメモリと複数の DLL インスタンス</span><span class="sxs-lookup"><span data-stu-id="3df93-250">DLL memory and multiple DLL instances</span></span>

<span data-ttu-id="3df93-p122">�A�v���P�[�V������ DLL ����[�h����ƁADLL �̎��s�\�R�[�h���O���[�o�� �q�[�v�Ƀ��[�h����āA���̃R�[�h�����s�ł���悤�ɂȂ�܂��B���̂Ƃ��A���̃R�[�h�̃f�[�^�\���̗p�̗̈悪�O���[�o�� �q�[�v�Ɋ��蓖�Ă��܂��BWindows �́A������ �}�b�s���O��g�p���āA���̃������̗̈��A�v���P�[�V�����̃v���Z�X�ł��邩�̂悤�Ɋm�ۂ��邽�߁A�A�v���P�[�V�����́A���̗̈�ɃA�N�Z�X�ł���悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p122">When an application loads a DLL, the DLL's executable code is loaded into the global heap so that it can be run, and space is allocated on the global heap for its data structures. Windows uses memory mapping to make these areas of memory appear as if they are in the application's process so that the application can access them.</span></span>
  
<span data-ttu-id="3df93-p123">���̌�A2 �Ԗڂ̃A�v���P�[�V������ DLL ����[�h���Ă�AWindows �� DLL �̎��s�\�R�[�h�̃R�s�[��ʂɍ쐬���邱�Ƃ͂���܂��� (���̃������͓ǂݎ���p�ɂȂ��Ă��邽��)�BWindows �́ADLL �̎��s�\�R�[�h�̃������𗼕��̃A�v���P�[�V�����̃v���Z�X�Ƀ}�b�s���O���܂��B�������ADLL �̃f�[�^�\���̂̃v���C�x�[�g �R�s�[�p�� 2 �Ԗڂ̗̈悪���蓖�Ă��A���̃R�s�[�� 2 �Ԗڂ̃v���Z�X��p�Ƀ}�b�s���O����܂��B����ɂ��A�ǂ���̃A�v���P�[�V��������݂� DLL �f�[�^�Ɋ����Ȃ��悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p123">If a second application then loads the DLL, Windows does not make another copy of the DLL executable code, as that memory is read-only. Windows maps the DLL executable code memory to the processes of both applications. It does, however, allocate a second space for a private copy of the DLL's data structures and maps this copy to the second process only. This ensures that neither application can interfere with the DLL data of the other.</span></span>
  
<span data-ttu-id="3df93-p124">���̂��߁ADLL �J���҂́A�ÓI�ϐ���O���[�o���ϐ��A�f�[�^�\���̂������̃A�v���P�[�V��������A�N�Z�X���ꂽ��A�����A�v���P�[�V�����̕����̃C���X�^���X����A�N�Z�X���ꂽ�肷�邱�Ƃɂ��ĐS�z����K�v���Ȃ��Ȃ�܂��B���ׂẴA�v���P�[�V�����̊e�C���X�^���X�́A���ꂼ��ɐ�p�� DLL �f�[�^�̃R�s�[��m�ۂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3df93-p124">This means that DLL developers do not have to be concerned about static and global variables and data structures being accessed by more than one application, or more than one instance of the same application. Every instance of every application gets its own copy of the DLL's data.</span></span>
  
<span data-ttu-id="3df93-p125">DLL �J���҂́A�A�v���P�[�V�����̓����C���X�^���X���A���̃C���X�^���X��p�� DLL ��ʂ̃X���b�h���牽���Ăяo�����Ƃɂ��Ĕz������K�v������܂��B���̏ꍇ�́A���̃C���X�^���X�̃f�[�^�ɋ�������������\��������܂��B�ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3df93-p125">DLL developers do need to be concerned about the same instance of an application calling their DLL many times from different threads, because this can result in contention for that instance's data. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3df93-261">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3df93-261">See also</span></span>

- [<span data-ttu-id="3df93-262">DLL ��J������</span><span class="sxs-lookup"><span data-stu-id="3df93-262">Developing DLLs</span></span>](developing-dlls.md) 
- [<span data-ttu-id="3df93-263">DLL �܂��� XLL ���� Excel �ɌĂяo��</span><span class="sxs-lookup"><span data-stu-id="3df93-263">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)

