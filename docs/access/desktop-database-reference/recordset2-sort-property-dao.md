---
title: Recordset2 プロパティ (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309270"
---
# <a name="recordset2sort-property-dao"></a>Recordset2 プロパティ (DAO)

**適用先:** Access 2013、Office 2013 

**[Recordset](recordset-object-dao.md)** オブジェクト内のレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。モダン

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Sort** プロパティは、ダイナセット タイプおよびスナップショット タイプの **Recordset** オブジェクトで使用できます。

オブジェクトに対してこのプロパティを設定すると、それ以降にそのオブジェクトから **Recordset** オブジェクトを作成するときに、レコードが並べ替えられます。 **Sort** プロパティの設定値は、 **[QueryDef](querydef-object-dao.md)** オブジェクトに指定されているいずれの並べ替え順序よりも優先されます。

既定の並べ替え順序は、昇順 (A ～ Z、0 ～ 100、あ～ん) です。

**Sort** プロパティは、テーブル タイプまたは前方スクロール タイプの **Recordset** オブジェクトには適用されません。 テーブルタイプの**Recordset**オブジェクトを並べ替えるには、 **[Index](recordset2-index-property-dao.md)** プロパティを使用します。

> [!NOTE]
> 多くの場合、並べ替え条件を含む SQL ステートメントを使用すると、新規の **Recordset** オブジェクトをより短時間で開くことができます。

## <a name="example"></a>例

次の例では、 **Sort** プロパティの値を変更して新規の **Recordset** を作成することで、このプロパティの機能を示します。このプロシージャを実行するには、SortOutput 関数が必要です。

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

選択するデータがわかっている場合は、SQL ステートメントを使用して **Recordset** を作成する方が一般に効率的です。次の例では、ただ 1 つの **Recordset** を作成して、前の例と同じ結果を得る方法を示します。

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
