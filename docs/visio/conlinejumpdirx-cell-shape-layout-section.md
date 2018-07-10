---
title: '[ConLineJumpDirX] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: 図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805081"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="d4e07-103">[ConLineJumpDirX] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="d4e07-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="d4e07-104">図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4e07-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="d4e07-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d4e07-105">**Value**</span></span>|<span data-ttu-id="d4e07-106">**線の飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="d4e07-106">**Line jump direction**</span></span>|<span data-ttu-id="d4e07-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="d4e07-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d4e07-108">0</span><span class="sxs-lookup"><span data-stu-id="d4e07-108">0</span></span>  <br/> | <span data-ttu-id="d4e07-109">ページの既定値</span><span class="sxs-lookup"><span data-stu-id="d4e07-109">Page default</span></span>  <br/> |<span data-ttu-id="d4e07-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="d4e07-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="d4e07-111">1</span><span class="sxs-lookup"><span data-stu-id="d4e07-111">1</span></span>  <br/> | <span data-ttu-id="d4e07-112">上</span><span class="sxs-lookup"><span data-stu-id="d4e07-112">Up</span></span>  <br/> |<span data-ttu-id="d4e07-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="d4e07-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="d4e07-114">2</span><span class="sxs-lookup"><span data-stu-id="d4e07-114">2</span></span>  <br/> | <span data-ttu-id="d4e07-115">下</span><span class="sxs-lookup"><span data-stu-id="d4e07-115">Down</span></span>  <br/> |<span data-ttu-id="d4e07-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="d4e07-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4e07-117">備考</span><span class="sxs-lookup"><span data-stu-id="d4e07-117">Remarks</span></span>

<span data-ttu-id="d4e07-118">ページにジャンプする*すべて*のコネクタの水平方向のデフォルトを設定するのには、PageLineJumpDirX セルを使用して、「ページ レイアウト」セクションでします。</span><span class="sxs-lookup"><span data-stu-id="d4e07-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="d4e07-119">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ConLineJumpDirX] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d4e07-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4e07-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="d4e07-120">Cell name:</span></span>  <br/> | <span data-ttu-id="d4e07-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="d4e07-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="d4e07-122">プログラムから、インデックスによって [ConLineJumpDirX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d4e07-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4e07-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4e07-123">Section index:</span></span>  <br/> |<span data-ttu-id="d4e07-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4e07-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d4e07-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4e07-125">Row index:</span></span>  <br/> |<span data-ttu-id="d4e07-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="d4e07-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="d4e07-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4e07-127">Cell index:</span></span>  <br/> |<span data-ttu-id="d4e07-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="d4e07-128">**visSLOJumpDirX**</span></span> <br/> |
   
