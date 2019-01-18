---
title: Recordset.Restartable プロパティ (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5142d0d47be37ca8c2e1c6b89462c05b7d41d302
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721697"
---
# <a name="recordsetrestartable-property-dao"></a><span data-ttu-id="979e7-102">Recordset.Restartable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="979e7-102">Recordset.Restartable property (DAO)</span></span>


<span data-ttu-id="979e7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="979e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="979e7-104">**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行する **[Requery](recordset-requery-method-dao.md)** メソッドを、 **Recordset** オブジェクトがサポートするかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="979e7-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="979e7-105">構文</span><span class="sxs-lookup"><span data-stu-id="979e7-105">Syntax</span></span>

<span data-ttu-id="979e7-106">*式*です。再開可能</span><span class="sxs-lookup"><span data-stu-id="979e7-106">*expression* .Restartable</span></span>

<span data-ttu-id="979e7-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="979e7-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="979e7-108">注釈</span><span class="sxs-lookup"><span data-stu-id="979e7-108">Remarks</span></span>

<span data-ttu-id="979e7-109">テーブル タイプの **Recordset** オブジェクトは、常に **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="979e7-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="979e7-p101">**Recordset** オブジェクトに対して **Requery** メソッドを使用する前に、 **Restartable** プロパティを確認します。そのオブジェクトの **Restartable** プロパティが **False** に設定されている場合は、基になる **[QueryDef](connection-openrecordset-method-dao.md)** オブジェクトの **[OpenRecordset](querydef-object-dao.md)** メソッドを使用してクエリを再実行します。</span><span class="sxs-lookup"><span data-stu-id="979e7-p101">Check the **Restartable** property before using the **Requery** method on a **Recordset** object. If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="979e7-112">例</span><span class="sxs-lookup"><span data-stu-id="979e7-112">Example</span></span>

<span data-ttu-id="979e7-113">以下の例は、さまざまな **Recordset** オブジェクトの **Restartable** プロパティの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="979e7-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
