---
title: RefBy 要素 (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: 図面内のページへの参照を指定します。
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538292"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="fbde9-103">RefBy 要素 (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fbde9-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fbde9-104">図面内のページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="fbde9-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbde9-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="fbde9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbde9-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="fbde9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fbde9-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="fbde9-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fbde9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fbde9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fbde9-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fbde9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fbde9-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="fbde9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fbde9-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="fbde9-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="fbde9-112">定義</span><span class="sxs-lookup"><span data-stu-id="fbde9-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fbde9-113">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fbde9-113">Elements and attributes</span></span>

<span data-ttu-id="fbde9-114">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fbde9-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fbde9-115">親要素</span><span class="sxs-lookup"><span data-stu-id="fbde9-115">Parent elements</span></span>

|<span data-ttu-id="fbde9-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="fbde9-116">**Element**</span></span>|<span data-ttu-id="fbde9-117">**型**</span><span class="sxs-lookup"><span data-stu-id="fbde9-117">**Type**</span></span>|<span data-ttu-id="fbde9-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="fbde9-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbde9-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="fbde9-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="fbde9-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="fbde9-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbde9-121">Visio ファイル内の文書パーツ間のリレーションシップを再計算するための手順を Microsoft Visio に提供します。</span><span class="sxs-lookup"><span data-stu-id="fbde9-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="fbde9-122">子要素</span><span class="sxs-lookup"><span data-stu-id="fbde9-122">Child elements</span></span>

<span data-ttu-id="fbde9-123">なし。</span><span class="sxs-lookup"><span data-stu-id="fbde9-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbde9-124">属性</span><span class="sxs-lookup"><span data-stu-id="fbde9-124">Attributes</span></span>

|<span data-ttu-id="fbde9-125">**属性**</span><span class="sxs-lookup"><span data-stu-id="fbde9-125">**Attribute**</span></span>|<span data-ttu-id="fbde9-126">**型**</span><span class="sxs-lookup"><span data-stu-id="fbde9-126">**Type**</span></span>|<span data-ttu-id="fbde9-127">**必須**</span><span class="sxs-lookup"><span data-stu-id="fbde9-127">**Required**</span></span>|<span data-ttu-id="fbde9-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="fbde9-128">**Description**</span></span>|<span data-ttu-id="fbde9-129">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="fbde9-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fbde9-130">ID</span><span class="sxs-lookup"><span data-stu-id="fbde9-130">ID</span></span>  <br/> |<span data-ttu-id="fbde9-131">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="fbde9-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fbde9-132">必須</span><span class="sxs-lookup"><span data-stu-id="fbde9-132">required</span></span>  <br/> |<span data-ttu-id="fbde9-133">図面内のページの ID 属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="fbde9-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="fbde9-134">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="fbde9-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fbde9-135">T</span><span class="sxs-lookup"><span data-stu-id="fbde9-135">T</span></span>  <br/> |<span data-ttu-id="fbde9-136">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fbde9-136">xsd:string</span></span>  <br/> |<span data-ttu-id="fbde9-137">必須</span><span class="sxs-lookup"><span data-stu-id="fbde9-137">required</span></span>  <br/> |<span data-ttu-id="fbde9-138">参照の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="fbde9-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="fbde9-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="fbde9-139">Values of the xsd:string type.</span></span>  <br/> |
   

