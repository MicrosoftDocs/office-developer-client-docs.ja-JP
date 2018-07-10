---
title: セル要素 ([nurbsto] 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: 2 番目の最後のノット、最初のウェイトまたは不均一な合理性のある B-スプライン (NURBS) の数式の位置、最初のノットの位置、最後のウェイトの位置の x 座標または y 座標、位置が含まれています。
ms.openlocfilehash: acdc61235fde88a0f5b03eb6e83f54092b4f1fd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804976"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a><span data-ttu-id="0f361-103">セル要素 ([nurbsto] 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0f361-103">Cell element (NURBSTo Row) ('Visio XML')</span></span>

<span data-ttu-id="0f361-104">2 番目の最後のノット、最初のウェイトまたは不均一な合理性のある B-スプライン (NURBS) の数式の位置、最初のノットの位置、最後のウェイトの位置の x 座標または y 座標、位置が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f361-104">Contains the x- or y-coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, or the formula for a nonuniform rational B-spline (NURBS).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f361-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="0f361-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f361-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="0f361-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0f361-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0f361-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0f361-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0f361-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0f361-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0f361-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0f361-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0f361-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0f361-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0f361-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0f361-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="0f361-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f361-113">定義</span><span class="sxs-lookup"><span data-stu-id="0f361-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f361-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0f361-114">Elements and attributes</span></span>

<span data-ttu-id="0f361-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f361-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0f361-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0f361-116">Parent elements</span></span>

|<span data-ttu-id="0f361-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0f361-117">**Element**</span></span>|<span data-ttu-id="0f361-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0f361-118">**Type**</span></span>|<span data-ttu-id="0f361-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f361-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f361-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="0f361-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0f361-121">NURBSTo_Type</span><span class="sxs-lookup"><span data-stu-id="0f361-121">NURBSTo_Type</span></span>](nurbsto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f361-122">2 番目の最後のノット、最初のウェイトまたは不均一な合理性のある B-スプライン (NURBS) の数式の位置、最初のノットの位置、最後のウェイトの位置の x 座標または y 座標、位置が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f361-122">Contains the x- or y-coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, or the formula for a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f361-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0f361-123">Child elements</span></span>

|<span data-ttu-id="0f361-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="0f361-124">**Element**</span></span>|<span data-ttu-id="0f361-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0f361-125">**Type**</span></span>|<span data-ttu-id="0f361-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f361-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f361-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="0f361-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f361-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0f361-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f361-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f361-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0f361-130">属性</span><span class="sxs-lookup"><span data-stu-id="0f361-130">Attributes</span></span>

|<span data-ttu-id="0f361-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="0f361-131">**Attribute**</span></span>|<span data-ttu-id="0f361-132">**型**</span><span class="sxs-lookup"><span data-stu-id="0f361-132">**Type**</span></span>|<span data-ttu-id="0f361-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="0f361-133">**Required**</span></span>|<span data-ttu-id="0f361-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f361-134">**Description**</span></span>|<span data-ttu-id="0f361-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0f361-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0f361-136">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="0f361-136">E</span></span>  <br/> |<span data-ttu-id="0f361-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0f361-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0f361-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0f361-138">optional</span></span>  <br/> |<span data-ttu-id="0f361-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="0f361-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="0f361-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="0f361-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="0f361-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="0f361-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="0f361-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="0f361-142">F</span></span>  <br/> |<span data-ttu-id="0f361-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0f361-143">xsd:string</span></span>  <br/> |<span data-ttu-id="0f361-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="0f361-144">optional</span></span>  <br/> | <span data-ttu-id="0f361-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="0f361-145">Represents the element's formula.</span></span> <span data-ttu-id="0f361-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0f361-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="0f361-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="0f361-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="0f361-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="0f361-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="0f361-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="0f361-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="0f361-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="0f361-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="0f361-151">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="0f361-151">N</span></span>  <br/> |<span data-ttu-id="0f361-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0f361-152">xsd:string</span></span>  <br/> |<span data-ttu-id="0f361-153">必須</span><span class="sxs-lookup"><span data-stu-id="0f361-153">required</span></span>  <br/> |<span data-ttu-id="0f361-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="0f361-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="0f361-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="0f361-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="0f361-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f361-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="0f361-157">U</span><span class="sxs-lookup"><span data-stu-id="0f361-157">U</span></span>  <br/> |<span data-ttu-id="0f361-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0f361-158">xsd:string</span></span>  <br/> |<span data-ttu-id="0f361-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="0f361-159">optional</span></span>  <br/> |<span data-ttu-id="0f361-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="0f361-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="0f361-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="0f361-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="0f361-162">V</span><span class="sxs-lookup"><span data-stu-id="0f361-162">V</span></span>  <br/> |<span data-ttu-id="0f361-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0f361-163">xsd:string</span></span>  <br/> |<span data-ttu-id="0f361-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="0f361-164">optional</span></span>  <br/> |<span data-ttu-id="0f361-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="0f361-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="0f361-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="0f361-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f361-167">備考</span><span class="sxs-lookup"><span data-stu-id="0f361-167">Remarks</span></span>

<span data-ttu-id="0f361-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f361-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="0f361-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f361-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="0f361-170">**値**</span><span class="sxs-lookup"><span data-stu-id="0f361-170">**Value**</span></span>|<span data-ttu-id="0f361-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f361-171">**Description**</span></span>|<span data-ttu-id="0f361-172">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="0f361-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f361-173">X</span><span class="sxs-lookup"><span data-stu-id="0f361-173">X</span></span>  <br/> |<span data-ttu-id="0f361-174">NURBS の最後のコントロール ポイントの x 座標。</span><span class="sxs-lookup"><span data-stu-id="0f361-174">The x-coordinate of the last control point of a NURBS.</span></span>  <br/> |<span data-ttu-id="0f361-175">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-175">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0f361-176">Y</span><span class="sxs-lookup"><span data-stu-id="0f361-176">Y</span></span>  <br/> |<span data-ttu-id="0f361-177">NURBS の最後のコントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="0f361-177">The y-coordinate of the last control point of a NURBS.</span></span>  <br/> |<span data-ttu-id="0f361-178">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-178">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0f361-179">A</span><span class="sxs-lookup"><span data-stu-id="0f361-179">A</span></span>  <br/> |<span data-ttu-id="0f361-180">NURBS の最後から 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="0f361-180">The second to the last knot of the NURBS.</span></span>  <br/> |<span data-ttu-id="0f361-181">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-181">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0f361-182">B</span><span class="sxs-lookup"><span data-stu-id="0f361-182">B</span></span>  <br/> |<span data-ttu-id="0f361-183">NURBS の最後のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="0f361-183">The last weight of the NURBS.</span></span>  <br/> |<span data-ttu-id="0f361-184">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-184">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0f361-185">C</span><span class="sxs-lookup"><span data-stu-id="0f361-185">C</span></span>  <br/> |<span data-ttu-id="0f361-186">NURBS の最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="0f361-186">The first knot of the NURBS.</span></span>  <br/> |<span data-ttu-id="0f361-187">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-187">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0f361-188">D</span><span class="sxs-lookup"><span data-stu-id="0f361-188">D</span></span>  <br/> |<span data-ttu-id="0f361-189">NURBS の最初のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="0f361-189">The first weight of the NURBS.</span></span>  <br/> |<span data-ttu-id="0f361-190">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-190">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0f361-191">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="0f361-191">E</span></span>  <br/> |<span data-ttu-id="0f361-192">NURBS の数式です。</span><span class="sxs-lookup"><span data-stu-id="0f361-192">A NURBS formula.</span></span>  <br/> |<span data-ttu-id="0f361-193">[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0f361-193">[NURBSTo Row (Geometry Section)](nurbsto-row-geometry-section.md)</span></span> <br/> |
   
