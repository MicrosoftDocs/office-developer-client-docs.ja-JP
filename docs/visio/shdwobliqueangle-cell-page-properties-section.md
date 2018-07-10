---
title: '[ShdwObliqueAngle] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: 既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806474"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="7b30f-103">[ShdwObliqueAngle] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="7b30f-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="7b30f-104">既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b30f-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b30f-105">備考</span><span class="sxs-lookup"><span data-stu-id="7b30f-105">Remarks</span></span>

<span data-ttu-id="7b30f-106">このセルの値がゼロ (0) の場合は影の傾きの角度が真上で、時計回りに角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b30f-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="7b30f-107">ShapeShdwType セル (ページ上の図形の影の種類) がページの既定値 (**visFSTPageDefault** ) に設定し、影の種類は、斜体にするたびに、このセルに記載されている角度が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b30f-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="7b30f-108">既定ページの影の種類は、[shdwtype] セルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="7b30f-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="7b30f-109">個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwObliqueAngle] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b30f-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="7b30f-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwObliqueAngle] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7b30f-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b30f-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7b30f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7b30f-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="7b30f-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="7b30f-113">プログラムから、インデックスによって [ShdwObliqueAngle] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b30f-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b30f-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7b30f-114">Section index:</span></span>  <br/> |<span data-ttu-id="7b30f-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b30f-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7b30f-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7b30f-116">Row index:</span></span>  <br/> |<span data-ttu-id="7b30f-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="7b30f-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="7b30f-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7b30f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7b30f-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="7b30f-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   
