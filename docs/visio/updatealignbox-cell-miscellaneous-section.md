---
title: '[UpdateAlignBox] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1085
localization_priority: Normal
ms.assetid: 3e3f8dc9-203f-447d-9674-eb0be2d557d1
description: コントロール ハンドルを移動するたびに選択範囲を再計算します。
ms.openlocfilehash: 837c25a2d4993f91a16cc4e292f34a94b00040c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806724"
---
# <a name="updatealignbox-cell-miscellaneous-section"></a><span data-ttu-id="bfb66-103">[UpdateAlignBox] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="bfb66-103">UpdateAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="bfb66-104">コントロール ハンドルを移動するたびに選択範囲を再計算します。</span><span class="sxs-lookup"><span data-stu-id="bfb66-104">Recalculates the selection rectangle whenever a control handle is moved.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfb66-105">備考</span><span class="sxs-lookup"><span data-stu-id="bfb66-105">Remarks</span></span>

<span data-ttu-id="bfb66-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[UpdateAlignBox] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="bfb66-106">To get a reference to the UpdateAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bfb66-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="bfb66-107">Cell name:</span></span>  <br/> | <span data-ttu-id="bfb66-108">UpdateAlignBox</span><span class="sxs-lookup"><span data-stu-id="bfb66-108">UpdateAlignBox</span></span>  <br/> |
   
<span data-ttu-id="bfb66-109">プログラムから、インデックスによって [UpdateAlignBox] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bfb66-109">To get a reference to the UpdateAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bfb66-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfb66-110">Section index:</span></span>  <br/> |<span data-ttu-id="bfb66-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bfb66-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bfb66-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfb66-112">Row index:</span></span>  <br/> |<span data-ttu-id="bfb66-113">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="bfb66-113">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="bfb66-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bfb66-114">Cell index:</span></span>  <br/> |<span data-ttu-id="bfb66-115">**visUpdateAlignBox**</span><span class="sxs-lookup"><span data-stu-id="bfb66-115">**visUpdateAlignBox**</span></span> <br/> |
   
