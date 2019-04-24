---
title: colorentry 要素 (Colors_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: カラーテーブルエントリを含みます。
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358087"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="d5a47-103">colorentry 要素 (Colors_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d5a47-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d5a47-104">カラーテーブルエントリを含みます。</span><span class="sxs-lookup"><span data-stu-id="d5a47-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5a47-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d5a47-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5a47-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d5a47-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d5a47-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="d5a47-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d5a47-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5a47-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d5a47-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d5a47-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d5a47-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d5a47-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d5a47-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d5a47-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d5a47-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="d5a47-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5a47-113">定義</span><span class="sxs-lookup"><span data-stu-id="d5a47-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d5a47-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d5a47-114">Elements and attributes</span></span>

<span data-ttu-id="d5a47-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5a47-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d5a47-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d5a47-116">Parent elements</span></span>

|<span data-ttu-id="d5a47-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d5a47-117">**Element**</span></span>|<span data-ttu-id="d5a47-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d5a47-118">**Type**</span></span>|<span data-ttu-id="d5a47-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5a47-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5a47-120">Colors</span><span class="sxs-lookup"><span data-stu-id="d5a47-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a47-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="d5a47-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d5a47-122">図面のカラーテーブルを含みます。</span><span class="sxs-lookup"><span data-stu-id="d5a47-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d5a47-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d5a47-123">Child elements</span></span>

<span data-ttu-id="d5a47-124">なし。</span><span class="sxs-lookup"><span data-stu-id="d5a47-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5a47-125">属性</span><span class="sxs-lookup"><span data-stu-id="d5a47-125">Attributes</span></span>

|<span data-ttu-id="d5a47-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="d5a47-126">**Attribute**</span></span>|<span data-ttu-id="d5a47-127">**型**</span><span class="sxs-lookup"><span data-stu-id="d5a47-127">**Type**</span></span>|<span data-ttu-id="d5a47-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="d5a47-128">**Required**</span></span>|<span data-ttu-id="d5a47-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5a47-129">**Description**</span></span>|<span data-ttu-id="d5a47-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d5a47-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5a47-131">IX</span><span class="sxs-lookup"><span data-stu-id="d5a47-131">IX</span></span>  <br/> |<span data-ttu-id="d5a47-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d5a47-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a47-133">必須</span><span class="sxs-lookup"><span data-stu-id="d5a47-133">required</span></span>  <br/> |<span data-ttu-id="d5a47-134">親要素内の要素の0から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="d5a47-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="d5a47-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a47-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a47-136">RGB</span><span class="sxs-lookup"><span data-stu-id="d5a47-136">RGB</span></span>  <br/> |<span data-ttu-id="d5a47-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d5a47-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d5a47-138">必須</span><span class="sxs-lookup"><span data-stu-id="d5a47-138">required</span></span>  <br/> |<span data-ttu-id="d5a47-139">色の表のエントリの16進数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5a47-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="d5a47-140">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a47-140">Values of the xsd:string type.</span></span>  <br/> |
   

