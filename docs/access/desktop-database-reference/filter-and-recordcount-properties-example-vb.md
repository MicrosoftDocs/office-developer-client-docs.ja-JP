---
title: Filter プロパティと RecordCount プロパティの使用例 (VB)
TOCTitle: Filter and RecordCount properties example (VB)
ms:assetid: 3da4623e-03e7-27ac-7351-3b22415be0b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249167(v=office.15)
ms:contentKeyID: 48544354
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f892349d2ddb9c8fc5063d3fbec37ca9ef0d469f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292483"
---
# <a name="filter-and-recordcount-properties-example-vb"></a>Filter プロパティと RecordCount プロパティの使用例 (VB)


**適用先:** Access 2013、Office 2013

この例では、**Pubs** データベースの Publishers テーブルにある ***Recordset*** を開きます。 次に、 [Filter](filter-property-ado.md) プロパティを使って、特定の国/領域のパブリッシャーに対して表示されるレコードの数を制限します。 **RecordCount** プロパティは、フィルターが適用されているレコードセットとフィルターが適用されていないレコードセットとの相違を示すために使います。

```vb 
 
'BeginFilterVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim SQLPublishers As String 
 
 ' criteria variables 
 Dim intPublisherCount As Integer 
 Dim strCountry As String 
 Dim strMessage As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with data from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 SQLPublishers = "publishers" 
 rstPublishers.Open SQLPublishers, strCnxn, adOpenStatic, , adCmdTable 
 
 intPublisherCount = rstPublishers.RecordCount 
 
 ' get user input 
 strCountry = Trim(InputBox("Enter a country to filter on (e.g. USA):")) 
 
 If strCountry <> "" Then 
 ' open a filtered Recordset object 
 rstPublishers.Filter = "Country ='" & strCountry & "'" 
 
 If rstPublishers.RecordCount = 0 Then 
 MsgBox "No publishers from that country." 
 Else 
 ' print number of records for the original recordset 
 ' and the filtered recordset 
 strMessage = "Orders in original recordset: " & _ 
 vbCr & intPublisherCount & vbCr & _ 
 "Orders in filtered recordset (Country = '" & _ 
 strCountry & "'): " & vbCr & _ 
 rstPublishers.RecordCount 
 MsgBox strMessage 
 End If 
 End If 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndFilterVB 
```


> [!NOTE]
> [!メモ] 選択するデータがわかっている場合は、SQL ステートメントを使用して **Recordset** を開く方が一般に効率的です。この例は、単一の **Recordset** を作成し、特定の国/地域からレコードを取得する方法を示します。



```vb 
 
'BeginFilter2VB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLPublishers As String 
 Dim strCnxn As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with criteria from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 strSQLPublishers = "SELECT * FROM publishers WHERE Country = 'USA'" 
 rstPublishers.Open strSQLPublishers, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' print recordset 
 rstPublishers.MoveFirst 
 Do While Not rstPublishers.EOF 
 Debug.Print rstPublishers!pub_name & ", " & rstPublishers!country 
 rstPublishers.MoveNext 
 Loop 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndFilter2VB 
```

