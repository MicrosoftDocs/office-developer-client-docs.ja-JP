---
title: AllowNullsEnum (デスクトップ データベース参照のアクセス)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04e67584e0f0c2eeb5a12e34fdf98a84cc1da852
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477884"
---
# <a name="allownullsenum"></a><span data-ttu-id="0d2e4-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="0d2e4-102">AllowNullsEnum</span></span>


<span data-ttu-id="0d2e4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d2e4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0d2e4-104">Null 値を含むレコードにインデックスを付けるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0d2e4-104">Specifies whether records with null values are indexed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d2e4-105">定数</span><span class="sxs-lookup"><span data-stu-id="0d2e4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0d2e4-106">値</span><span class="sxs-lookup"><span data-stu-id="0d2e4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0d2e4-107">説明</span><span class="sxs-lookup"><span data-stu-id="0d2e4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d2e4-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="0d2e4-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2e4-109">0</span><span class="sxs-lookup"><span data-stu-id="0d2e4-109">0</span></span></p></td>
<td><p><span data-ttu-id="0d2e4-p101">インデックスは、キー列が Null 値のエントリを許可します。Null 値がキー列に入力された場合、そのエントリはインデックスに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="0d2e4-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d2e4-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="0d2e4-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2e4-113">1</span><span class="sxs-lookup"><span data-stu-id="0d2e4-113">1</span></span></p></td>
<td><p><span data-ttu-id="0d2e4-p102">既定値です。インデックスは、キー列が Null 値のエントリを許可しません。Null 値がキー列に入力された場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0d2e4-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d2e4-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="0d2e4-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2e4-118">2</span><span class="sxs-lookup"><span data-stu-id="0d2e4-118">2</span></span></p></td>
<td><p><span data-ttu-id="0d2e4-p103">インデックスは、Null 値のキーを含むエントリを挿入しません。Null 値がキー列に入力された場合、そのエントリは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="0d2e4-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d2e4-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="0d2e4-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="0d2e4-122">4</span><span class="sxs-lookup"><span data-stu-id="0d2e4-122">4</span></span></p></td>
<td><p><span data-ttu-id="0d2e4-p104">インデックスは、キー列に Null 値を含むエントリを挿入しません。複数列キーを持つインデックスでは、Null 値が入力された列がある場合、そのエントリは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="0d2e4-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>
