---
title: Recordset プロパティ (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307652"
---
# <a name="recordseteditmode-property-dao"></a>Recordset プロパティ (DAO)


**適用先:** Access 2013、Office 2013

カレント レコードの編集状態を示す値を返します。

## <a name="syntax"></a>構文

*式*。EditMode

*式***Recordset**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

戻り値は、編集状態を示す長整数型 ( **Long**) の値です。使用できる値は、 **[EditModeEnum](editmodeenum-enumeration-dao.md)** クラスの定数のいずれかです。

**EditMode** プロパティは、検証中のエラーなどによって、編集プロセスが中断した場合に便利です。 **EditMode** プロパティの値を使用して、 **[Update](recordset-update-method-dao.md)** メソッドと **[CancelUpdate](recordset-cancelupdate-method-dao.md)** メソッドのいずれを使用する必要があるかを確認できます。

**[LockEdits](recordset-lockedits-property-dao.md)** プロパティの設定値が **True** で、 **EditMode** プロパティの設定値が **dbEditInProgress** であるかどうかを確認して、現在のページがロックされているかどうかを判断することもできます。

## <a name="example"></a>例

次の使用例は、さまざまな条件下での **EditMode** プロパティの値を示します。このプロシージャを実行するには、EditModeOutput 関数が必要です。

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```
