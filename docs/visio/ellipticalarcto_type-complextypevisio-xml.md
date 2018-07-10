---
title: EllipticalArcTo_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: da67df28a2081a52b9bcef39c06540b247a2a79e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805310"
---
# <a name="ellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="2395d-102">EllipticalArcTo_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="2395d-102">EllipticalArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2395d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="2395d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2395d-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="2395d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2395d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2395d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2395d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2395d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2395d-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="2395d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2395d-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2395d-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2395d-109">定義</span><span class="sxs-lookup"><span data-stu-id="2395d-109">Definition</span></span>

```XML
          <xs:complexType name="EllipticalArcTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2395d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2395d-110">Elements and attributes</span></span>

<span data-ttu-id="2395d-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2395d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2395d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="2395d-112">Child elements</span></span>

|<span data-ttu-id="2395d-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="2395d-113">**Element**</span></span>|<span data-ttu-id="2395d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="2395d-114">**Type**</span></span>|<span data-ttu-id="2395d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="2395d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2395d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2395d-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="2395d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2395d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2395d-118">属性</span><span class="sxs-lookup"><span data-stu-id="2395d-118">Attributes</span></span>

<span data-ttu-id="2395d-119">なし。</span><span class="sxs-lookup"><span data-stu-id="2395d-119">None.</span></span>
  
