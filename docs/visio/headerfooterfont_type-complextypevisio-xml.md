---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335624"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="43713-102">HeaderFooterFont_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="43713-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="43713-103">型情報</span><span class="sxs-lookup"><span data-stu-id="43713-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43713-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="43713-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43713-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="43713-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43713-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="43713-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43713-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="43713-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43713-108">なし</span><span class="sxs-lookup"><span data-stu-id="43713-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43713-109">定義</span><span class="sxs-lookup"><span data-stu-id="43713-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43713-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="43713-110">Elements and attributes</span></span>

<span data-ttu-id="43713-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43713-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43713-112">子要素</span><span class="sxs-lookup"><span data-stu-id="43713-112">Child elements</span></span>

<span data-ttu-id="43713-113">なし。</span><span class="sxs-lookup"><span data-stu-id="43713-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43713-114">属性</span><span class="sxs-lookup"><span data-stu-id="43713-114">Attributes</span></span>

|<span data-ttu-id="43713-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="43713-115">**Attribute**</span></span>|<span data-ttu-id="43713-116">**型**</span><span class="sxs-lookup"><span data-stu-id="43713-116">**Type**</span></span>|<span data-ttu-id="43713-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="43713-117">**Required**</span></span>|<span data-ttu-id="43713-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="43713-118">**Description**</span></span>|<span data-ttu-id="43713-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="43713-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43713-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="43713-120">CharSet</span></span>  <br/> |<span data-ttu-id="43713-121">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-122">optional</span></span>  <br/> ||<span data-ttu-id="43713-123">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="43713-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="43713-125">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-126">optional</span></span>  <br/> ||<span data-ttu-id="43713-127">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-128">実際</span><span class="sxs-lookup"><span data-stu-id="43713-128">Escapement</span></span>  <br/> |<span data-ttu-id="43713-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="43713-129">xsd:int</span></span>  <br/> |<span data-ttu-id="43713-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-130">optional</span></span>  <br/> ||<span data-ttu-id="43713-131">xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="43713-132">facename</span><span class="sxs-lookup"><span data-stu-id="43713-132">FaceName</span></span>  <br/> |<span data-ttu-id="43713-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="43713-133">xsd:string</span></span>  <br/> |<span data-ttu-id="43713-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-134">optional</span></span>  <br/> ||<span data-ttu-id="43713-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43713-136">Height</span><span class="sxs-lookup"><span data-stu-id="43713-136">Height</span></span>  <br/> |<span data-ttu-id="43713-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="43713-137">xsd:int</span></span>  <br/> |<span data-ttu-id="43713-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-138">optional</span></span>  <br/> ||<span data-ttu-id="43713-139">xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="43713-140">斜体</span><span class="sxs-lookup"><span data-stu-id="43713-140">Italic</span></span>  <br/> |<span data-ttu-id="43713-141">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-142">optional</span></span>  <br/> ||<span data-ttu-id="43713-143">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="43713-144">Orientation</span></span>  <br/> |<span data-ttu-id="43713-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="43713-145">xsd:int</span></span>  <br/> |<span data-ttu-id="43713-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-146">optional</span></span>  <br/> ||<span data-ttu-id="43713-147">xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="43713-148">アウト精度</span><span class="sxs-lookup"><span data-stu-id="43713-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="43713-149">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-150">optional</span></span>  <br/> ||<span data-ttu-id="43713-151">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="43713-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="43713-153">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-154">optional</span></span>  <br/> ||<span data-ttu-id="43713-155">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-156">Quality</span><span class="sxs-lookup"><span data-stu-id="43713-156">Quality</span></span>  <br/> |<span data-ttu-id="43713-157">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-158">optional</span></span>  <br/> ||<span data-ttu-id="43713-159">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-160">線</span><span class="sxs-lookup"><span data-stu-id="43713-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="43713-161">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-162">optional</span></span>  <br/> ||<span data-ttu-id="43713-163">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-164">Underline</span><span class="sxs-lookup"><span data-stu-id="43713-164">Underline</span></span>  <br/> |<span data-ttu-id="43713-165">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="43713-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43713-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-166">optional</span></span>  <br/> ||<span data-ttu-id="43713-167">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43713-168">太さ</span><span class="sxs-lookup"><span data-stu-id="43713-168">Weight</span></span>  <br/> |<span data-ttu-id="43713-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="43713-169">xsd:int</span></span>  <br/> |<span data-ttu-id="43713-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-170">optional</span></span>  <br/> ||<span data-ttu-id="43713-171">xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="43713-172">Width</span><span class="sxs-lookup"><span data-stu-id="43713-172">Width</span></span>  <br/> |<span data-ttu-id="43713-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="43713-173">xsd:int</span></span>  <br/> |<span data-ttu-id="43713-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="43713-174">optional</span></span>  <br/> ||<span data-ttu-id="43713-175">xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="43713-175">Values of the xsd:int type.</span></span>  <br/> |
   

