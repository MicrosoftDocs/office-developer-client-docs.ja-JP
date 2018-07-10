---
title: '[FlipY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: 図形が上下反転されているかを示します。
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805398"
---
# <a name="flipy-cell-shape-transform-section"></a><span data-ttu-id="3439a-103">[FlipY] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="3439a-103">FlipY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="3439a-104">図形が上下反転されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="3439a-104">Indicates whether the shape has been flipped vertically.</span></span>
  
|<span data-ttu-id="3439a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3439a-105">**Value**</span></span>|<span data-ttu-id="3439a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3439a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3439a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3439a-107">TRUE</span></span>  <br/> | <span data-ttu-id="3439a-108">図形は上下反転されています。</span><span class="sxs-lookup"><span data-stu-id="3439a-108">The shape has been flipped vertically.</span></span>  <br/> |
| <span data-ttu-id="3439a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3439a-109">FALSE</span></span>  <br/> | <span data-ttu-id="3439a-110">図形は上下反転されていません。</span><span class="sxs-lookup"><span data-stu-id="3439a-110">The shape has not been flipped vertically.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3439a-111">備考</span><span class="sxs-lookup"><span data-stu-id="3439a-111">Remarks</span></span>

<span data-ttu-id="3439a-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [flipy] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3439a-112">To get a reference to the FlipY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3439a-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="3439a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3439a-114">[Flipy]</span><span class="sxs-lookup"><span data-stu-id="3439a-114">FlipY</span></span>  <br/> |
   
<span data-ttu-id="3439a-115">プログラムから、インデックスによって [flipy] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3439a-115">To get a reference to the FlipY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3439a-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3439a-116">Section index:</span></span>  <br/> |<span data-ttu-id="3439a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3439a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3439a-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3439a-118">Row index:</span></span>  <br/> |<span data-ttu-id="3439a-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="3439a-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="3439a-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3439a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3439a-121">**visXFormFlipY**</span><span class="sxs-lookup"><span data-stu-id="3439a-121">**visXFormFlipY**</span></span> <br/> |
   
