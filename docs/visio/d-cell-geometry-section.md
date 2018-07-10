---
title: '[D] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: 各行に対応する情報を表示します。次の表に、各行で [D] セルが示す内容を説明します。
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805140"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="51bc0-104">[D] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="51bc0-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="51bc0-p102">各行に対応する情報を表示します。次の表に、各行で [D] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="51bc0-p102">Represents different information in different rows. This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="51bc0-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="51bc0-107">**Row**</span></span>|<span data-ttu-id="51bc0-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="51bc0-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51bc0-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="51bc0-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="51bc0-p103">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="51bc0-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|<span data-ttu-id="51bc0-113">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="51bc0-113">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="51bc0-114">NURBS (nonuniform rational B-spline) の最初の太さです。</span><span class="sxs-lookup"><span data-stu-id="51bc0-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="51bc0-115">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="51bc0-115">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="51bc0-116">スプラインの角度 (1 ～ 25 の整数) です。</span><span class="sxs-lookup"><span data-stu-id="51bc0-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="51bc0-117">楕円</span><span class="sxs-lookup"><span data-stu-id="51bc0-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="51bc0-118">*Y* -楕円上の点の座標対応する*x*の座標は、[ [C](c-cell-geometry-section.md) ] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="51bc0-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51bc0-119">備考</span><span class="sxs-lookup"><span data-stu-id="51bc0-119">Remarks</span></span>

<span data-ttu-id="51bc0-120">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="51bc0-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51bc0-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="51bc0-121">Cell name:</span></span>  <br/> | <span data-ttu-id="51bc0-122">ジオメトリの*i*です。D *j* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="51bc0-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="51bc0-123">ジオメトリの*i*です。D1 ([Ellipse] 行)、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="51bc0-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="51bc0-124">プログラムから、インデックスによって [D] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="51bc0-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51bc0-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="51bc0-125">Section index:</span></span>  <br/> |<span data-ttu-id="51bc0-126">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="51bc0-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="51bc0-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="51bc0-127">Row index:</span></span>  <br/> |<span data-ttu-id="51bc0-128">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="51bc0-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="51bc0-129">**visRowVertex**([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="51bc0-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="51bc0-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="51bc0-130">Cell index</span></span>  <br/> |<span data-ttu-id="51bc0-131">**visAspectRatio**(EllipticalArcTo 行)</span><span class="sxs-lookup"><span data-stu-id="51bc0-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="51bc0-132">**visNURBSWeightPrev**([Nurbsto] 行)</span><span class="sxs-lookup"><span data-stu-id="51bc0-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="51bc0-133">**visSplineDegree**([A 行)</span><span class="sxs-lookup"><span data-stu-id="51bc0-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="51bc0-134">**visEllipseMinorY**([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="51bc0-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   
