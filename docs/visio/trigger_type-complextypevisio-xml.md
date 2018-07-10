---
title: Trigger_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 38ba2800a32f4f1b4809a5e542fd6b79794bf369
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806685"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="9f7a7-102">Trigger_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="9f7a7-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9f7a7-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9f7a7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f7a7-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9f7a7-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9f7a7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9f7a7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9f7a7-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9f7a7-108">なし</span><span class="sxs-lookup"><span data-stu-id="9f7a7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f7a7-109">定義</span><span class="sxs-lookup"><span data-stu-id="9f7a7-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9f7a7-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9f7a7-110">Elements and attributes</span></span>

<span data-ttu-id="9f7a7-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f7a7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9f7a7-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9f7a7-112">Child elements</span></span>

|<span data-ttu-id="9f7a7-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-113">**Element**</span></span>|<span data-ttu-id="9f7a7-114">**型**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-114">**Type**</span></span>|<span data-ttu-id="9f7a7-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f7a7-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="9f7a7-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f7a7-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="9f7a7-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9f7a7-118">属性</span><span class="sxs-lookup"><span data-stu-id="9f7a7-118">Attributes</span></span>

|<span data-ttu-id="9f7a7-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-119">**Attribute**</span></span>|<span data-ttu-id="9f7a7-120">**型**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-120">**Type**</span></span>|<span data-ttu-id="9f7a7-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-121">**Required**</span></span>|<span data-ttu-id="9f7a7-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-122">**Description**</span></span>|<span data-ttu-id="9f7a7-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9f7a7-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9f7a7-124">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="9f7a7-124">N</span></span>  <br/> |<span data-ttu-id="9f7a7-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9f7a7-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9f7a7-126">必須</span><span class="sxs-lookup"><span data-stu-id="9f7a7-126">required</span></span>  <br/> ||<span data-ttu-id="9f7a7-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f7a7-127">Values of the xsd:string type.</span></span>  <br/> |
   
