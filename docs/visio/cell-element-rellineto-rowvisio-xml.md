---
title: セル要素 (RelLineTo 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 44d369f0-ab37-75ca-727e-b421d6f95ba7
description: 含まれている x、または図形の幅と高さを基準にして、直線の線分の終点の y 座標。
ms.openlocfilehash: 73930b15a62a483b38da4791511f735ac81bb1a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804989"
---
# <a name="cell-element-rellineto-row-visio-xml"></a><span data-ttu-id="dafcf-103">セル要素 (RelLineTo 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="dafcf-103">Cell element (RelLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="dafcf-104">含まれている x、または図形の幅と高さを基準にして、直線の線分の終点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="dafcf-104">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dafcf-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="dafcf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dafcf-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="dafcf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dafcf-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="dafcf-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dafcf-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="dafcf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dafcf-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dafcf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dafcf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dafcf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dafcf-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="dafcf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dafcf-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="dafcf-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dafcf-113">定義</span><span class="sxs-lookup"><span data-stu-id="dafcf-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dafcf-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dafcf-114">Elements and attributes</span></span>

<span data-ttu-id="dafcf-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dafcf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dafcf-116">親要素</span><span class="sxs-lookup"><span data-stu-id="dafcf-116">Parent elements</span></span>

|<span data-ttu-id="dafcf-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="dafcf-117">**Element**</span></span>|<span data-ttu-id="dafcf-118">**型**</span><span class="sxs-lookup"><span data-stu-id="dafcf-118">**Type**</span></span>|<span data-ttu-id="dafcf-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dafcf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dafcf-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="dafcf-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="dafcf-121">RelLineTo_Type</span><span class="sxs-lookup"><span data-stu-id="dafcf-121">RelLineTo_Type</span></span>](rellineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dafcf-122">含まれている x、または図形の幅と高さを基準にして、直線の線分の終点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="dafcf-122">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dafcf-123">子要素</span><span class="sxs-lookup"><span data-stu-id="dafcf-123">Child elements</span></span>

|<span data-ttu-id="dafcf-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="dafcf-124">**Element**</span></span>|<span data-ttu-id="dafcf-125">**型**</span><span class="sxs-lookup"><span data-stu-id="dafcf-125">**Type**</span></span>|<span data-ttu-id="dafcf-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="dafcf-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dafcf-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="dafcf-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dafcf-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="dafcf-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dafcf-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="dafcf-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="dafcf-130">属性</span><span class="sxs-lookup"><span data-stu-id="dafcf-130">Attributes</span></span>

|<span data-ttu-id="dafcf-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="dafcf-131">**Attribute**</span></span>|<span data-ttu-id="dafcf-132">**型**</span><span class="sxs-lookup"><span data-stu-id="dafcf-132">**Type**</span></span>|<span data-ttu-id="dafcf-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="dafcf-133">**Required**</span></span>|<span data-ttu-id="dafcf-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="dafcf-134">**Description**</span></span>|<span data-ttu-id="dafcf-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="dafcf-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dafcf-136">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="dafcf-136">E</span></span>  <br/> |<span data-ttu-id="dafcf-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dafcf-137">xsd:string</span></span>  <br/> |<span data-ttu-id="dafcf-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="dafcf-138">optional</span></span>  <br/> |<span data-ttu-id="dafcf-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="dafcf-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="dafcf-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="dafcf-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="dafcf-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="dafcf-142">F</span></span>  <br/> |<span data-ttu-id="dafcf-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dafcf-143">xsd:string</span></span>  <br/> |<span data-ttu-id="dafcf-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="dafcf-144">optional</span></span>  <br/> | <span data-ttu-id="dafcf-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="dafcf-145">Represents the element's formula.</span></span> <span data-ttu-id="dafcf-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="dafcf-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="dafcf-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="dafcf-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="dafcf-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="dafcf-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="dafcf-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="dafcf-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="dafcf-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="dafcf-151">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="dafcf-151">N</span></span>  <br/> |<span data-ttu-id="dafcf-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dafcf-152">xsd:string</span></span>  <br/> |<span data-ttu-id="dafcf-153">必須</span><span class="sxs-lookup"><span data-stu-id="dafcf-153">required</span></span>  <br/> |<span data-ttu-id="dafcf-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="dafcf-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="dafcf-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="dafcf-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dafcf-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="dafcf-157">U</span><span class="sxs-lookup"><span data-stu-id="dafcf-157">U</span></span>  <br/> |<span data-ttu-id="dafcf-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dafcf-158">xsd:string</span></span>  <br/> |<span data-ttu-id="dafcf-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="dafcf-159">optional</span></span>  <br/> |<span data-ttu-id="dafcf-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="dafcf-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="dafcf-162">V</span><span class="sxs-lookup"><span data-stu-id="dafcf-162">V</span></span>  <br/> |<span data-ttu-id="dafcf-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dafcf-163">xsd:string</span></span>  <br/> |<span data-ttu-id="dafcf-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="dafcf-164">optional</span></span>  <br/> |<span data-ttu-id="dafcf-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="dafcf-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="dafcf-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="dafcf-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dafcf-167">備考</span><span class="sxs-lookup"><span data-stu-id="dafcf-167">Remarks</span></span>

<span data-ttu-id="dafcf-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="dafcf-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="dafcf-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dafcf-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="dafcf-170">**値**</span><span class="sxs-lookup"><span data-stu-id="dafcf-170">**Value**</span></span>|<span data-ttu-id="dafcf-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="dafcf-171">**Description**</span></span>|<span data-ttu-id="dafcf-172">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="dafcf-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dafcf-173">X</span><span class="sxs-lookup"><span data-stu-id="dafcf-173">X</span></span>  <br/> |<span data-ttu-id="dafcf-174">図形の幅を基準にして、直線の線分の終点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="dafcf-174">The x-coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |<span data-ttu-id="dafcf-175">[RelLineTo 行 ([Geometry] セクション)](rellineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="dafcf-175">[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="dafcf-176">Y</span><span class="sxs-lookup"><span data-stu-id="dafcf-176">Y</span></span>  <br/> |<span data-ttu-id="dafcf-177">図形の高さを基準にして、直線の線分の終点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="dafcf-177">The y-coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |<span data-ttu-id="dafcf-178">[RelLineTo 行 ([Geometry] セクション)](rellineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="dafcf-178">[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md)</span></span> <br/> |
   
