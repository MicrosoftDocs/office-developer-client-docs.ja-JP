---
title: SortOrder プロパティの使用例 (VB)
TOCTitle: SortOrder property example (VB)
ms:assetid: 97937644-e3ef-06dc-d8ba-55ecaf7ac1ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249675(v=office.15)
ms:contentKeyID: 48546472
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58bde31a3386e3c129933d02e6464de5bc18fd68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308625"
---
# <a name="sortorder-property-example-vb"></a>SortOrder プロパティの使用例 (VB)

**適用先:** Access 2013、Office 2013

この例では、[Index](sortorder-property-adox.md) の [Columns](column-object-adox.md) コレクションに追加された [Column](columns-collection-adox.md) の [SortOrder](index-object-adox.md) プロパティの機能を示します。このコードは、 **Employees** テーブルの Country 列に昇順のインデックスを追加してレコードを表示します。次に、 **Employees** テーブルの Country 列に降順のインデックスを追加して、レコードを再表示します。これにより、昇順と降順のインデックスの違いを示します。


```vb 
 
' BeginSortOrderVB 
Sub Main() 
 On Error GoTo SortOrderXError 
 
 Dim cnn As New ADODB.Connection 
 Dim catNorthwind As New ADOX.Catalog 
 Dim idxAscending As New ADOX.Index 
 Dim idxDescending As New ADOX.Index 
 Dim rstEmployees As New ADODB.Recordset 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set catNorthwind.ActiveConnection = cnn 
 
 ' Append Country column to new index 
 idxAscending.Columns.Append "Country" 
 idxAscending.Columns("Country").SortOrder = adSortAscending 
 idxAscending.Name = "Ascending" 
 idxAscending.IndexNulls = adIndexNullsAllow 
 
 'Append new index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxAscending 
 
 rstEmployees.Index = idxAscending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Append Country column to new index 
 idxDescending.Columns.Append "Country" 
 idxDescending.Columns("Country").SortOrder = adSortDescending 
 idxDescending.Name = "Descending" 
 idxDescending.IndexNulls = adIndexNullsAllow 
 
 'Append descending index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxDescending 
 
 rstEmployees.Index = idxDescending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Delete new Indexes because this is a demonstration. 
 catNorthwind.Tables("Employees").Indexes.Delete idxAscending.Name 
 catNorthwind.Tables("Employees").Indexes.Delete idxDescending.Name 
 
 'Clean up 
 cnn.Close 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 Set rstEmployees = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
SortOrderXError: 
 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndSortOrderVB 
```

