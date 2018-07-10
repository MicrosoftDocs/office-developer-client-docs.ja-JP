---
title: AuthorList 要素 (Comments_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: 図面内のコメントの作成者を指定します。
ms.openlocfilehash: 0f31e11e52809df60b41cb67b868b15435e0eb47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804815"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="ae4b3-103">AuthorList 要素 (Comments_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ae4b3-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ae4b3-104">図面内のコメントの作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae4b3-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae4b3-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ae4b3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae4b3-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ae4b3-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="ae4b3-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ae4b3-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ae4b3-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ae4b3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ae4b3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ae4b3-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ae4b3-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="ae4b3-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae4b3-113">定義</span><span class="sxs-lookup"><span data-stu-id="ae4b3-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ae4b3-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ae4b3-114">Elements and attributes</span></span>

<span data-ttu-id="ae4b3-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae4b3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ae4b3-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ae4b3-116">Parent elements</span></span>

|<span data-ttu-id="ae4b3-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-117">**Element**</span></span>|<span data-ttu-id="ae4b3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-118">**Type**</span></span>|<span data-ttu-id="ae4b3-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae4b3-120">Comments</span><span class="sxs-lookup"><span data-stu-id="ae4b3-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae4b3-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="ae4b3-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae4b3-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae4b3-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae4b3-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ae4b3-123">Child elements</span></span>

|<span data-ttu-id="ae4b3-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-124">**Element**</span></span>|<span data-ttu-id="ae4b3-125">**型**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-125">**Type**</span></span>|<span data-ttu-id="ae4b3-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae4b3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae4b3-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="ae4b3-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae4b3-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="ae4b3-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae4b3-129">図面内のコメントの作成者を識別するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae4b3-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ae4b3-130">属性</span><span class="sxs-lookup"><span data-stu-id="ae4b3-130">Attributes</span></span>

<span data-ttu-id="ae4b3-131">なし。</span><span class="sxs-lookup"><span data-stu-id="ae4b3-131">None.</span></span>
  
