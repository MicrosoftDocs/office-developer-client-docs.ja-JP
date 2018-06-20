---
title: 関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xll functions [excel 2007], calling from replace dialog box,Replace dialog box [Excel 2007], calling XLL functions,Function Wizard [Excel 2007], calling XLL functions,XLL functions [Excel 2007], calling from Function Wizard
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798894"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�����̏ꍇ�AMicrosoft Excel �̓u�b�N (�v�Z���}�N���̐��䉺�ɂ���ꍇ�̓u�b�N�̈ꕔ) �̒ʏ�̍Čv�Z���� XLL �֐���Ăяo���܂��B�֐��͖��O�t���͈͂����t�������ݒ莮�Ɋ܂܂�Ă��邱�Ƃ�����A�Z���̐����ɂ͑��݂��Ȃ����Ƃ�����_�ɒ��ӂ��Ă��������B
  
2 つ、[Excel] ダイアログ ボックスから関数を呼び出すことができます。 1 つは、**貼り付けの関数の引数**] ダイアログ ボックスは、ユーザーが同時に関数呼び出しの 1 つの引数を構築することです。 数式がされているときは、もう一方を変更し、[**置換**] ダイアログ ボックスで Excel を使用して再入力します。 ダイアログ ボックスの [**貼り付けの関数の引数**は、正常に実行する関数をしないことも。 実行に時間がかかるし、ダイアログ ボックスを使用して速度が低下しない可能性があります。 
  
**[関数貼り付け**] ダイアログ ボックスと、[**置換**] ダイアログ ボックスの両方がある Windows クラスの名前・ **bosa_sdm_XL**・ n、n は数値です。 Windows には、 **GetClassName**Windows のハンドル、HWND 変数の型からこの名前を取得する API 関数が用意されています。 また、 **EnumWindows**、(DLL) 内で指定されたコールバック関数を呼び出す別の関数と現在開いているすべてのトップレベル ウィンドウの。
  
�R�[���o�b�N�֐��́A���̎菇�ł̂ݎ��s����K�v������܂��B
  
1. ���̃E�B���h�E�̐e�� Excel �̌��݂̃C���X�^���X�ł��邱�Ƃ�m�F���܂� (���s���̃C���X�^���X����������ꍇ)�B
    
2. Windows �ɂ���ēn���ꂽ�n���h������N���X����擾���܂��B
    
3. �N���X���� **bosa_sdm_XL**n �̌`���ł��邱�Ƃ�m�F���܂��B
    
4. 2 つのダイアログ ボックスの間の区別をする場合は、ダイアログ ボックスのタイトルに識別するテキストが含まれているかどうかを確認してください。 **GetWindowText**Windows API 呼び出しを使用して、ウィンドウのタイトルを取得します。
    
���� C++ �R�[�h�́AWindows �ɓn�����N���X�ƃR�[���o�b�N������Ă��܂� (��L�̎菇����s���܂�)�B����́A�Y������_�C�A���O �{�b�N�X�̂ǂ��炩�ɐ�p�̃e�X�g��Ăяo���֐�����Ăяo���܂��B 
  
> [!NOTE]
> [!����] ������ Excel �̃o�[�W�����̃E�B���h�E �^�C�g���͕ύX�����\��������A���̃R�[�h�������ɂȂ邱�Ƃ�����܂��B�܂��A **window_title_text** �� **NULL** �ɐݒ肷��ƁA�R�[���o�b�N�̌����ŃE�B���h�E �^�C�g���𖳎�����Ƃ������ʂ������܂��B 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

**[�֐��̓\��t��]** �_�C�A���O �{�b�N�X�ɂ̓^�C�g��������܂���B���̂��߁A���Ɏ����֐��ł́A�^�C�g���̂Ȃ��E�B���h�E�Ƃ�����v�����\�����߂ɁA�^�C�g�������̕�����ɋ�̕�����ł��� "" ��R�[���o�b�N�֐��ɓn���Ă��܂��B 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a>�֘A����



[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)
  
[DLL �܂��� XLL ���� Excel �ɌĂяo��](calling-into-excel-from-the-dll-or-xll.md)
  
[Excel XLL �̊J��](developing-excel-xlls.md)

