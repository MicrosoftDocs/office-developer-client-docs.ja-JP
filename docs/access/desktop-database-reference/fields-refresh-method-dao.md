---
title: Fields.Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 138679acb9b0cec737d17d613f26efd1347ffd99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477724"
---
# <a name="fieldsrefresh-method-dao"></a><span data-ttu-id="a9d5a-102">Fields.Refresh メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9d5a-102">Fields.Refresh Method (DAO)</span></span>


<span data-ttu-id="a9d5a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9d5a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a9d5a-104">指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。</span><span class="sxs-lookup"><span data-stu-id="a9d5a-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d5a-105">構文</span><span class="sxs-lookup"><span data-stu-id="a9d5a-105">Syntax</span></span>

<span data-ttu-id="a9d5a-106">*式*です。更新</span><span class="sxs-lookup"><span data-stu-id="a9d5a-106">*expression* .Refresh</span></span>

<span data-ttu-id="a9d5a-107">\*式\***Fields**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a9d5a-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d5a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="a9d5a-108">Remarks</span></span>

<span data-ttu-id="a9d5a-p101">Microsoft Access データベース エンジンで **QueryDef**、 **Recordset**、または **TableDef** の各オブジェクトの **Fields** コレクションに含まれる **Field** オブジェクトに使用される場所を確認するには、各 **Field** オブジェクトの **OrdinalPosition** プロパティを使用します。 **Field** オブジェクトの **OrdinalPosition** プロパティを変更しても、 **Refresh** メソッドを使用しない限り、コレクションにおける **Field** オブジェクトの順序は変化しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9d5a-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="a9d5a-p102">**Refresh** メソッドは、マルチユーザー環境で、他のユーザーがデータベースを変更する可能性がある場合に使用します。このメソッドは、データベースに対する変更によって間接的に影響を受けるコレクションでも使用する必要がある場合があります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に、その **Groups** コレクションを変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9d5a-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="a9d5a-p103">コレクションのオブジェクトはそのコレクションが最初に参照されたときに設定され、それ以降に他のユーザーが行った変更は自動的には反映されません。他のユーザーがコレクションを変更した可能性がある場合は、コレクション内に特定のオブジェクトが存在する (または存在しない) ことを前提とするタスクをアプリケーションで実行する直前に、コレクションの Refresh メソッドを使用してください。これにより、そのコレクションを最新の状態にしておくことができます。一方で、Refresh を使用すると、パフォーマンスが大幅に低下する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9d5a-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

## <a name="example"></a><span data-ttu-id="a9d5a-118">例</span><span class="sxs-lookup"><span data-stu-id="a9d5a-118">Example</span></span>

<span data-ttu-id="a9d5a-p104">**Refresh** メソッドの次の使用例では、 **OrdinalPosition** データへの変更に基づいて、[商品区分] テーブルの **Fields** コレクションを更新します。コレクションにおける **Fields** オブジェクトの順序は、 **Refresh** メソッドの使用後に初めて変化します。</span><span class="sxs-lookup"><span data-stu-id="a9d5a-p104">This example uses the **Refresh** method to update the **Fields** collection of the Categories table based on changes to the **OrdinalPosition** data. The order of the **Fields** in the collection changes only after the **Refresh** method is used.</span></span>

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
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
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```