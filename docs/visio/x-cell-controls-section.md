---
title: '[X] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: X を表す-座標をローカル座標にある図形のコントロール ハンドルの位置を示します。
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806810"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="ea3bd-103">[X] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="ea3bd-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="ea3bd-104">*X*を表す-座標をローカル座標にある図形のコントロール ハンドルの位置を示します。</span><span class="sxs-lookup"><span data-stu-id="ea3bd-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ea3bd-105">備考</span><span class="sxs-lookup"><span data-stu-id="ea3bd-105">Remarks</span></span>

<span data-ttu-id="ea3bd-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ea3bd-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea3bd-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="ea3bd-107">Cell name:</span></span>  <br/> | <span data-ttu-id="ea3bd-108">制御します。</span><span class="sxs-lookup"><span data-stu-id="ea3bd-108">Controls.</span></span>  <span data-ttu-id="ea3bd-109">*名*です。X を制御します。</span><span class="sxs-lookup"><span data-stu-id="ea3bd-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="ea3bd-110">*名*は、コントロールの行の名前です。</span><span class="sxs-lookup"><span data-stu-id="ea3bd-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="ea3bd-111">プログラムから、インデックスによって [X] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea3bd-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea3bd-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea3bd-112">Section index:</span></span>  <br/> |<span data-ttu-id="ea3bd-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="ea3bd-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="ea3bd-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea3bd-114">Row index:</span></span>  <br/> |<span data-ttu-id="ea3bd-115">**visRowControl** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="ea3bd-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ea3bd-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea3bd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ea3bd-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="ea3bd-117">**visCtlX**</span></span> <br/> |
   
