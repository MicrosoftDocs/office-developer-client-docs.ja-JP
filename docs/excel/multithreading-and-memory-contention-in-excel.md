---
title: Excel 2007 �ɂ�����}���`�X���b�h�����ƃ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading in excel,memory contention in Excel,functions [Excel 2007], thread-safe,thread-safe functions [Excel 2007],thread-local memory [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798940"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Excel 2007 �ɂ�����}���`�X���b�h�����ƃ���������

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
以前のバージョンの Microsoft Excel Excel 2007 よりもは、すべてのワークシートの計算のまま 1 つのスレッドを使用します。 ただし、Excel 2007 以降では、Excel 構成できますを使用して、1 から 1024 の同時実行スレッドにワークシートの計算をします。 マルチプロセッサまたはマルチコア コンピューターでは、既定のスレッド数はプロセッサまたはコアの数です。 したがって、スレッド セーフであるセル、またはのみ関数を含むセルはスレッド セーフで、割り当てることのできる参照元の後を計算する必要があるの通常の再計算ロジックの対象となる、同時実行スレッドにします。
  
## <a name="thread-safe-functions"></a>�X���b�h �Z�[�t�֐�

Excel 2007 �ȍ~�̑g�ݍ��݂̃��[�N�V�[�g�֐��̑����́A�X���b�h �Z�[�t�ł��BXLL �֐���X���b�h �Z�[�t�Ƃ��ċL�q���ēo�^���邱�Ƃ�ł��܂��BExcel �́A1 �̃X���b�h (���C�� �X���b�h) ��g�p���āA���ׂẴR�}���h�A�X���b�h �A���Z�[�t�֐��A **xlAuto** �֐� ( [xlAutoFree](xlautofree-xlautofree12.md) �� **xlAutoFree12** �����)�A����� COM �֐��� Visual Basic for Applications (VBA) �֐���Ăяo���܂��B
  
XLL �֐��� **xlbitDLLFree** ���ݒ肳�ꂽ **XLOPER** �܂��� **XLOPER12** ��Ԃ��ꍇ�́AExcel �͂��̊֐��̌Ăяo�������s���ꂽ�̂Ɠ����X���b�h��g�p���� **xlAutoFree** �܂��� **xlAutoFree12** ��Ăяo���܂��B **xlAutoFree** �܂��� **xlAutoFree12** �̌Ăяo���́A���̃X���b�h�Ŏ��̊֐��̌Ăяo�����s����O�ɍs���܂��B 
  
XLL �J���҂ɂƂ��āA�X���b�h �Z�[�t�֐���쐬���邱�Ƃ͗��_������܂��B
  
- そうすることにより、Excel でマルチプロセッサまたはマルチコア のコンピューターを最大限に活用することができます。
    
- 1 �̃X���b�h��g�p���čs��������ʓI�Ƀ����[�g �T�[�o�[��g�p�ł���\��������܂��B
    
���Ƃ��΁A *N*  �̃X���b�h��g�p����悤�ɍ\������Ă���V���O�� �v���Z�b�T�̃R���s���[�^�[��g�p���Ă���Ɖ��肵�܂��B���� XLL �֐�������Ăяo���X�v���b�h�V�[�g����s���Ă���Ɖ��肵�܂��B���� XLL �֐��͌Ăяo�����ƃf�[�^�̗v���܂��͌v�Z���s�̗v��������[�g �T�[�o�[�܂��̓T�[�o�[�̃N���X�^�[�ɑ��M�����̂ł��B�ˑ��֌W�c���[�̃g�|���W�Ɉˑ����� Excel �́A�֐���قړ����� N ���Ăяo�����Ƃ��ł����̂Ƃ��܂��B1 �܂��͕����̃T�[�o�[���\���ɍ����܂��͕��񂵂Ď��s����Ă���ꍇ�A�X�v���b�h�V�[�g�̍Čv�Z�Ɋ|���鎞�Ԃ� N ���� 1 ��Z�k����܂��B 
  
�X���b�h �Z�[�t�֐���L�q����ۂɏd�v�Ȃ��Ƃ́A���\�[�X�̋����𐳂����������邱�Ƃł��B�ʏ�A����̓������̋�����Ӗ����A���� 2 �̓_�ɕ����邱�Ƃ��ł��܂��B
  
- ���̃X���b�h�ł̂ݎg�p����邱�Ƃ��������Ă��郁�����̍쐬���@�B
    
- ���L�������������̃X���b�h�ɂ���ĕK�����S�ɃA�N�Z�X�����悤�ɂ�����@�B
    
�܂����ӂ��ׂ��_�́AXLL �ł��ׂẴX���b�h�ɂ���ăA�N�Z�X�\�ł��郁�����ƁA���ݎ��s���̃X���b�h�ɂ���Ă̂݃A�N�Z�X�\�ȃ������ł��B
  
 **���ׂẴX���b�h�ɂ���ăA�N�Z�X�\�Ȃ��**
  
- �֐��̖{�̂̊O���ɂ���A�錾����Ă���ϐ��A�\���́A����уN���X�B
    
- �֐��̖{�̓�Ő錾���ꂽ�ÓI�ϐ��B
    
������ 2 �̏ꍇ�A�������́ADLL �̂��̃C���X�^���X�p�ɍ쐬���ꂽ DLL �̃����� �u���b�N�Ɋm�ۂ���Ă��܂��B�ʂ̃A�v���P�[�V���� �C���X�^���X�� DLL ��ǂݍ��ޏꍇ�́ADLL �̂��̃C���X�^���X�̊O���ł����̃��\�[�X�̋������N���Ȃ��悤�ɁA���̃������̓Ǝ��̃R�s�[��擾���܂��B
  
 **���݂̃X���b�h�ɂ���Ă̂݃A�N�Z�X�\�Ȃ��**
  
- �֐��̃R�[�h��̎����ϐ� (�֐��̈�����܂�)�B
    
���̏ꍇ�A�������͊֐��Ăяo���̃C���X�^���X���ƂɃX�^�b�N�Ɋm�ۂ���Ă��܂��B
  
> [!NOTE]
> [!����] ���I�Ɋ��蓖�Ă�ꂽ�������͈̔͂́A�����w���|�C���^�[�͈̔͂ɂ���ĈقȂ�܂��B�|�C���^�[�����ׂẴX���b�h�ɂ���ăA�N�Z�X�\�ȏꍇ�́A����������l�ł��B�|�C���^�[���֐��̎����ϐ��ł���ꍇ�́A���蓖�Ă�ꂽ�������͂��̃X���b�h�ɑ΂��Č��ʓI�ɔ���J�ɂȂ�܂��B 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>1 �̃X���b�h�ɂ���Ă̂݃A�N�Z�X�\�ȃ�����:�X���b�h ���[�J�� ������

�֐��̖{����̐ÓI�ϐ������ׂẴX���b�h�ɂ���ăA�N�Z�X�\�ł���ꍇ�A������g�p����֐��͖��炩�ɃX���b�h �Z�[�t�ł͂���܂���B1 �̃X���b�h��ɂ���֐��� 1 �̃C���X�^���X���l��ύX���Ă���\��������A�ʂ̃X���b�h��ɂ���ʂ̃C���X�^���X�͂����܂������قȂ��̂ł���Ɖ��肵�Ă��܂��B 
  
�֐���ŐÓI�ϐ���錾���邱�Ƃɂ� 2 �̗��R������܂��B
  
1. �ÓI�f�[�^�́A1 �̌Ăяo�����玟�̌Ăяo���܂ňێ�����܂��B
    
2. �ÓI�f�[�^�ւ̃|�C���^�[�́A�֐��ɂ���Ĉ��S�ɕԂ���܂��B
    
1 �ڂ̗��R�̏ꍇ�A�֐��̂��ׂĂ̌Ăяo���ňێ�����A�Ȃ����L���ȃf�[�^ (�����炭�A�֐����X���b�h�ɌĂяo����邽�т� 1 ����������P���ȃJ�E���^�[�A�܂��͂��ׂĂ̌Ăяo���Ŏg�p���ƃp�t�H�[�}���X�f�[�^����W����\��) ��ێ����邱�Ƃ��ł��܂��B���́A���L�f�[�^�܂��̓f�[�^�\����ی삷����@�ł��B�����s���ɂ́A���̃Z�N�V�����Ő������N���e�B�J�� �Z�N�V������g�p���邱�Ƃ��őP�̕��@�ł��B
  
�f�[�^�����̃X���b�h�ł̂ݎg�p�����悤�Ӑ}����Ă���ꍇ (����͗��R �P�ɊY������ꍇ������܂��B���R 2 �ɂ͏�ɊY�����܂�)�A�������Ȃ������̃X���b�h����̂݃A�N�Z�X�ł��郁������ǂ�����č쐬���邩�����ɂȂ�܂��B1 �̉����Ƃ��āA�X���b�h ���[�J�� �X�g���[�W (TLS) API ��g�p���邱�Ƃ��������܂��B
  
���Ƃ��΁A **XLOPER** �ւ̃|�C���^�[��Ԃ��֐���l���Ă݂܂��B
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

1 �̃X���b�h�͐ÓI **XLOPER12** ��Ԃ����Ƃ��ł��A�ʂ̃X���b�h�����̃X���b�h��㏑�����Ă��邽�߁A���̊֐��̓X���b�h �Z�[�t�ł͂���܂���B **XLOPER12** �� **xlAutoFree12** �ɓn�����K�v������ꍇ�A���̂悤�Ȏ��Ԃ���������\�����傫���Ȃ�܂��B1 �̉����́A **XLOPER12** ����蓖�ĂāA����ɑ΂���|�C���^�[��Ԃ��A **XLOPER12** ���������̂���������悤�� **xlAutoFree12** ��������邱�Ƃł��B���̃A�v���[�`�́A�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v�Ɏ�����Ă��鑽���̊֐���Ŏg�p����Ă��܂��B
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

このアプローチは、TLS API に依存する次のセクションで説明されている方法よりも実装が簡単ですが、いくつかのデメリットがあります。 Excel で**xlAutoFree**を呼び出す必要があります最初に、/ **xlAutoFree12**返される**XLOPER**の種類を問わず/ **XLOPER12**。 第 2 に、問題がある**XLOPER**を返すときに/ C API のコールバック関数への呼び出しの戻り値は、**XLOPER12**s。 **XLOPER**/ **XLOPER12**は Excel では、 **XLOPER**を解放する必要のあるメモリを指す場合があります/ **XLOPER12**自体は割り当てられているのと同じ方法で解放する必要があります。 場合このような**XLOPER**/ **XLOPER12**は XLL ワークシート関数の戻り値として使用するのには、 **xlAutoFree**に通知する簡単な方法はありません/ **xlAutoFree12**を適切な方法で両方のポインターを解放する必要があるのです。 ( **XlbitXLFree**と**xlbitDLLFree**の両方を設定できない問題が解決しない、両方のセットを使用して Excel では、 **XLOPER と XLOPER12s**の処理方法は定義されていませんし、バージョンを変更する場合があります。)この問題を回避するには、xll ファイルはすべて Excel によって割り当てられる**XLOPER/XLOPER12s**ワークシートに返されるの深さのコピーを作成できます。 
  
これらの制限を回避するソリューションが追加し、スレッド ローカルの**XLOPER/XLOPER12**を返すには、その**xlAutoFree と xlAutoFree12**が必要になりますアプローチは**XLOPER/XLOPER12**ポインターそのものを解放しません。 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

���̖��́A�ǂ̂悤�ɃX���b�h ���[�J�� ��������Z�b�g�A�b�v���Ď擾���邩�ł��B�܂�A�O�̗�̊֐� **get_thread_local_xloper12** ��ǂ̂悤�Ɏ������邩�Ƃ������Ƃł��B����́A�X���b�h ���[�J�� �X�g���[�W (TLS) API ��g�p���čs���܂��B�ŏ��̎菇�Ƃ��āATLS �C���f�b�N�X�� **TlsAlloc** ��g�p���� �擾���܂��B����́A�ŏI�I�� **TlsFree** �ɂ���ĉ�������K�v������܂��B�����Ƃ� **DllMain** ����ȒP�Ɏ��s�ł��܂��B
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

�C���f�b�N�X��擾������A���ɍs���菇�̓X���b�h���ƂɃ����� �u���b�N����蓖�Ă邱�Ƃł��B[Windows �J���̃h�L�������g](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx)�ł́A����� **DllMain** �R�[���o�b�N�֐��� **DLL_THREAD_ATTACH** �C�x���g�ŌĂяo����邽�тɍs���A���ׂĂ� **DLL_THREAD_DETACH** ��̃�������J�����邱�Ƃ𐄏����Ă��܂��B�������A���̃A�h�o�C�X�ɏ]���ƁADLL �͍Čv�Z�Ɏg�p����Ȃ��X���b�h�ɑ΂��ĕs�v�ȍ�Ƃ�s�����ƂɂȂ�\��������܂��B 
  
���̕��@����A�ŏ��Ɏg�p����Ƃ��Ɋ��蓖�Ă���@��g�p���邱�Ƃ�����߂��܂��B�܂��A�X���b�h���ƂɊ��蓖�Ă�\�����`����K�v������܂��B **XLOPERs** �܂��� **XLOPER12s** ��Ԃ��O�q�̗�̏ꍇ�́A���̂Ƃ���ŏ\���ł����A���ł���j�[�Y�𖞂����\����쐬���邱�Ƃ��ł��܂��B
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

���̊֐��́A�X���b�h ���[�J�� �C���X�^���X�ւ̃|�C���^�[��擾���邩�A�܂��͂��ꂪ�ŏ��̌Ăяo���ł���ꍇ��1 ����蓖�Ă܂��B
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

����ŁA�X���b�h ���[�J�� **XLOPER/XLOPER12** ��������擾������@���킩��͂��ł��B�܂��A�X���b�h�� **TLS_data** �̃C���X�^���X�ւ̃|�C���^�[��擾���Ă���A���̂悤�ɂ��̓���Ɋ܂܂�Ă��� **XLOPER/XLOPER12** �ւ̃|�C���^�[��Ԃ��܂��B 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

**Mtr_safe_example_1**と**mtr_safe_example_2**関数は、Excel を実行している場合、スレッド セーフであるワークシート関数として登録できます。 ただし、xll ファイルの 1 つで 2 つのアプローチを組み合わせることはできません。 Xll ファイルがエクスポートできるは、 **xlAutoFree**と**xlAutoFree12**の実装の 1 つのみと、各メモリ戦略には、さまざまなアプローチが必要です。 **Mtr_safe_example_1**とを指すすべてのデータと**xlAutoFree と xlAutoFree12**に渡されたポインターを解放する必要があります。 **Mtr_safe_example_2**でポイントされるデータのみを解放する必要があります。
  
Windows �ɂ́A���݂̃X���b�h�̃V�X�e�����C�h�̈�ӂ� ID ��Ԃ��֐� **GetCurrentThreadId** �����܂��B�����A�R�[�h��X���b�h �Z�[�t�ɂ�����R�[�h�̓����X���b�h�ŗL�ɂ����肷�邽�߂̎�i�ɂȂ�܂��B
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>�����̃X���b�h�ɂ���ăA�N�Z�X�\�ȃ�����:�N���e�B�J�� �Z�N�V����

�N���e�B�J�� �Z�N�V������g�p���ĕ����̃X���b�h���A�N�Z�X�ł���ǂݎ��/�������݃�������ی삷��K�v������܂��B�ی삷�郁�����̃u���b�N���ƂɎw�肳�ꂽ�N���e�B�J�� �Z�N�V�������K�v�ƂȂ�܂��B������ **xlAutoOpen** �֐��̌Ăяo�����ɏ������ł��A�܂� **xlAutoClose** �֐��̌Ăяo�����ɁA���������Anull �ɐݒ肵���肷�邱�Ƃ��ł��܂��B **EnterCriticalSection** �� **LeaveCriticalSection** �̌Ăяo���̃y�A��ɕی삳�ꂽ�u���b�N�ւ̊e�A�N�Z�X��܂߂�K�v������܂��B�N���e�B�J�� �Z�N�V�����ւ̃A�N�Z�X��������̂́A��� 1 �̃X���b�h�݂̂ł��B�ȉ��ɁA **g_csSharedTable** �ƌĂ΂��Z�N�V�����̏������A����������A����юg�p�̗������܂��B
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

�������̃u���b�N��ی삷��A�����S�ȕʂ̕��@�͂����炭�A�Ǝ��� **CRITICAL_SECTION** �ƁA�����g�p���邽�߂̂��̃R���X�g���N�^�[�A�f�X�g���N�^�[�A����уA�N�Z�T�[�̃��\�b�h��܂ރN���X��쐬���邱�Ƃł��B���̃A�v���[�`�ɂ́A **xlAutoOpen** �̎��s�̑O�ɏ��������ꂽ�� **xlAutoClose** �̌Ăяo�����ێ����ꂽ�肷��\���̂���I�u�W�F�N�g���ی삳���Ƃ������_���ǉ�����Ă��܂��B�������A���܂�ɑ����̃N���e�B�J�� �Z�N�V�������쐬����邱�Ƃ�A����ɂ�萶����I�y���[�e�B���O �V�X�e���̃I�[�o�[�w�b�h�ɒ��ӂ���K�v������܂��B 
  
�ی삳�ꂽ�������̕����̃u���b�N�ɓ����ɃA�N�Z�X����K�v������R�[�h������ꍇ�́A�N���e�B�J�� �Z�N�V�����̊J�n�ƏI���̏�������ɐT�d�Ɍ�������K�v������܂��B���Ƃ��΁A���� 2 �̊֐��̓f�b�h���b�N��쐬����\��������܂��B
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

1 �̃X���b�h�̍ŏ��̊֐��� **g_csSharedTableA** ��J�n���A�ʂ̃X���b�h��2 �Ԗڂ̊֐��� **g_csSharedTableB** ��J�n����ƁA�����̃X���b�h���n���O���܂��B���̂悤�ɁA��т��������ŊJ�n���āA���̋t�̏����ŏI������̂��������A�v���[�`�ł��B
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

�\�ł���΁A�X���b�h�A�g�̊ϓ_����A���Ɏ����悤�ɁA�ʂ̃u���b�N�ɃA�N�Z�X�𕪗����邱�Ƃ�����߂��܂��B
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

�Z���Ԃ̃A�N�Z�X�v�����p�ɂɍs����ȂǁA���L���\�[�X�̋����������������Ă���ꍇ�́A�N���e�B�J�� �Z�N�V�����̃X�s���@�\�̗��p���������K�v������܂��B����́A���\�[�X�̑ҋ@�ɂ��v���Z�b�T�ւ̕��ׂ�Ȃ�ׂ����������邽�߂̎�@�ł��B�����s�����߂ɂ́A�Z�N�V�����̏��������� **InitializeCriticalSectionAndSpinCount**�A������͏���������Ă���� **SetCriticalSectionSpinCount** ��g�p���āA���\�[�X���g�p�\�ɂȂ�̂�ҋ@����O�ɃX���b�h�����[�v����񐔂�ݒ�ł��܂��B�@�@�@�@�@�@�@�@�ҋ@����ɂ̓R�X�g�������邽�߁A���̊ԂɃ��\�[�X����������ƁA�X�s���ɂ���đҋ@����͉�����܂��B�V���O�� �v���Z�b�T �V�X�e���ł́A�X�s�����͌��ʓI�ɖ�������܂����A�X�s������w�肵�Ă��Ă���ɂȂ邱�Ƃ͂���܂���B������ �q�[�v �}�l�[�W���[�Ŏg�p����X�s������ 4000 �ł��B�N���e�B�J�� �Z�N�V�����̎g�p�Ɋւ���ڍׂɂ��ẮAWindows SDK �̃h�L�������g����Q�Ƃ��������B 
  
## <a name="see-also"></a>�֘A����



[Excel �̃������Ǘ�](memory-management-in-excel.md)
  
[Excel �ł̃}���`�X���b�h�Čv�Z](multithreaded-recalculation-in-excel.md)
  
[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)
