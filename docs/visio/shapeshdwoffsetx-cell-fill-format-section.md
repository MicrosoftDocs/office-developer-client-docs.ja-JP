---
title: '[ShapeShdwOffsetX] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60076
localization_priority: Normal
ms.assetid: a426f471-d35f-ef87-4c59-2c007ec2653f
description: 図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。
ms.openlocfilehash: 12512ce9edf49f91c786c3cd50baa8d07498a3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806429"
---
# <a name="shapeshdwoffsetx-cell-fill-format-section"></a><span data-ttu-id="6b697-103">[ShapeShdwOffsetX] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="6b697-103">ShapeShdwOffsetX Cell (Fill Format Section)</span></span>

<span data-ttu-id="6b697-104">図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="6b697-104">Determines the distance in page units that a shape's shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b697-105">注釈</span><span class="sxs-lookup"><span data-stu-id="6b697-105">Remarks</span></span>

<span data-ttu-id="6b697-106">この値は、[**影**] ダイアログ ボックスで設定する**X オフセット**の値に対応して ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="6b697-106">This value corresponds to the value in the **X Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="6b697-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeShdwOffsetX] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6b697-107">To get a reference to the ShapeShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b697-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="6b697-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6b697-109">ShapeShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="6b697-109">ShapeShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="6b697-110">プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b697-110">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b697-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6b697-111">Section index:</span></span>  <br/> |<span data-ttu-id="6b697-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b697-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b697-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6b697-113">Row index:</span></span>  <br/> |<span data-ttu-id="6b697-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="6b697-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="6b697-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6b697-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6b697-116">**visFillShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="6b697-116">**visFillShdwOffsetX**</span></span> <br/> |
   
