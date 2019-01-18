---
title: Sort プロパティの使用例 (VB)
TOCTitle: Sort property example (VB)
ms:assetid: 6f981e5e-7ee8-e1e7-bea9-7c2081400391
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249440(v=office.15)
ms:contentKeyID: 48545539
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f1d82a792961b0be398bb0ef8c2c046d9e8b375
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726226"
---
# <a name="sort-property-example-vb"></a><span data-ttu-id="5abad-102">Sort プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="5abad-102">Sort property example (VB)</span></span>


<span data-ttu-id="5abad-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5abad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5abad-104">この例では、[レコード セット](recordset-object-ado.md)オブジェクトの[Sort](sort-property-ado.md)プロパティを使用して、 ***Pubs***データベースの***Authors***テーブルから派生した**レコード セット**の行の順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="5abad-104">This example uses the [Recordset](recordset-object-ado.md) object's [Sort](sort-property-ado.md) property to reorder the rows of a **Recordset** derived from the ***Authors*** table of the ***Pubs*** database.</span></span> <span data-ttu-id="5abad-105">2 次ユーティリティ ルーチンで各行を出力します。</span><span class="sxs-lookup"><span data-stu-id="5abad-105">A secondary utility routine prints each row.</span></span>

```vb 
 
'BeginSortVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim Cnxn As New ADODB.Connection 
 Dim rstAuthors As New ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 Dim strTitle As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open client-side recordset to enable sort method 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' sort the recordset last name ascending 
 rstAuthors.Sort = "au_lname ASC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Ascending:" 
 Debug.Print "First Name Last Name" & vbCr 
 
 rstAuthors.MoveFirst 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
 ' sort the recordset last name descending 
 rstAuthors.Sort = "au_lname DESC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Descending" 
 Debug.Print "First Name Last Name" & vbCr 
 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSortVB 
```

<span data-ttu-id="5abad-106">次のコードは、与えられたタイトルと、指定された **Recordset** の内容を出力する 2 次ユーティリティ ルーチンです。</span><span class="sxs-lookup"><span data-stu-id="5abad-106">This is the secondary utility routine that prints the given title, and the contents of the specified **Recordset**.</span></span>

```vb 
 
Attribute VB_Name = "Sort" 
```

