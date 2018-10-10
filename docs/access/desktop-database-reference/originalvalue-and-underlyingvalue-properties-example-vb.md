---
title: OriginalValue プロパティと UnderlyingValue プロパティの使用例 (VB)
TOCTitle: OriginalValue and UnderlyingValue Properties Example (VB)
ms:assetid: de88d99d-7f2e-8418-b40f-0375b1d90a8e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250127(v=office.15)
ms:contentKeyID: 48548189
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab68cf5d1c398503b9d261bfb7a7b2e49a89a3d0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477759"
---
# <a name="originalvalue-and-underlyingvalue-properties-example-vb"></a><span data-ttu-id="a7b82-102">OriginalValue プロパティと UnderlyingValue プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="a7b82-102">OriginalValue and UnderlyingValue Properties Example (VB)</span></span>

<span data-ttu-id="a7b82-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7b82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a7b82-104">この例では、[OriginalValue](originalvalue-property-ado.md) プロパティと [UnderlyingValue](underlyingvalue-property-ado.md) プロパティを使用して、 [Recordset](recordset-object-ado.md) の一括更新中にレコードの基になるデータが変更された場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="a7b82-104">This example demonstrates the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties by displaying a message if a record's underlying data has changed during a [Recordset](recordset-object-ado.md) batch update.</span></span>

```vb 
 
'BeginOriginalValueVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstTitles As ADODB.Recordset 
 Dim fldType As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' Open connection. 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset for batch update 
 ' using object refs to set properties 
 Set rstTitles = New ADODB.Recordset 
 Set rstTitles.ActiveConnection = Cnxn 
 rstTitles.CursorType = adOpenKeyset 
 rstTitles.LockType = adLockBatchOptimistic 
 strSQLTitles = "titles" 
 rstTitles.Open strSQLTitles 
 
 ' Set field object variable for Type field 
 Set fldType = rstTitles!Type 
 
 ' Change the type of psychology titles 
 Do Until rstTitles.EOF 
 If Trim(fldType) = "psychology" Then 
 fldType = "self_help" 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Similate a change by another user by updating 
 ' data using a command string 
 Cnxn.Execute "UPDATE Titles SET type = 'sociology' " & _ 
 "WHERE type = 'psychology'" 
 
 'Check for changes 
 rstTitles.MoveFirst 
 Do Until rstTitles.EOF 
 If fldType.OriginalValue <> fldType.UnderlyingValue Then 
 MsgBox "Data has changed!" & vbCr & vbCr & _ 
 " Title ID: " & rstTitles!title_id & vbCr & _ 
 " Current value: " & fldType & vbCr & _ 
 " Original value: " & _ 
 fldType.OriginalValue & vbCr & _ 
 " Underlying value: " & _ 
 fldType.UnderlyingValue & vbCr 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Cancel the update because this is a demonstration 
 rstTitles.CancelBatch 
 
 ' Restore original values 
 Cnxn.Execute "UPDATE Titles SET type = 'psychology' " & _ 
 "WHERE type = 'sociology'" 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstTitles Is Nothing Then 
 If rstTitles.State = adStateOpen Then rstTitles.Close 
 End If 
 Set rstTitles = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOriginalValueVB 
```
