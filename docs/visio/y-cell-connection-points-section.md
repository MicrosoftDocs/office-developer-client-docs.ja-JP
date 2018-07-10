---
title: '[Y] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Y を表す-ローカル座標での接続ポイントの座標です。
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806819"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="70cdd-103">[Y] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="70cdd-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="70cdd-104">*Y*を表す-ローカル座標での接続ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="70cdd-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="70cdd-105">備考</span><span class="sxs-lookup"><span data-stu-id="70cdd-105">Remarks</span></span>

<span data-ttu-id="70cdd-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="70cdd-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70cdd-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="70cdd-107">Cell name:</span></span>  <br/> | <span data-ttu-id="70cdd-108">Connections.Y *i* 、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="70cdd-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="70cdd-109">プログラムから、インデックスによって [Y] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="70cdd-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70cdd-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="70cdd-110">Section index:</span></span>  <br/> |<span data-ttu-id="70cdd-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="70cdd-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="70cdd-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="70cdd-112">Row index:</span></span>  <br/> |<span data-ttu-id="70cdd-113">**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="70cdd-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="70cdd-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="70cdd-114">Cell index:</span></span>  <br/> |<span data-ttu-id="70cdd-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="70cdd-115">**visY**</span></span> <br/> |
   
