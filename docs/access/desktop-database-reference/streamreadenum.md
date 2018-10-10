---
title: StreamReadEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1255f691f2cd0bde1e3ed83ebffc1f0d31fb3119
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478254"
---
# <a name="streamreadenum"></a><span data-ttu-id="5e385-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="5e385-102">StreamReadEnum</span></span>


<span data-ttu-id="5e385-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e385-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5e385-104">[Stream](stream-object-ado.md) オブジェクトから、ストリーム全体を読み取るか、または次の行を読み取るかを表します。</span><span class="sxs-lookup"><span data-stu-id="5e385-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e385-105">定数</span><span class="sxs-lookup"><span data-stu-id="5e385-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5e385-106">値</span><span class="sxs-lookup"><span data-stu-id="5e385-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5e385-107">説明</span><span class="sxs-lookup"><span data-stu-id="5e385-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e385-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="5e385-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="5e385-109">-1</span><span class="sxs-lookup"><span data-stu-id="5e385-109">-1</span></span></p></td>
<td><p><span data-ttu-id="5e385-p101">既定値。現在の位置から <a href="eos-property-ado.md">EOS</a> マーカー方向に、すべてのバイトをストリームから読み取ります。これは、バイナリ ストリーム (<a href="type-property-ado-stream.md">Type</a> は <strong>adTypeBinary</strong>) に唯一有効な <strong>StreamReadEnum</strong> 値です。</span><span class="sxs-lookup"><span data-stu-id="5e385-p101">Default. Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker. This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e385-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="5e385-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="5e385-114">-2</span><span class="sxs-lookup"><span data-stu-id="5e385-114">-2</span></span></p></td>
<td><p><span data-ttu-id="5e385-115">ストリームから次の行を読み取ります  (<a href="lineseparator-property-ado.md">LineSeparator</a> プロパティで指定)。</span><span class="sxs-lookup"><span data-stu-id="5e385-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e385-116">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="5e385-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="5e385-117">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="5e385-117">These constants do not have ADO/WFC equivalents.</span></span>
