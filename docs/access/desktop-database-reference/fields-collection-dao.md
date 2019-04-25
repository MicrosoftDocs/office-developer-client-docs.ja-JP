---
title: Fields コレクション (DAO)
TOCTitle: Fields Collection
ms:assetid: 4be3ba07-20c1-d958-c1b8-7dd8b4731f60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193530(v=office.15)
ms:contentKeyID: 48544702
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: d87d1535afeaf0740627a7af3852b1929a0e6d50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292532"
---
# <a name="fields-collection-dao"></a><span data-ttu-id="64e18-102">Fields コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="64e18-102">Fields Collection (DAO)</span></span>


<span data-ttu-id="64e18-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="64e18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64e18-104">
            \*\*Fields\*\* コレクションには、\*\*Index*\*、*\*QueryDef*\*、*\*Relation**、\*\*Recordset\*\*、または \*\*TableDef\*\* オブジェクトのすべての格納済み \*\*Field\*\* オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="64e18-104">A **Fields** collection contains all stored **Field** objects of an **Index**, **QueryDef**, **Recordset**, **Relation**, or **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64e18-105">解説</span><span class="sxs-lookup"><span data-stu-id="64e18-105">Remarks</span></span>

<span data-ttu-id="64e18-p101">
            \*\*Index*\*、*\*QueryDef*\*、\*\*Relation\*\*、および \*\*TableDef*\* の各オブジェクトの \*\*Fields\*\* コレクションには、そのオブジェクトが表すフィールドの定義が含まれます。\*\*Recordset\*\* オブジェクトの \*\*Fields\*\* コレクションは、データの行、またはレコードの \*\*Field\** オブジェクトを表します。\*\*Recordset\*\* オブジェクトのカレント レコードのフィールドの値を取得および設定するには、\*\*Recordset\*\* オブジェクトの \*\*Field\*\* オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="64e18-p101">The **Fields** collections of the **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and to set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="64e18-109">コレクション内の **Field** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="64e18-109">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="64e18-110">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="64e18-110">**Fields**(0)</span></span>

<span data-ttu-id="64e18-111">**Fields**(「名前」)</span><span class="sxs-lookup"><span data-stu-id="64e18-111">**Fields**("name")</span></span>

<span data-ttu-id="64e18-112">**Fields**\!\[名前\]</span><span class="sxs-lookup"><span data-stu-id="64e18-112">**Fields**\!\[name\]</span></span>

<span data-ttu-id="64e18-p102">同じ構文を使用して、作成して **Fields** コレクションに追加する **Field** オブジェクトの **Value** プロパティを参照することもできます。フィールド参照のコンテキストにより、**Field** オブジェクトと **Field** オブジェクトの **Value** プロパティのいずれを参照するかが決まります。</span><span class="sxs-lookup"><span data-stu-id="64e18-p102">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="64e18-115">例</span><span class="sxs-lookup"><span data-stu-id="64e18-115">Example</span></span>

<span data-ttu-id="64e18-p103">この例では、**Field** オブジェクトの場所 (**TableDef** の **Fields** コレクション、**QueryDef** の **Fields** コレクションなど) に応じた、**Field** オブジェクトに対して有効なプロパティを示します。このプロシージャを実行するには、FieldOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="64e18-p103">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

<span data-ttu-id="64e18-p104">この例では、**CreateField** メソッドを使用して、新しい **TableDef** に 3 つの **Fields** オブジェクトを作成します。次に、**CreateField** メソッドによって自動的に設定される、これらの **Field** オブジェクトのプロパティを表示します (**Field** オブジェクトの作成時に値が空のプロパティは表示されません)。</span><span class="sxs-lookup"><span data-stu-id="64e18-p104">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
