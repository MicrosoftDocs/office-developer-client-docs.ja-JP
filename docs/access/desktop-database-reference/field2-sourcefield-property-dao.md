---
title: Field2.SourceField プロパティ (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09351acfea263c41bd9cb7f857139dfacf359421
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477857"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="c6ee1-102">Field2.SourceField プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6ee1-102">Field2.SourceField Property (DAO)</span></span>


<span data-ttu-id="c6ee1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6ee1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6ee1-p101">**Field2** オブジェクトのデータの元のソースであるフィールドの名前を示す値を返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ee1-106">構文</span><span class="sxs-lookup"><span data-stu-id="c6ee1-106">Syntax</span></span>

<span data-ttu-id="c6ee1-107">*式*です。SourceField</span><span class="sxs-lookup"><span data-stu-id="c6ee1-107">*expression* .SourceField</span></span>

<span data-ttu-id="c6ee1-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ee1-109">注釈</span><span class="sxs-lookup"><span data-stu-id="c6ee1-109">Remarks</span></span>

<span data-ttu-id="c6ee1-110">**Field2** オブジェクトでは、 **SourceField** プロパティと **SourceTable** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6ee1-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="c6ee1-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="c6ee1-112">使用例</span><span class="sxs-lookup"><span data-stu-id="c6ee1-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6ee1-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="c6ee1-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="c6ee1-114">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6ee1-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="c6ee1-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c6ee1-116">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6ee1-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c6ee1-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="c6ee1-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6ee1-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="c6ee1-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="c6ee1-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6ee1-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c6ee1-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c6ee1-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6ee1-p102">これらのプロパティは、 **Field2** オブジェクトに関連付けられた元のフィールドおよびテーブル名を示します。たとえば、これらのプロパティを使用して、クエリ フィールド内の、基になるテーブルのフィールド名に無関係な名前を持つデータの、元のソースを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="c6ee1-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>
