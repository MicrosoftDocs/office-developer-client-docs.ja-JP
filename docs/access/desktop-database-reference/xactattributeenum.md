---
title: XactAttributeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a44546a63583a03bd40b9e86405c3d560b3a94e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478898"
---
# <a name="xactattributeenum"></a><span data-ttu-id="750d5-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="750d5-102">XactAttributeEnum</span></span>


<span data-ttu-id="750d5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="750d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="750d5-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="750d5-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750d5-105">定数</span><span class="sxs-lookup"><span data-stu-id="750d5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="750d5-106">値</span><span class="sxs-lookup"><span data-stu-id="750d5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="750d5-107">説明</span><span class="sxs-lookup"><span data-stu-id="750d5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750d5-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="750d5-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="750d5-109">262144</span><span class="sxs-lookup"><span data-stu-id="750d5-109">262144</span></span></p></td>
<td><p><span data-ttu-id="750d5-p101">保持中止を実行します (つまり、<a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> を呼び出すと、自動的に新規トランザクションが開始されます)。この設定をサポートしていないプロバイダーもあります。</span><span class="sxs-lookup"><span data-stu-id="750d5-p101">Performs retaining aborts — that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction. Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d5-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="750d5-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="750d5-113">131072</span><span class="sxs-lookup"><span data-stu-id="750d5-113">131072</span></span></p></td>
<td><p><span data-ttu-id="750d5-p102">保持コミットを実行します (つまり、<a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> を呼び出すと、自動的に新規トランザクションが開始されます)。この設定をサポートしていないプロバイダーもあります。</span><span class="sxs-lookup"><span data-stu-id="750d5-p102">Performs retaining commits — that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction. Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="750d5-116">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="750d5-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="750d5-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="750d5-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750d5-118">定数</span><span class="sxs-lookup"><span data-stu-id="750d5-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750d5-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="750d5-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750d5-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="750d5-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>
