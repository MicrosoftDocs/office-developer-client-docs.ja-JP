---
title: Field2.DataUpdatable プロパティ (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7360e5ddf45275983521ddf7e1140321cc19630
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476857"
---
# <a name="field2dataupdatable-property-dao"></a><span data-ttu-id="9eec2-102">Field2.DataUpdatable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9eec2-102">Field2.DataUpdatable Property (DAO)</span></span>


<span data-ttu-id="9eec2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9eec2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="9eec2-104">**Field2** オブジェクトで表されるフィールドのデータが更新可能かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="9eec2-104">Returns a value that indicates whether the data in the field represented by a **Field2** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eec2-105">構文</span><span class="sxs-lookup"><span data-stu-id="9eec2-105">Syntax</span></span>

<span data-ttu-id="9eec2-106">*式*です。DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="9eec2-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="9eec2-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9eec2-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eec2-108">注釈</span><span class="sxs-lookup"><span data-stu-id="9eec2-108">Remarks</span></span>

<span data-ttu-id="9eec2-p101">このプロパティを使用して、 [Field2](field-value-property-dao.md) オブジェクトの \*\*\*\*Value\*\*\*\* プロパティの設定値が変更可能かどうかを識別します。このプロパティは、 \*\*\*\*Attributes\*\*\*\* プロパティが [dbAutoIncrField](field-attributes-property-dao.md) の **Field2** オブジェクトでは常に **False** です。</span><span class="sxs-lookup"><span data-stu-id="9eec2-p101">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field2** object. This property is always **False** on a **Field2** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="9eec2-111">DataUpdatable プロパティは、QueryDef、Recordset、および Relation の各オブジェクトの Fields コレクションに追加される Field2 オブジェクトでは使用できますが、Index オブジェクトまたは TableDef オブジェクトの Fields コレクションに追加される Field2 オブジェクトでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="9eec2-111">You can use the **DataUpdatable** property on **Field2** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="9eec2-112">例</span><span class="sxs-lookup"><span data-stu-id="9eec2-112">Example</span></span>

<span data-ttu-id="9eec2-p102">次の使用例では、6 つの異なる **Recordsets** オブジェクトの最初のフィールドを使用して **DataUpdatable** プロパティを示します。このプロシージャを実行するには、DataOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="9eec2-p102">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**. The DataOutput function is required for this procedure to run.</span></span>

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```
