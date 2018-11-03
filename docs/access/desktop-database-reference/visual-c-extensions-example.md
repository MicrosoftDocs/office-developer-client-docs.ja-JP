---
title: Visual C++ Extensions の例
TOCTitle: Visual C++ Extensions Example
ms:assetid: fe57868f-5707-3c5b-cb93-4121732d67cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250305(v=office.15)
ms:contentKeyID: 48548934
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f7bbcdc4f3ddcadfd45ba627873945ec1a3adfe
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946914"
---
# <a name="visual-c-extensions-example"></a>Visual C++ Extensions の例


**適用されます**Access 2013、Office 2013。

このプログラムは、値がフィールドからどのように取得され、C/C++ 変数に変換されるかを示します。

この例では、スマート ポインター、」の呼び出し、 **IADORecordBinding**インターフェイスに対する参照カウントの COM 固有の詳細情報を自動的に処理することも活用します。

スマート ポインターを使用しない場合は、次のようにコーディングします。

```cpp 
 
IADORecordBinding *picRs = NULL; 
... 
TESTHR(pRs->QueryInterface( 
 __uuidof(IADORecordBinding), (LPVOID*)&picRs)); 
... 
if (picRs) picRs->Release(); 
```

スマート ポインターを使用する IADORecordBindingPtr 型から派生次のステートメントで IADORecordBinding インターフェイスからの種類。

```cpp 
 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
```

そして、次のようにポインターのインスタンスを作成します。

```cpp 
 
IADORecordBindingPtr picRs(pRs); 
```

PicRs、スマート ポインターのコンス トラクターは、**レコード セット**オブジェクトでは、Visual C++ の拡張機能が実装されている、ため、 \_RecordsetPtr ポインター、pRs です。 コンス トラクターが pRs を使用して検索する QueryInterface を呼び出すのでは、 \_RecordsetPtr ポインター、pRs です。 コンス トラクターには、IADORecordBinding インターフェイスを検索するのには、pRs を使用して QueryInterface が呼び出されます。

```cpp 
 
// Visual C++ Extensions Example 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <stdio.h> 
#include <icrsint.h> 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
 
inline void TESTHR(HRESULT _hr) { if FAILED(_hr) _com_issue_error(_hr); } 
 
class CCustomRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CCustomRs) 
 ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_ch_fname, 
 sizeof(m_ch_fname), m_ul_fnameStatus, false) 
 ADO_VARIABLE_LENGTH_ENTRY2(4, adVarChar, m_ch_lname, 
 sizeof(m_ch_lname), m_ul_lnameStatus, false) 
END_ADO_BINDING() 
public: 
 CHAR m_ch_fname[22]; 
 CHAR m_ch_lname[32]; 
 ULONG m_ul_fnameStatus; 
 ULONG m_ul_lnameStatus; 
}; 
 
void main(void) 
{ 
 ::CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 CCustomRs rs; 
 IADORecordBindingPtr picRs(pRs); 
 
 pRs->Open("SELECT * FROM Employee ORDER BY lname", 
 "dsn=pubs;uid=sa;pwd=;", 
 adOpenStatic, adLockOptimistic, adCmdText); 
 
 TESTHR(picRs->BindToRecordset(&rs)); 
 
 while (!pRs->EndOfFile) 
 { 
 // Process data in the CCustomRs C++ instance variables. 
 printf("Name = %s %s\n", 
 (rs.m_ul_fnameStatus == adFldOK ? rs.m_ch_fname: "<Error>"), 
 (rs.m_ul_lnameStatus == adFldOK ? rs.m_ch_lname: "<Error>")); 
 
 // Move to the next row of the Recordset. 
 // Fields in the new row will automatically be 
 // placed in the CCustomRs C++ instance variables. 
 
 pRs->MoveNext(); 
 } 
 } 
 catch (_com_error &e ) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Meaning = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 } 
 ::CoUninitialize(); 
} 
```

