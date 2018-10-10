---
title: Database.PopulatePartial メソッド (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 11c999fcac3b77ddc4eeb9ef8f4414a5f8aa1559
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477136"
---
# <a name="databasepopulatepartial-method-dao"></a><span data-ttu-id="6681f-102">Database.PopulatePartial メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="6681f-102">Database.PopulatePartial Method (DAO)</span></span>


<span data-ttu-id="6681f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6681f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6681f-p101">部分レプリカ内の変更をフル レプリカと同期させ、部分レプリカ内のすべてのレコードを消去し、現在のレプリカ フィルターに基づいて部分レプリカのデータを再設定します (Microsoft Office Access データベース エンジンのデータベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="6681f-p101">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span>

## <a name="syntax"></a><span data-ttu-id="6681f-106">構文</span><span class="sxs-lookup"><span data-stu-id="6681f-106">Syntax</span></span>

<span data-ttu-id="6681f-107">*式*です。PopulatePartial (***DbPathName***)</span><span class="sxs-lookup"><span data-stu-id="6681f-107">*expression* .PopulatePartial(***DbPathName***)</span></span>

<span data-ttu-id="6681f-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6681f-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="6681f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6681f-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6681f-110">名前</span><span class="sxs-lookup"><span data-stu-id="6681f-110">Name</span></span></p></th>
<th><p><span data-ttu-id="6681f-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="6681f-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6681f-112">データ型</span><span class="sxs-lookup"><span data-stu-id="6681f-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="6681f-113">説明</span><span class="sxs-lookup"><span data-stu-id="6681f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6681f-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="6681f-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="6681f-115">必須</span><span class="sxs-lookup"><span data-stu-id="6681f-115">Required</span></span></p></td>
<td><p><span data-ttu-id="6681f-116"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6681f-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6681f-117">レコードの設定元となるフル レプリカのパスおよび名前。</span><span class="sxs-lookup"><span data-stu-id="6681f-117">The path and name of the full replica from which to populate records.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6681f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="6681f-118">Remarks</span></span>

<span data-ttu-id="6681f-119">部分レプリカとフル レプリカを同期させると、部分レプリカ内に "孤立化した" レコードが作成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="6681f-119">When you synchronize a partial replica with a full replica, it is possible to create "orphaned" records in the partial replica.</span></span> <span data-ttu-id="6681f-120">たとえばに、 **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** で、[得意先] テーブルがある場合」領域 = 'CA'"です。</span><span class="sxs-lookup"><span data-stu-id="6681f-120">For example, suppose you have a Customers table with its **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** set to "Region = 'CA'".</span></span> <span data-ttu-id="6681f-121">ユーザーが部分レプリカで得意先の地域を CA から NY に変更し、その後、 **[Synchronize](database-synchronize-method-dao.md)** メソッドを使用して同期が行われた場合、この変更がフル レプリカに反映されますが、部分レプリカ内で NY を持つレコードはレプリカのフィルター抽出条件に一致しなくなるため、孤立化します。</span><span class="sxs-lookup"><span data-stu-id="6681f-121">If a user changes a customer's region from CA to NY in the partial replica, and then a synchronization occurs via the **[Synchronize](database-synchronize-method-dao.md)** method, the change is propagated to the full replica but the record containing NY in the partial replica is orphaned because it now doesn't meet the replica filter criteria.</span></span>

<span data-ttu-id="6681f-p103">孤立化したレコードの問題を解決するには、 **PopulatePartial** メソッドを使用します。 **PopulatePartial** メソッドは **Synchronize** メソッドと似ていますが、すべての変更をフル レプリカと同期させ、部分レプリカ内のすべてのレコードを削除し、現在のレプリカ フィルターに基づいて部分レプリカを再設定します。レプリカ フィルターが変更されていない場合でも、 **PopulatePartial** は必ず部分レプリカ内のすべてのレコードを消去し、現在のフィルターに基づいて部分レプリカを再設定します。</span><span class="sxs-lookup"><span data-stu-id="6681f-p103">To solve the problem of orphaned records, you can use the **PopulatePartial** method. The **PopulatePartial** method is similar to the **Synchronize** method, but it synchronizes any changes with the full replica, removes all records in the partial replica, and then repopulates the partial replica based on the current replica filters. Even if your replica filters have not changed, **PopulatePartial** will always clear all records in the partial replica and repopulate it based on the current filters.</span></span>

<span data-ttu-id="6681f-p104">一般に、部分レプリカの作成時、およびレプリカ フィルターを変更したときは **PopulatePartial** メソッドを使用してください。アプリケーションでレプリカ フィルターを変更する場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6681f-p104">Generally, you should use the **PopulatePartial** method when you create a partial replica and whenever you change your replica filters. If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="6681f-127">フル レプリカと、フィルターが変更される部分レプリカを同期させます。</span><span class="sxs-lookup"><span data-stu-id="6681f-127">Synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="6681f-128">**ReplicaFilter** プロパティおよび **[PartialReplica](relation-partialreplica-property-dao.md)** プロパティを使用して、レプリカ フィルターに必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="6681f-128">Use the **ReplicaFilter** and **[PartialReplica](relation-partialreplica-property-dao.md)** properties to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="6681f-129">**PopulatePartial** メソッドを呼び出して、部分レプリカのすべてのレコードを削除し、新しいレプリカのフィルター抽出条件に一致するすべてのレコードをフル レプリカから送信します。</span><span class="sxs-lookup"><span data-stu-id="6681f-129">Call the **PopulatePartial** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="6681f-130">レプリカ フィルターが変更された場合、最初に **PopulatePartial** を呼び出さずに **Synchronize** メソッドが呼び出されると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6681f-130">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

<span data-ttu-id="6681f-p105">**PopulatePartial** メソッドは、排他的に開かれている部分レプリカでのみ呼び出すことができます。また、部分レプリカ内で実行しているコードから **PopulatePartial** メソッドを呼び出すことはできません。代わりに、フル レプリカまたは別のデータベースから部分レプリカを排他モードで開き、 **PopulatePartial** を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="6681f-p105">The **PopulatePartial** method can only be invoked on a partial replica that has been opened for exclusive access. Furthermore, you can't call the **PopulatePartial** method from code running within the partial replica itself. Instead, open the partial replica exclusively from the full replica or another database, then call **PopulatePartial**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6681f-p106">[!メモ] <STRONG>PopulatePartial</STRONG> は部分レプリカを消去して再設定する前に単方向の同期を行いますが、 <STRONG>PopulatePartial</STRONG> を呼び出す前に <STRONG>Synchronize</STRONG> を呼び出すことをお勧めします。 <STRONG>Synchronize</STRONG> の呼び出しが失敗した場合は、トラップ可能なエラーが発生するためです。このエラーを使用して、(部分レプリカのすべてのレコードを削除する) <STRONG>PopulatePartial</STRONG> メソッドを実行するかどうかを判断できます。 <STRONG>PopulatePartial</STRONG> が単独で呼び出された場合、レコードの同期中にエラーが発生したとしても、部分レプリカ内のレコードが削除されますが、これは目的の結果ではないことがあります。</span><span class="sxs-lookup"><span data-stu-id="6681f-p106">Although <STRONG>PopulatePartial</STRONG> performs a one-way synchronization before clearing and repopulating the partial replica, it is still a good idea to call <STRONG>Synchronize</STRONG> before calling <STRONG>PopulatePartial</STRONG>. This is because if the call to <STRONG>Synchronize</STRONG> fails, a trappable error occurs. You can use this error to decide whether or not to proceed with the <STRONG>PopulatePartial</STRONG> method (which removes all records in the partial replica). If <STRONG>PopulatePartial</STRONG> is called by itself and an error occurs while records are being synchronized, records in the partial replica will still be cleared, which may not be the desired result.</span></span></P>



## <a name="example"></a><span data-ttu-id="6681f-138">例</span><span class="sxs-lookup"><span data-stu-id="6681f-138">Example</span></span>

<span data-ttu-id="6681f-139">次の使用例では、レプリカ フィルターを変更した後で **PopulatePartial** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6681f-139">The following example uses the **PopulatePartial** method after changing a replica filter.</span></span>

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```
