---
title: InheritTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706808"
---
# <a name="inherittypeenum"></a><span data-ttu-id="eccfb-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="eccfb-102">InheritTypeEnum</span></span>

<span data-ttu-id="eccfb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="eccfb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eccfb-104">[SetPermissions](setpermissions-method-adox.md) メソッドで設定された権限をオブジェクトが継承する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="eccfb-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eccfb-105">定数</span><span class="sxs-lookup"><span data-stu-id="eccfb-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="eccfb-106">値</span><span class="sxs-lookup"><span data-stu-id="eccfb-106">Value</span></span></p></th>
<th><p><span data-ttu-id="eccfb-107">説明</span><span class="sxs-lookup"><span data-stu-id="eccfb-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eccfb-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="eccfb-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="eccfb-109">3</span><span class="sxs-lookup"><span data-stu-id="eccfb-109">3</span></span></p></td>
<td><p><span data-ttu-id="eccfb-110">主オブジェクトに含まれるオブジェクトおよびその他のコンテナーの両方が、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="eccfb-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eccfb-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="eccfb-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="eccfb-112">2</span><span class="sxs-lookup"><span data-stu-id="eccfb-112">2</span></span></p></td>
<td><p><span data-ttu-id="eccfb-113">主オブジェクトに含まれるその他のコンテナーが、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="eccfb-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eccfb-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="eccfb-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="eccfb-115">0</span><span class="sxs-lookup"><span data-stu-id="eccfb-115">0</span></span></p></td>
<td><p><span data-ttu-id="eccfb-p101">既定値です。継承は行われません。</span><span class="sxs-lookup"><span data-stu-id="eccfb-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eccfb-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="eccfb-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="eccfb-119">4</span><span class="sxs-lookup"><span data-stu-id="eccfb-119">4</span></span></p></td>
<td><p><span data-ttu-id="eccfb-120"><strong>adInheritObjects</strong> フラグおよび <strong>adInheritContainers</strong> フラグは、継承されたエントリに伝えられません。</span><span class="sxs-lookup"><span data-stu-id="eccfb-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eccfb-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="eccfb-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="eccfb-122">1</span><span class="sxs-lookup"><span data-stu-id="eccfb-122">1</span></span></p></td>
<td><p><span data-ttu-id="eccfb-123">コンテナー内のコンテナー以外のオブジェクトが、権限を継承します。</span><span class="sxs-lookup"><span data-stu-id="eccfb-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

