---
title: DataColumns_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: f125bce02fab43b808608ef6b14d59dfc08a1179
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805158"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="a5b91-102">DataColumns_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a5b91-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a5b91-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a5b91-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5b91-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a5b91-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a5b91-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a5b91-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a5b91-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a5b91-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a5b91-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="a5b91-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a5b91-108">なし</span><span class="sxs-lookup"><span data-stu-id="a5b91-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a5b91-109">定義</span><span class="sxs-lookup"><span data-stu-id="a5b91-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a5b91-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a5b91-110">Elements and attributes</span></span>

<span data-ttu-id="a5b91-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5b91-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a5b91-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a5b91-112">Child elements</span></span>

|<span data-ttu-id="a5b91-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="a5b91-113">**Element**</span></span>|<span data-ttu-id="a5b91-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a5b91-114">**Type**</span></span>|<span data-ttu-id="a5b91-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a5b91-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a5b91-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="a5b91-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5b91-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="a5b91-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a5b91-118">属性</span><span class="sxs-lookup"><span data-stu-id="a5b91-118">Attributes</span></span>

|<span data-ttu-id="a5b91-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="a5b91-119">**Attribute**</span></span>|<span data-ttu-id="a5b91-120">**型**</span><span class="sxs-lookup"><span data-stu-id="a5b91-120">**Type**</span></span>|<span data-ttu-id="a5b91-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="a5b91-121">**Required**</span></span>|<span data-ttu-id="a5b91-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="a5b91-122">**Description**</span></span>|<span data-ttu-id="a5b91-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a5b91-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a5b91-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="a5b91-124">SortAsc</span></span>  <br/> |<span data-ttu-id="a5b91-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a5b91-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a5b91-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a5b91-126">optional</span></span>  <br/> ||<span data-ttu-id="a5b91-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5b91-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a5b91-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="a5b91-128">SortColumn</span></span>  <br/> |<span data-ttu-id="a5b91-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a5b91-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a5b91-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="a5b91-130">optional</span></span>  <br/> ||<span data-ttu-id="a5b91-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5b91-131">Values of the xsd:string type.</span></span>  <br/> |
   
