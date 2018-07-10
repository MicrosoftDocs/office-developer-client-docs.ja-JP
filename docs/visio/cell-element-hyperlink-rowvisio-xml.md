---
title: セル要素 (ハイパーリンクの行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804961"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a><span data-ttu-id="a391e-104">セル要素 (ハイパーリンクの行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a391e-104">Cell element (Hyperlink Row) ('Visio XML')</span></span>

<span data-ttu-id="a391e-105">図形に関連付けられている 1 つのハイパーリンクの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a391e-105">Contains the information for a single hyperlink associated with a shape.</span></span> <span data-ttu-id="a391e-106">図形には、ハイパーリンクごとに 1 つの**ハイパーリンク**の行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a391e-106">A shape will contain one **Hyperlink** row for each hyperlink.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a391e-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="a391e-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a391e-108">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="a391e-108">**Element type**</span></span> <br/> |[<span data-ttu-id="a391e-109">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a391e-109">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a391e-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a391e-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a391e-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a391e-111">**Schema file**</span></span> <br/> |<span data-ttu-id="a391e-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a391e-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a391e-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a391e-113">**Document parts**</span></span> <br/> |<span data-ttu-id="a391e-114"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="a391e-114">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a391e-115">定義</span><span class="sxs-lookup"><span data-stu-id="a391e-115">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a391e-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a391e-116">Elements and attributes</span></span>

<span data-ttu-id="a391e-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a391e-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a391e-118">親要素</span><span class="sxs-lookup"><span data-stu-id="a391e-118">Parent elements</span></span>

|<span data-ttu-id="a391e-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="a391e-119">**Element**</span></span>|<span data-ttu-id="a391e-120">**型**</span><span class="sxs-lookup"><span data-stu-id="a391e-120">**Type**</span></span>|<span data-ttu-id="a391e-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="a391e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a391e-122">行要素 (ハイパーリンクを参照)</span><span class="sxs-lookup"><span data-stu-id="a391e-122">Row element (Hyperlink Section)</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a391e-123">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="a391e-123">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a391e-124">図形に関連付けられている 1 つのハイパーリンクの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a391e-124">Contains the information for a single hyperlink associated with a shape.</span></span> <span data-ttu-id="a391e-125">図形には、ハイパーリンクごとに 1 つの**ハイパーリンク**の行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a391e-125">A shape will contain one **Hyperlink** row for each hyperlink.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a391e-126">子要素</span><span class="sxs-lookup"><span data-stu-id="a391e-126">Child elements</span></span>

|<span data-ttu-id="a391e-127">**要素**</span><span class="sxs-lookup"><span data-stu-id="a391e-127">**Element**</span></span>|<span data-ttu-id="a391e-128">**型**</span><span class="sxs-lookup"><span data-stu-id="a391e-128">**Type**</span></span>|<span data-ttu-id="a391e-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="a391e-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a391e-130">RefBy</span><span class="sxs-lookup"><span data-stu-id="a391e-130">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a391e-131">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a391e-131">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a391e-132">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="a391e-132">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a391e-133">属性</span><span class="sxs-lookup"><span data-stu-id="a391e-133">Attributes</span></span>

|<span data-ttu-id="a391e-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="a391e-134">**Attribute**</span></span>|<span data-ttu-id="a391e-135">**型**</span><span class="sxs-lookup"><span data-stu-id="a391e-135">**Type**</span></span>|<span data-ttu-id="a391e-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="a391e-136">**Required**</span></span>|<span data-ttu-id="a391e-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="a391e-137">**Description**</span></span>|<span data-ttu-id="a391e-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a391e-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a391e-139">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="a391e-139">E</span></span>  <br/> |<span data-ttu-id="a391e-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a391e-140">xsd:string</span></span>  <br/> |<span data-ttu-id="a391e-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="a391e-141">optional</span></span>  <br/> |<span data-ttu-id="a391e-142">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="a391e-142">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="a391e-143">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="a391e-143">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="a391e-144">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="a391e-144">An error message string.</span></span>  <br/> |
|<span data-ttu-id="a391e-145">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="a391e-145">F</span></span>  <br/> |<span data-ttu-id="a391e-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a391e-146">xsd:string</span></span>  <br/> |<span data-ttu-id="a391e-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="a391e-147">optional</span></span>  <br/> | <span data-ttu-id="a391e-148">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="a391e-148">Represents the element's formula.</span></span> <span data-ttu-id="a391e-149">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a391e-149">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="a391e-150">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="a391e-150">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="a391e-151">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="a391e-151">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="a391e-152">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="a391e-152">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="a391e-153">数式です。</span><span class="sxs-lookup"><span data-stu-id="a391e-153">A formula.</span></span>  <br/> |
|<span data-ttu-id="a391e-154">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="a391e-154">N</span></span>  <br/> |<span data-ttu-id="a391e-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a391e-155">xsd:string</span></span>  <br/> |<span data-ttu-id="a391e-156">必須</span><span class="sxs-lookup"><span data-stu-id="a391e-156">required</span></span>  <br/> |<span data-ttu-id="a391e-157">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="a391e-157">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="a391e-158">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="a391e-158">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="a391e-159">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a391e-159">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="a391e-160">U</span><span class="sxs-lookup"><span data-stu-id="a391e-160">U</span></span>  <br/> |<span data-ttu-id="a391e-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a391e-161">xsd:string</span></span>  <br/> |<span data-ttu-id="a391e-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="a391e-162">optional</span></span>  <br/> |<span data-ttu-id="a391e-163">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="a391e-163">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="a391e-164">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="a391e-164">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="a391e-165">V</span><span class="sxs-lookup"><span data-stu-id="a391e-165">V</span></span>  <br/> |<span data-ttu-id="a391e-166">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a391e-166">xsd:string</span></span>  <br/> |<span data-ttu-id="a391e-167">省略可能</span><span class="sxs-lookup"><span data-stu-id="a391e-167">optional</span></span>  <br/> |<span data-ttu-id="a391e-168">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="a391e-168">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="a391e-169">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="a391e-169">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a391e-170">備考</span><span class="sxs-lookup"><span data-stu-id="a391e-170">Remarks</span></span>

<span data-ttu-id="a391e-171">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a391e-171">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="a391e-172">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a391e-172">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="a391e-173">**値**</span><span class="sxs-lookup"><span data-stu-id="a391e-173">**Value**</span></span>|<span data-ttu-id="a391e-174">**説明**</span><span class="sxs-lookup"><span data-stu-id="a391e-174">**Description**</span></span>|<span data-ttu-id="a391e-175">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="a391e-175">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a391e-176">Address</span><span class="sxs-lookup"><span data-stu-id="a391e-176">Address</span></span>  <br/> |<span data-ttu-id="a391e-177">移動先の URL アドレス、ファイル名、または UNC パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a391e-177">Specifies a URL address, file name, or UNC path to which to jump.</span></span>  <br/> |<span data-ttu-id="a391e-178">[[Address] セル ([Hyperlinks] セクション)](address-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-178">[Address Cell (Hyperlinks Section)](address-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-179">Default</span><span class="sxs-lookup"><span data-stu-id="a391e-179">Default</span></span>  <br/> |<span data-ttu-id="a391e-180">図形またはページの既定のハイパーリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="a391e-180">Determines the default hyperlink for a shape or page.</span></span>  <br/> |<span data-ttu-id="a391e-181">[[Default] セル ([Hyperlinks] セクション)](default-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-181">[Default Cell (Hyperlinks Section)](default-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-182">説明</span><span class="sxs-lookup"><span data-stu-id="a391e-182">Description</span></span>  <br/> |<span data-ttu-id="a391e-183">ハイパーリンクの説明文を表示します。</span><span class="sxs-lookup"><span data-stu-id="a391e-183">Represents a descriptive text string for a hyperlink.</span></span>  <br/> |<span data-ttu-id="a391e-184">[[Description] セル ([Hyperlinks] セクション)](description-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-184">[Description Cell (Hyperlinks Section)](description-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-185">ExtraInfo</span><span class="sxs-lookup"><span data-stu-id="a391e-185">ExtraInfo</span></span>  <br/> |<span data-ttu-id="a391e-186">イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。</span><span class="sxs-lookup"><span data-stu-id="a391e-186">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span>  <br/> |<span data-ttu-id="a391e-187">[[ExtraInfo] セル ([Hyperlinks] セクション)](extrainfo-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-187">[ExtraInfo Cell (Hyperlinks Section)](extrainfo-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-188">Frame</span><span class="sxs-lookup"><span data-stu-id="a391e-188">Frame</span></span>  <br/> |<span data-ttu-id="a391e-p107">コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a391e-p107">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>  <br/> |<span data-ttu-id="a391e-191">[[Frame] セル ([Hyperlinks] セクション)](frame-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-191">[Frame Cell (Hyperlinks Section)](frame-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-192">非表示</span><span class="sxs-lookup"><span data-stu-id="a391e-192">Invisible</span></span>  <br/> |<span data-ttu-id="a391e-193">図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a391e-193">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span>  <br/> |<span data-ttu-id="a391e-194">[[Invisible] セル ([Hyperlinks] セクション)](invisible-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-194">[Invisible Cell (Hyperlinks Section)](invisible-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-195">NewWindow</span><span class="sxs-lookup"><span data-stu-id="a391e-195">NewWindow</span></span>  <br/> |<span data-ttu-id="a391e-196">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a391e-196">Specifies whether to open the hyperlink in a new window.</span></span>  <br/> |<span data-ttu-id="a391e-197">[[NewWindow] セル ([Hyperlinks] セクション)](newwindow-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-197">[NewWindow Cell (Hyperlinks Section)](newwindow-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-198">[Sortkey]</span><span class="sxs-lookup"><span data-stu-id="a391e-198">SortKey</span></span>  <br/> |<span data-ttu-id="a391e-199">ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。</span><span class="sxs-lookup"><span data-stu-id="a391e-199">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>  <br/> |<span data-ttu-id="a391e-200">[[SortKey] セル ([Hyperlinks] セクション)](sortkey-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-200">[SortKey Cell (Hyperlinks Section)](sortkey-cell-hyperlinks-section.md)</span></span> <br/> |
|<span data-ttu-id="a391e-201">サブアドレス</span><span class="sxs-lookup"><span data-stu-id="a391e-201">SubAddress</span></span>  <br/> |<span data-ttu-id="a391e-202">リンク先のターゲット図面内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="a391e-202">Specifies a location within the target document to link to.</span></span>  <br/> |<span data-ttu-id="a391e-203">[[SubAddress] セル ([Hyperlinks] セクション)](subaddress-cell-hyperlinks-section.md)</span><span class="sxs-lookup"><span data-stu-id="a391e-203">[SubAddress Cell (Hyperlinks Section)](subaddress-cell-hyperlinks-section.md)</span></span> <br/> |
   
