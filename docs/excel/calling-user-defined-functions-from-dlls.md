---
title: Dll からユーザー定義関数の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], calling from dlls,user-defined functions [Excel 2007], calling from DLLs,DLLs [Excel 2007], calling UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798776"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Dll からユーザー定義関数の呼び出し

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���[�N�V�[�g����̃��[�U�[��[](xludf.md)�ς݊֐��R�[�h�͂���܂���BUDF ��Ăяo����悤�ɁAC API �� XLL ��p�̊֐��A�܂� [xlUDF ](xludf.md) �֐���G�N�X�|�[�g���܂��B�֐��̍ŏ��̈����́A�֐����ł��镶����ŁA�㑱�̈����� UDF ���ʏ�z�肵�Ă��镶����ł��B 
  
���� 44 ��w�肵�� **xlfGetWorkspace** �֐���g�p���āA���ݓo�^����Ă��� XLL �A�h�C���̊֐��ƃR�}���h�̈ꗗ��擾�ł��܂��B����� 3 ��̔z���Ԃ��A�e��͎���\���܂��B 
  
- XLL �̊��S�p�X�ƃt�@�C����
    
- XLL ����G�N�X�|�[�g���ꂽ UDF �܂��̓R�}���h�̖��O
    
- �߂�l�ƈ����R�[�h������
    
> [!NOTE]
> [!����] XLL �t�@�C������G�N�X�|�[�g���ꂽ�Ƃ��̖��O�́AExcel ���F�����Ă��� UDF �܂��̓R�}���h�̓o�^���Ƃ͈�v���Ȃ��\��������܂��B 
  
Excel 2007 �ȍ~�́A���̓c�[�� (ATP) �֐��͊��S�ɑg�ݍ��܂�Ă���AC API �ɂ́APRICE �� **xlfPrice** �Ȃǂ̊֐��ɑ΂��邻�̓Ǝ��̗񋓑̂�����܂��B�ȑO�̃o�[�W�����ł́A���������֐��̎g�p�ɂ́A **xlUDF** ��g�p����K�v������܂����B�A�h�C���� Excel 2003 ����� Excel 2007 �ȍ~�̃o�[�W�����Ŏg���K�v������A�A�h�C�������������֐���g���ꍇ�A���[�U�[���ŐV�o�[�W��������肵�āA�K�؂ȕ��@�Ŋ֐���Ăяo���K�v������܂��B 
  
## <a name="examples"></a>��

���̗�́A���s���� Excel �̃o�[�W������ 2003 �ȑO�̏ꍇ�ɁAATP �֐� **PRICE** ��Ăяo�� **xlUDF** �֐���\���Ă��܂��B�O���[�o�� �o�[�W�����ϐ� (���̗�ł� **gExcelVersion12plus** �Ȃ�) �̐ݒ�ɂ��ẮA [���ʌ݊���](backward-compatibility.md) ��Q�Ƃ��Ă��������B
  
> [!NOTE]
> [!����] ���̗�ł́A�t���[�����[�N�֐� **TempNum**�A **TempStrConst** ��g�p���A��������� Excel �� C API ��Ăяo���悤�ɐݒ肵�Ă��܂��B 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

�C���v���[�X�ň�����ύX���āA�l��Ԃ� XLL �֐���Ăяo���Ă�A **xlUDF** �֐��͂���܂łǂ���A���� **XLOPER/XLOPER12** �̃A�h���X��g�p���Ēl��Ԃ��܂��B�܂�A�ʏ�� return �X�e�[�g�����g��p���邩�̂悤�ɂ��Č��ʂ�Ԃ��܂��B�߂�l�Ɏg�p���������ɑΉ����� **XLOPER/XLOPER12** �͕ύX����Ă��܂���B���Ƃ��΁A���� 2 �� UDF ��l���Ă݂Ă��������B 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

**UDF\_2**の呼び出し**UDF\_1**、 **pxArg**の値変更されず**Excel12**への呼び出しの後、 **xRetVal**の**UDF_1**によって返される値が含まれています。
  
���̕��@�� UDS �ւ̌Ăяo���񐔂𑽂��s���ꍇ�A�܂��ŏ��� [xlfEvaluate �֐�](xlfevaluate.md)��g�p���Ċ֐��̖��O��]���ł��܂��B���̌��ʂ̐��́A **xlfRegister** �֐����Ԃ��o�^ ID �Ɠ����ŁA�֐����̑���� **xlUDF** �֐��ւ̍ŏ��̈����Ƃ��ēn�����Ƃ��ł��܂��B����ɂ�� Excel �́A�֐����̌���������K�v�ȏꍇ�ɔ�ׁA��葬���֐�������A�Ăяo�����Ƃ��ł��܂��B 
  
## <a name="see-also"></a>�֘A����

- [���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Excel XLL SDK �̊T�v](getting-started-with-the-excel-xll-sdk.md)

