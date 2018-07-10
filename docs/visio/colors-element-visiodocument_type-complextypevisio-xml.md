---
title: 色要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: 図面のカラー テーブルが含まれています。
ms.openlocfilehash: d13690ce6e1772ab1a43e697e8b99c0776a204b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805029"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="39b6f-103">色要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="39b6f-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="39b6f-104">図面のカラー テーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="39b6f-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39b6f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="39b6f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39b6f-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="39b6f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="39b6f-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="39b6f-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="39b6f-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="39b6f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="39b6f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="39b6f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="39b6f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="39b6f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="39b6f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="39b6f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="39b6f-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="39b6f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39b6f-113">定義</span><span class="sxs-lookup"><span data-stu-id="39b6f-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39b6f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="39b6f-114">Elements and attributes</span></span>

<span data-ttu-id="39b6f-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b6f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="39b6f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="39b6f-116">Parent elements</span></span>

|<span data-ttu-id="39b6f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="39b6f-117">**Element**</span></span>|<span data-ttu-id="39b6f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="39b6f-118">**Type**</span></span>|<span data-ttu-id="39b6f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="39b6f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39b6f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="39b6f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="39b6f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="39b6f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39b6f-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="39b6f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39b6f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="39b6f-123">Child elements</span></span>

|<span data-ttu-id="39b6f-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="39b6f-124">**Element**</span></span>|<span data-ttu-id="39b6f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="39b6f-125">**Type**</span></span>|<span data-ttu-id="39b6f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="39b6f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39b6f-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="39b6f-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="39b6f-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="39b6f-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39b6f-129">カラー テーブルのエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="39b6f-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="39b6f-130">属性</span><span class="sxs-lookup"><span data-stu-id="39b6f-130">Attributes</span></span>

<span data-ttu-id="39b6f-131">なし。</span><span class="sxs-lookup"><span data-stu-id="39b6f-131">None.</span></span>
  
