---
title: OrdinalPosition プロパティ (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d45f0362831d91b83b3a2449affbbfb5ac2b4e51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293036"
---
# <a name="fieldordinalposition-property-dao"></a>OrdinalPosition プロパティ (DAO)


**適用先:** Access 2013、Office 2013

**[Fields](fields-collection-dao.md)** コレクション内の**[Field](field-object-dao.md)** オブジェクトの相対位置を設定または取得します。 .

## <a name="syntax"></a>構文

*式*。OrdinalPosition

*式***Field**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Fields** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

既定値は 0 です。

**OrdinalPosition** プロパティを使用できるかどうかは、次の表に示すように、**Fields** コレクションを含むオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションが属するオブジェクト</p></th>
<th><p>OrdinalPosition プロパティの使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p>サポートされない</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>値の取得および設定が可能です。</p></td>
</tr>
</tbody>
</table>


通常、コレクションに追加するオブジェクトの順序位置は、そのオブジェクトを追加した順序になります。 最初に追加したオブジェクトが最初の位置 (0) に格納され、2 番目に追加したオブジェクトは 2 番目の位置 (1) に格納され、これ以降も同様です。 最後に追加されたオブジェクトは、位置を表す count –1、count プロパティの設定値で指定された**[](containers-count-property-dao.md)** コレクション内のオブジェクトの数です。

**OrdinalPosition** プロパティを使用すると、新しい **Field** オブジェクトの順序位置を指定可能で、これは、これらのオブジェクトをコレクションに追加するときの順序と異なります。 これにより、テーブル、クエリ、およびレコードセットをアプリケーションで使用するときのフィールドの順序を指定できます。 たとえば、選択\*クエリでフィールドが返される順序は、現在の**OrdinalPosition**プロパティの値によって決まります。

**OrdinalPosition** プロパティを任意の正の整数に設定することにより、レコードセットにフィールドが返される順序を永続的にリセットできます。

同じコレクション内の複数の **Field** オブジェクトが同じ **OrdinalPosition** プロパティ値を持つことが可能で、この場合、これらのオブジェクトの順序はアルファベット順になります。たとえば、Age という名前のフィールドを 4 に設定し、2 番目の Weight という名前のフィールドも 4 に設定すると、Age の後に Weight が返されます。

フィールド数から 1 を引いた数値より大きい数値を指定できます。フィールドは、最も大きい数値に対する相対的な順序で返されます。たとえば、フィールドの **OrdinalPosition** プロパティを 20 に設定し (フィールドは 5 つのみ)、他の 2 つのフィールドの **OrdinalPosition** プロパティをそれぞれ 10 と 30 に設定した場合、20 に設定されたフィールドは、10 に設定されたフィールドと 30 に設定されたフィールドの間に返されます。

> [!NOTE]
> [tabledef](tabledef-object-dao.md)の**Fields**コレクションが更新されていない場合でも、tabledef から開いた[Recordset](recordset-object-dao.md)内の**** フィールドの順序には、 **tabledef**オブジェクトの**OrdinalPosition**データが反映されます。 テーブル タイプの **Recordset** には、基になるテーブルと同じ **OrdinalPosition** データが使用されますが、その他のタイプの **Recordset** には、**TableDef** オブジェクトの **OrdinalPosition** データによって指定される順序に従った、0 から始まる新しい **OrdinalPosition** データが使用されます。

## <a name="example"></a>例

次の例は、 **Recordset** オブジェクト内の **Field** オブジェクトの順序を制御するために、Employees **TableDef** オブジェクトの **OrdinalPosition** プロパティの値を変更します。すべての **Fields** オブジェクトの **OrdinalPosition** プロパティを 1 に設定することにより、 **Recordset** オブジェクトの **Fields** オブジェクトは順序がアルファベット順になります。 **Recordset** オブジェクトの **OrdinalPosition** 値は **TableDef** オブジェクトの値と一致しませんが、最終的な **TableDef** の変更には反映されます。

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
