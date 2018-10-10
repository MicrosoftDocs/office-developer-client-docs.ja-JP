---
title: Field.SourceField プロパティ (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 729a858ae39c6403d8ccefcacaa7bade754f0484
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477623"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="fc04c-102">Field.SourceField プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc04c-102">Field.SourceField Property (DAO)</span></span>


<span data-ttu-id="fc04c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc04c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc04c-p101">**Field** オブジェクトの元のデータ ソースであるフィールド名を示す値を取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc04c-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc04c-106">構文</span><span class="sxs-lookup"><span data-stu-id="fc04c-106">Syntax</span></span>

<span data-ttu-id="fc04c-107">*式*です。SourceField</span><span class="sxs-lookup"><span data-stu-id="fc04c-107">*expression* .SourceField</span></span>

<span data-ttu-id="fc04c-108">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="fc04c-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc04c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="fc04c-109">Remarks</span></span>

<span data-ttu-id="fc04c-110">**Field** オブジェクトでは、 **SourceField** プロパティおよび **SourceTable** プロパティの使用方法は、次の表に示すように、 **Field** オブジェクトを追加する **Fields** コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="fc04c-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc04c-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="fc04c-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="fc04c-112">使用例</span><span class="sxs-lookup"><span data-stu-id="fc04c-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc04c-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="fc04c-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="fc04c-114">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="fc04c-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc04c-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="fc04c-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="fc04c-116">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fc04c-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc04c-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="fc04c-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="fc04c-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fc04c-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc04c-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="fc04c-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="fc04c-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="fc04c-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc04c-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="fc04c-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="fc04c-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fc04c-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc04c-p102">これらのプロパティは、 **Field** オブジェクトに関連付けられている元のフィールドおよびテーブルの名前を示します。たとえば、これらのプロパティを使用すると、クエリ フィールドの元のデータ ソースの名前と基になるテーブルのフィールドの名前に関連性がない場合でも、そのデータ ソースを特定できます。</span><span class="sxs-lookup"><span data-stu-id="fc04c-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>
