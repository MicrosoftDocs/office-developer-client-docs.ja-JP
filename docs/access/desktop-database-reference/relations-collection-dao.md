---
title: Relations コレクション (DAO)
TOCTitle: Relations Collection
ms:assetid: 8929b5cc-cf52-03f2-8cf5-7f45276d258e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197067(v=office.15)
ms:contentKeyID: 48546153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78fdc7fc236a3e366cc97d466deb1e31cc030ac7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919473"
---
# <a name="relations-collection-dao"></a><span data-ttu-id="70c37-102">Relations コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="70c37-102">Relations collection (DAO)</span></span>


<span data-ttu-id="70c37-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="70c37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70c37-104">**Relations** コレクションには、 **Database** オブジェクトの、格納された **Relation** オブジェクトが含まれます (Microsoft Access データベース エンジンのデータベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="70c37-104">A **Relations** collection contains stored **Relation** objects of a **Database** object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="70c37-105">注釈</span><span class="sxs-lookup"><span data-stu-id="70c37-105">Remarks</span></span>

<span data-ttu-id="70c37-p101">**Relation** オブジェクトを使用すると、新しいリレーションシップを作成し、データベースの既存のリレーションシップを確認できます。 **Relation** オブジェクトを **Relations** コレクションに追加するには、 **CreateRelation** メソッドを使用してオブジェクトを作成してから **Append** メソッドを使用して **Relations** コレクションに追加します。これによって、 **Database** オブジェクトを閉じたときに **Relation** オブジェクトが保存されます。コレクションから **Relation** オブジェクトを削除するには、 **Delete** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="70c37-p101">You can use the **Relation** object to create new relationships and examine existing relationships in your database. To add a **Relation** object to the **Relations** collection, first create it with the **CreateRelation** method, and then append it to the **Relations** collection with the **Append** method. This will save the **Relation** object when you close the **Database** object. To remove a **Relation** object from the collection, use the **Delete** method.</span></span>

<span data-ttu-id="70c37-110">コレクション内の **Relation** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="70c37-110">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="70c37-111">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="70c37-111">**Relations**(0)</span></span>

<span data-ttu-id="70c37-112">**関係**("name")</span><span class="sxs-lookup"><span data-stu-id="70c37-112">**Relations**("name")</span></span>

<span data-ttu-id="70c37-113">**関係**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="70c37-113">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="70c37-114">例</span><span class="sxs-lookup"><span data-stu-id="70c37-114">Example</span></span>

<span data-ttu-id="70c37-p102">この例では、既存の **Relation** オブジェクトがデータ入力を制御する方法を示します。このプロシージャは、故意に正しくない CategoryID を使用してレコードを追加します。これによって、エラー処理ルーチンが起動します。</span><span class="sxs-lookup"><span data-stu-id="70c37-p102">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

```vb
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

<span data-ttu-id="70c37-p103">この例では、 **CreateRelation** メソッドを使用して、Employees **TableDef** と新規作成された Departments という **TableDef** の間に **Relation** を作成します。この例では、 **Relation** を新規作成することによって、外部テーブルに必要な **Indexes** が作成されることも示します (Employees テーブルの DepartmentsEmployees Index)。</span><span class="sxs-lookup"><span data-stu-id="70c37-p103">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
