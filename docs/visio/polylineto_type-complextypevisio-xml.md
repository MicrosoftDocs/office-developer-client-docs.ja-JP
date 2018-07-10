---
title: PolylineTo_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: 051054b8ad95438392a006814331d75e4721d0e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806023"
---
# <a name="polylinetotype-complextype-visio-xml"></a><span data-ttu-id="72732-102">PolylineTo_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="72732-102">PolylineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="72732-103">型情報</span><span class="sxs-lookup"><span data-stu-id="72732-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72732-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="72732-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="72732-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="72732-105">**Schema file**</span></span> <br/> |<span data-ttu-id="72732-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="72732-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="72732-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="72732-107">**Extension base**</span></span> <br/> |<span data-ttu-id="72732-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="72732-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72732-109">定義</span><span class="sxs-lookup"><span data-stu-id="72732-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="72732-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="72732-110">Elements and attributes</span></span>

<span data-ttu-id="72732-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72732-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="72732-112">子要素</span><span class="sxs-lookup"><span data-stu-id="72732-112">Child elements</span></span>

|<span data-ttu-id="72732-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="72732-113">**Element**</span></span>|<span data-ttu-id="72732-114">**型**</span><span class="sxs-lookup"><span data-stu-id="72732-114">**Type**</span></span>|<span data-ttu-id="72732-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="72732-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72732-116">Cell</span><span class="sxs-lookup"><span data-stu-id="72732-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="72732-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="72732-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="72732-118">属性</span><span class="sxs-lookup"><span data-stu-id="72732-118">Attributes</span></span>

<span data-ttu-id="72732-119">なし。</span><span class="sxs-lookup"><span data-stu-id="72732-119">None.</span></span>
  
