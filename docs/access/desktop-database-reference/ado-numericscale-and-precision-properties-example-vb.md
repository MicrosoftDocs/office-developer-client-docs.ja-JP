---
title: ADO NumericScale と Precision プロパティの使用例 (VB)
TOCTitle: NumericScale and Precision properties example (VB)
ms:assetid: 060394b1-0c2c-3726-92a0-0f350bbaa3d5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15)
ms:contentKeyID: 48543044
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ed77da6c537407d347ff6d4ebf9d254986c8618
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869695"
---
# <a name="ado-numericscale-and-precision-properties-example-vb"></a>ADO NumericScale と Precision プロパティの使用例 (VB)


**適用されます**Access 2013、Office 2013。

この例では、[NumericScale](numericscale-property-ado.md) プロパティと [Precision](precision-property-ado.md) プロパティを使って、***Pubs*** データベースの ***Discounts*** テーブル内にあるフィールドの小数点以下の桁数と精度を表示します。

```vb 
 
'BeginNumericScaleVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim rstDiscounts As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim fldTemp As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLDiscounts As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset 
 Set rstDiscounts = New ADODB.Recordset 
 strSQLDiscounts = "Discounts" 
 rstDiscounts.Open strSQLDiscounts, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 
 ' Display numeric scale and precision of 
 ' numeric and small integer fields 
 For Each fldTemp In rstDiscounts.Fields 
 If fldTemp.Type = adNumeric Or fldTemp.Type = adSmallInt Then 
 MsgBox "Field: " & fldTemp.Name & vbCr & _ 
 "Numeric scale: " & _ 
 fldTemp.NumericScale & vbCr & _ 
 "Precision: " & fldTemp.Precision 
 End If 
 Next fldTemp 
 
 ' clean up 
 rstDiscounts.Close 
 Cnxn.Close 
 Set rstDiscounts = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstDiscounts Is Nothing Then 
 If rstDiscounts.State = adStateOpen Then rstDiscounts.Close 
 End If 
 Set rstDiscounts = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndNumericScaleVB 
```

