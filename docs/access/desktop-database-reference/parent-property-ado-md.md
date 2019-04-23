---
title: Parent プロパティ (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287791"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="9bd6d-102">Parent プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9bd6d-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="9bd6d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bd6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bd6d-104">階層内の現在のメンバーの親であるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="9bd6d-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="9bd6d-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="9bd6d-105">Return values</span></span>

<span data-ttu-id="9bd6d-106">[Member](member-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="9bd6d-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bd6d-107">注釈</span><span class="sxs-lookup"><span data-stu-id="9bd6d-107">Remarks</span></span>

<span data-ttu-id="9bd6d-p101">階層の最上位レベル (ルート) にあるメンバーには、親はありません。このプロパティは、[Level](level-object-ado-md.md) オブジェクトに属する **Member** オブジェクトでのみサポートされます。[Position](position-object-ado-md.md) オブジェクトに属する **Member** オブジェクトからこのプロパティが参照されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9bd6d-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

