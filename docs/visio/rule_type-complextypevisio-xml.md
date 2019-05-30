---
title: Rule_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541716"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="1b921-102">Rule_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1b921-102">Rule_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1b921-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1b921-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b921-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b921-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b921-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b921-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b921-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="1b921-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b921-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1b921-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b921-108">None</span><span class="sxs-lookup"><span data-stu-id="1b921-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b921-109">定義</span><span class="sxs-lookup"><span data-stu-id="1b921-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b921-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1b921-110">Elements and attributes</span></span>

<span data-ttu-id="1b921-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b921-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b921-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1b921-112">Child elements</span></span>

|<span data-ttu-id="1b921-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b921-113">**Element**</span></span>|<span data-ttu-id="1b921-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1b921-114">**Type**</span></span>|<span data-ttu-id="1b921-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b921-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b921-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="1b921-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b921-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="1b921-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1b921-118">ルール</span><span class="sxs-lookup"><span data-stu-id="1b921-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b921-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="1b921-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1b921-120">属性</span><span class="sxs-lookup"><span data-stu-id="1b921-120">Attributes</span></span>

|<span data-ttu-id="1b921-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="1b921-121">**Attribute**</span></span>|<span data-ttu-id="1b921-122">**型**</span><span class="sxs-lookup"><span data-stu-id="1b921-122">**Type**</span></span>|<span data-ttu-id="1b921-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="1b921-123">**Required**</span></span>|<span data-ttu-id="1b921-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b921-124">**Description**</span></span>|<span data-ttu-id="1b921-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1b921-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b921-126">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="1b921-126">Category</span></span>  <br/> |<span data-ttu-id="1b921-127">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1b921-127">xsd:string</span></span>  <br/> |<span data-ttu-id="1b921-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b921-128">optional</span></span>  <br/> ||<span data-ttu-id="1b921-129">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b921-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b921-130">説明</span><span class="sxs-lookup"><span data-stu-id="1b921-130">Description</span></span>  <br/> |<span data-ttu-id="1b921-131">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1b921-131">xsd:string</span></span>  <br/> |<span data-ttu-id="1b921-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b921-132">optional</span></span>  <br/> ||<span data-ttu-id="1b921-133">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b921-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b921-134">ID</span><span class="sxs-lookup"><span data-stu-id="1b921-134">ID</span></span>  <br/> |<span data-ttu-id="1b921-135">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="1b921-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b921-136">必須</span><span class="sxs-lookup"><span data-stu-id="1b921-136">required</span></span>  <br/> ||<span data-ttu-id="1b921-137">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b921-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b921-138">Ignored</span><span class="sxs-lookup"><span data-stu-id="1b921-138">Ignored</span></span>  <br/> |<span data-ttu-id="1b921-139">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="1b921-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1b921-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b921-140">optional</span></span>  <br/> ||<span data-ttu-id="1b921-141">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b921-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1b921-142">NameU</span><span class="sxs-lookup"><span data-stu-id="1b921-142">NameU</span></span>  <br/> |<span data-ttu-id="1b921-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1b921-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1b921-144">必須</span><span class="sxs-lookup"><span data-stu-id="1b921-144">required</span></span>  <br/> ||<span data-ttu-id="1b921-145">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b921-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b921-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="1b921-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="1b921-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="1b921-147">xsd:int</span></span>  <br/> |<span data-ttu-id="1b921-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b921-148">optional</span></span>  <br/> ||<span data-ttu-id="1b921-149">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b921-149">Values of the xsd:int type.</span></span>  <br/> |
   

