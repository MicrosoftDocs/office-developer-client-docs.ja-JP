---
title: Layer_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f92ac1cc-fad2-dab9-5507-838c006ed633
ms.openlocfilehash: 9e6e477e97a0c8f1be1a89bd14262bb4c2a0d7dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396702"
---
# <a name="layertype-complextype-visio-xml"></a><span data-ttu-id="943bc-102">Layer_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="943bc-102">Layer_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="943bc-103">型情報</span><span class="sxs-lookup"><span data-stu-id="943bc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="943bc-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="943bc-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="943bc-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="943bc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="943bc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="943bc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="943bc-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="943bc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="943bc-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="943bc-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="943bc-109">定義</span><span class="sxs-lookup"><span data-stu-id="943bc-109">Definition</span></span>

```XML
          <xs:complexType name="Layer_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LayerRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="943bc-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="943bc-110">Elements and attributes</span></span>

<span data-ttu-id="943bc-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="943bc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="943bc-112">子要素</span><span class="sxs-lookup"><span data-stu-id="943bc-112">Child elements</span></span>

|<span data-ttu-id="943bc-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="943bc-113">**Element**</span></span>|<span data-ttu-id="943bc-114">**型**</span><span class="sxs-lookup"><span data-stu-id="943bc-114">**Type**</span></span>|<span data-ttu-id="943bc-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="943bc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="943bc-116">Row</span><span class="sxs-lookup"><span data-stu-id="943bc-116">Row</span></span>](row-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="943bc-117">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="943bc-117">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="943bc-118">属性</span><span class="sxs-lookup"><span data-stu-id="943bc-118">Attributes</span></span>

<span data-ttu-id="943bc-119">なし。</span><span class="sxs-lookup"><span data-stu-id="943bc-119">None.</span></span>
  

