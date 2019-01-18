---
title: Recordset2.Bookmarkable プロパティ (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26b8b60255b4e50a2288dedb8e27906476926e8c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714683"
---
# <a name="recordset2bookmarkable-property-dao"></a><span data-ttu-id="e1e6a-102">Recordset2.Bookmarkable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1e6a-102">Recordset2.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="e1e6a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1e6a-104">**Recordset** オブジェクトがブックマークをサポートしているかどうかを示す、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを使用して設定できる値を返します。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e6a-105">構文</span><span class="sxs-lookup"><span data-stu-id="e1e6a-105">Syntax</span></span>

<span data-ttu-id="e1e6a-106">*式*です。ブックマークを設定</span><span class="sxs-lookup"><span data-stu-id="e1e6a-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="e1e6a-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1e6a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e1e6a-108">Remarks</span></span>

<span data-ttu-id="e1e6a-109">**Bookmark** プロパティを設定または確認しようとする前に、 **Recordset** オブジェクトの **Bookmarkable** プロパティの設定値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="e1e6a-110">Microsoft Access データベース エンジンのテーブルに基づく**Recordset**オブジェクトの**Bookmarkable**プロパティの値は、true の場合、およびブックマークを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="e1e6a-111">ただし、その他のデータベース製品では、ブックマークがサポートされていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="e1e6a-112">たとえば、主キーがない Paradox リンク テーブルを基にした **Recordset** オブジェクトでブックマークを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="e1e6a-113">例</span><span class="sxs-lookup"><span data-stu-id="e1e6a-113">Example</span></span>

<span data-ttu-id="e1e6a-114">この例では、 **Bookmark** プロパティおよび **Bookmarkable** プロパティを使用して、ユーザーがレコードセット内のレコードにフラグを設定し、後でそのレコードに戻ることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="e1e6a-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
