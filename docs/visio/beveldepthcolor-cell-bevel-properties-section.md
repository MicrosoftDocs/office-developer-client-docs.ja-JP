---
title: '[BevelDepthColor] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1665774f-4049-4eda-ba7a-62314286699e
description: RGB 値として、またはアクティブなテーマでの面取りの奥行、色を決定します。
ms.openlocfilehash: b3b10ad220367a504a3df5c90453524a1c5fe59d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804813"
---
# <a name="beveldepthcolor-cell-bevel-properties-section"></a><span data-ttu-id="78180-103">[BevelDepthColor] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="78180-103">BevelDepthColor Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="78180-104">RGB 値として、またはアクティブなテーマでの面取りの奥行、色を決定します。</span><span class="sxs-lookup"><span data-stu-id="78180-104">Determines the color of the bevel's depth, as an RGB value or as determined by the active theme.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78180-105">備考</span><span class="sxs-lookup"><span data-stu-id="78180-105">Remarks</span></span>

<span data-ttu-id="78180-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelDepthColor** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="78180-106">To get a reference to the **BevelDepthColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="78180-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="78180-107">Cell name:</span></span>  <br/> | <span data-ttu-id="78180-108">BevelDepthColor</span><span class="sxs-lookup"><span data-stu-id="78180-108">BevelDepthColor</span></span>  <br/> |
   
<span data-ttu-id="78180-109">プログラムから、インデックスによって [ **BevelDepthColor** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="78180-109">To get a reference to the **BevelDepthColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="78180-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="78180-110">Section index:</span></span>  <br/> |<span data-ttu-id="78180-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="78180-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="78180-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="78180-112">Row index:</span></span>  <br/> |<span data-ttu-id="78180-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="78180-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="78180-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="78180-114">Cell index:</span></span>  <br/> |<span data-ttu-id="78180-115">**visBevelDepthColor**</span><span class="sxs-lookup"><span data-stu-id="78180-115">**visBevelDepthColor**</span></span> <br/> |
   
