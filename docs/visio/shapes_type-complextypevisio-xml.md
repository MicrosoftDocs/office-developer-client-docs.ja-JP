---
title: Shapes_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 707f20823d0413e0b064b2a367da803419889ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806423"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="09b06-102">Shapes_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="09b06-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="09b06-103">型情報</span><span class="sxs-lookup"><span data-stu-id="09b06-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09b06-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="09b06-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09b06-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="09b06-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09b06-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="09b06-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09b06-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="09b06-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09b06-108">なし</span><span class="sxs-lookup"><span data-stu-id="09b06-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09b06-109">定義</span><span class="sxs-lookup"><span data-stu-id="09b06-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09b06-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="09b06-110">Elements and attributes</span></span>

<span data-ttu-id="09b06-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09b06-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09b06-112">子要素</span><span class="sxs-lookup"><span data-stu-id="09b06-112">Child elements</span></span>

|<span data-ttu-id="09b06-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="09b06-113">**Element**</span></span>|<span data-ttu-id="09b06-114">**型**</span><span class="sxs-lookup"><span data-stu-id="09b06-114">**Type**</span></span>|<span data-ttu-id="09b06-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="09b06-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09b06-116">Shape</span><span class="sxs-lookup"><span data-stu-id="09b06-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09b06-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="09b06-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="09b06-118">属性</span><span class="sxs-lookup"><span data-stu-id="09b06-118">Attributes</span></span>

<span data-ttu-id="09b06-119">なし。</span><span class="sxs-lookup"><span data-stu-id="09b06-119">None.</span></span>
  
