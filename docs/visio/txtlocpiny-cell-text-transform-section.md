---
title: '[TxtLocPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: Y が決まりますが、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。 既定の数式は次のとおりです。
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806699"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="231b5-104">[TxtLocPinY] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="231b5-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="231b5-105">*Y*が決まりますが、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。</span><span class="sxs-lookup"><span data-stu-id="231b5-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="231b5-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="231b5-106">The default formula is:</span></span> 
  
<span data-ttu-id="231b5-107">= [Txtheight] \* 0.5</span><span class="sxs-lookup"><span data-stu-id="231b5-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="231b5-108">備考</span><span class="sxs-lookup"><span data-stu-id="231b5-108">Remarks</span></span>

<span data-ttu-id="231b5-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって TxtLocPinY] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="231b5-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="231b5-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="231b5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="231b5-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="231b5-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="231b5-112">プログラムから、インデックスによって [TxtLocPinY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="231b5-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="231b5-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="231b5-113">Section index:</span></span>  <br/> |<span data-ttu-id="231b5-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="231b5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="231b5-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="231b5-115">Row index:</span></span>  <br/> |<span data-ttu-id="231b5-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="231b5-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="231b5-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="231b5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="231b5-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="231b5-118">**visXFormLocPinY**</span></span> <br/> |
   
