---
title: '[SortKey] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: このセルの値は文字列として扱われ、評価されます。この値に基づいて、[図形データ] ウィンドウ内にある項目を一覧表示するための順序が決まります。
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417855"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="c9e4b-103">[SortKey] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="c9e4b-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="c9e4b-104">このセルの値は文字列として扱われ、評価されます。この値に基づいて、[**図形データ**] ウィンドウ内にある項目を一覧表示するための順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9e4b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="c9e4b-105">Remarks</span></span>

<span data-ttu-id="c9e4b-106">[SortKey] の値を比較するときに使用される計算方法は、ロケールに固有のもので、大文字と小文字は区別されます。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="c9e4b-107">[SortKey] の値が等しい場合は、図形データは行の順序に基づいて一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="c9e4b-108">並べ替えキーを持たない図形データは、並べ替えキーを含む図形データの後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="c9e4b-109">並べ替えキーを使用して、[**図形データ**] ウィンドウに、項目番号、数量、および価格の順序で図形データを表示する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="c9e4b-110">*行、ラベル、* および*SortKey*は、図形データ行のセルを参照します。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="c9e4b-111">この例では、図形データ行に名前が付けられています。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="c9e4b-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="c9e4b-112">**Row**</span></span>|<span data-ttu-id="c9e4b-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="c9e4b-113">**Label**</span></span>|<span data-ttu-id="c9e4b-114">**[sortkey]**</span><span class="sxs-lookup"><span data-stu-id="c9e4b-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c9e4b-115">Prop. アイテム</span><span class="sxs-lookup"><span data-stu-id="c9e4b-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="c9e4b-116">項目番号</span><span class="sxs-lookup"><span data-stu-id="c9e4b-116">Item Number</span></span>  <br/> | <span data-ttu-id="c9e4b-117">1 </span><span class="sxs-lookup"><span data-stu-id="c9e4b-117">1</span></span>  <br/> |
| <span data-ttu-id="c9e4b-118">Prop</span><span class="sxs-lookup"><span data-stu-id="c9e4b-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="c9e4b-119">Price</span><span class="sxs-lookup"><span data-stu-id="c9e4b-119">Price</span></span>  <br/> | <span data-ttu-id="c9e4b-120">3 </span><span class="sxs-lookup"><span data-stu-id="c9e4b-120">3</span></span>  <br/> |
| <span data-ttu-id="c9e4b-121">Prop</span><span class="sxs-lookup"><span data-stu-id="c9e4b-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="c9e4b-122">数量</span><span class="sxs-lookup"><span data-stu-id="c9e4b-122">Quantity</span></span>  <br/> | <span data-ttu-id="c9e4b-123">2 </span><span class="sxs-lookup"><span data-stu-id="c9e4b-123">2</span></span>  <br/> |
   
<span data-ttu-id="c9e4b-124">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SortKey] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9e4b-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="c9e4b-125">Cell name:</span></span>  <br/> | <span data-ttu-id="c9e4b-126">提案. *名前*です。SortKey (Prop) *name*はカスタムプロパティ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="c9e4b-127">プログラムから、インデックスによって [SortKey] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9e4b-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9e4b-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9e4b-128">Section index:</span></span>  <br/> |<span data-ttu-id="c9e4b-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="c9e4b-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="c9e4b-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9e4b-130">Row index:</span></span>  <br/> |<span data-ttu-id="c9e4b-131">**visRowProp** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="c9e4b-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c9e4b-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9e4b-132">Cell index:</span></span>  <br/> |<span data-ttu-id="c9e4b-133">**viscustpropssortkey**</span><span class="sxs-lookup"><span data-stu-id="c9e4b-133">**visCustPropsSortKey**</span></span> <br/> |
   

