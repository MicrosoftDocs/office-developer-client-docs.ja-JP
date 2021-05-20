---
title: Window_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538453"
---
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="6130d-102">Window_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6130d-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6130d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6130d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6130d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6130d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6130d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6130d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6130d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6130d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6130d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6130d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6130d-108">なし</span><span class="sxs-lookup"><span data-stu-id="6130d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6130d-109">定義</span><span class="sxs-lookup"><span data-stu-id="6130d-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6130d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6130d-110">Elements and attributes</span></span>

<span data-ttu-id="6130d-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6130d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6130d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6130d-112">Child elements</span></span>

|<span data-ttu-id="6130d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6130d-113">**Element**</span></span>|<span data-ttu-id="6130d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="6130d-114">**Type**</span></span>|<span data-ttu-id="6130d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="6130d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6130d-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="6130d-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="6130d-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="6130d-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="6130d-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="6130d-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="6130d-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="6130d-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="6130d-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="6130d-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="6130d-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="6130d-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="6130d-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6130d-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="6130d-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6130d-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="6130d-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6130d-142">属性</span><span class="sxs-lookup"><span data-stu-id="6130d-142">Attributes</span></span>

|<span data-ttu-id="6130d-143">**属性**</span><span class="sxs-lookup"><span data-stu-id="6130d-143">**Attribute**</span></span>|<span data-ttu-id="6130d-144">**型**</span><span class="sxs-lookup"><span data-stu-id="6130d-144">**Type**</span></span>|<span data-ttu-id="6130d-145">**必須**</span><span class="sxs-lookup"><span data-stu-id="6130d-145">**Required**</span></span>|<span data-ttu-id="6130d-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="6130d-146">**Description**</span></span>|<span data-ttu-id="6130d-147">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="6130d-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6130d-148">Container</span><span class="sxs-lookup"><span data-stu-id="6130d-148">Container</span></span>  <br/> |<span data-ttu-id="6130d-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-150">optional</span></span>  <br/> ||<span data-ttu-id="6130d-151">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="6130d-152">ContainerType</span></span>  <br/> |<span data-ttu-id="6130d-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6130d-153">xsd:token</span></span>  <br/> |<span data-ttu-id="6130d-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-154">optional</span></span>  <br/> ||<span data-ttu-id="6130d-155">xsd:token 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6130d-156">Document</span><span class="sxs-lookup"><span data-stu-id="6130d-156">Document</span></span>  <br/> |<span data-ttu-id="6130d-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6130d-157">xsd:string</span></span>  <br/> |<span data-ttu-id="6130d-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-158">optional</span></span>  <br/> ||<span data-ttu-id="6130d-159">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6130d-160">ID</span><span class="sxs-lookup"><span data-stu-id="6130d-160">ID</span></span>  <br/> |<span data-ttu-id="6130d-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-162">必須</span><span class="sxs-lookup"><span data-stu-id="6130d-162">required</span></span>  <br/> ||<span data-ttu-id="6130d-163">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-164">Master</span><span class="sxs-lookup"><span data-stu-id="6130d-164">Master</span></span>  <br/> |<span data-ttu-id="6130d-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-166">optional</span></span>  <br/> ||<span data-ttu-id="6130d-167">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-168">Page</span><span class="sxs-lookup"><span data-stu-id="6130d-168">Page</span></span>  <br/> |<span data-ttu-id="6130d-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-170">optional</span></span>  <br/> ||<span data-ttu-id="6130d-171">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="6130d-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="6130d-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-174">optional</span></span>  <br/> ||<span data-ttu-id="6130d-175">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6130d-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="6130d-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6130d-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6130d-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-178">optional</span></span>  <br/> ||<span data-ttu-id="6130d-179">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6130d-180">Sheet</span><span class="sxs-lookup"><span data-stu-id="6130d-180">Sheet</span></span>  <br/> |<span data-ttu-id="6130d-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-182">optional</span></span>  <br/> ||<span data-ttu-id="6130d-183">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="6130d-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="6130d-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6130d-185">xsd:double</span></span>  <br/> |<span data-ttu-id="6130d-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-186">optional</span></span>  <br/> ||<span data-ttu-id="6130d-187">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6130d-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="6130d-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="6130d-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6130d-189">xsd:double</span></span>  <br/> |<span data-ttu-id="6130d-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-190">optional</span></span>  <br/> ||<span data-ttu-id="6130d-191">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6130d-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="6130d-192">ViewScale</span></span>  <br/> |<span data-ttu-id="6130d-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6130d-193">xsd:double</span></span>  <br/> |<span data-ttu-id="6130d-194">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-194">optional</span></span>  <br/> ||<span data-ttu-id="6130d-195">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6130d-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="6130d-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="6130d-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-198">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-198">optional</span></span>  <br/> ||<span data-ttu-id="6130d-199">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="6130d-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="6130d-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="6130d-201">xsd:short</span></span>  <br/> |<span data-ttu-id="6130d-202">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-202">optional</span></span>  <br/> ||<span data-ttu-id="6130d-203">xsd:short 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="6130d-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="6130d-204">WindowState</span></span>  <br/> |<span data-ttu-id="6130d-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-206">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-206">optional</span></span>  <br/> ||<span data-ttu-id="6130d-207">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6130d-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="6130d-208">WindowTop</span></span>  <br/> |<span data-ttu-id="6130d-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="6130d-209">xsd:short</span></span>  <br/> |<span data-ttu-id="6130d-210">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-210">optional</span></span>  <br/> ||<span data-ttu-id="6130d-211">xsd:short 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="6130d-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="6130d-212">WindowType</span></span>  <br/> |<span data-ttu-id="6130d-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6130d-213">xsd:token</span></span>  <br/> |<span data-ttu-id="6130d-214">必須</span><span class="sxs-lookup"><span data-stu-id="6130d-214">required</span></span>  <br/> ||<span data-ttu-id="6130d-215">xsd:token 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6130d-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="6130d-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="6130d-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6130d-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6130d-218">省略可能</span><span class="sxs-lookup"><span data-stu-id="6130d-218">optional</span></span>  <br/> ||<span data-ttu-id="6130d-219">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6130d-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

