---
title: '[Sharpen] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: ビットマップ イメージを鮮明にします。既定値は 0% です。イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。
ms.openlocfilehash: fbc66f8c88cde67ad1f259f8392f6d3bd0457be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806445"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="45102-105">[Sharpen] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="45102-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="45102-p102">ビットマップ イメージを鮮明にします。既定値は 0% です。イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。</span><span class="sxs-lookup"><span data-stu-id="45102-p102">Sharpens a bitmap image. The default value is 0%. Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45102-109">備考</span><span class="sxs-lookup"><span data-stu-id="45102-109">Remarks</span></span>

<span data-ttu-id="45102-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって sharpen] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="45102-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45102-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="45102-111">Cell name:</span></span>  <br/> | <span data-ttu-id="45102-112">Sharpen</span><span class="sxs-lookup"><span data-stu-id="45102-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="45102-113">プログラムから、インデックスによって [sharpen] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="45102-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45102-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="45102-114">Section index:</span></span>  <br/> |<span data-ttu-id="45102-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="45102-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="45102-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="45102-116">Row index:</span></span>  <br/> |<span data-ttu-id="45102-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="45102-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="45102-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="45102-118">Cell index:</span></span>  <br/> |<span data-ttu-id="45102-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="45102-119">**visImageSharpen**</span></span> <br/> |
   
