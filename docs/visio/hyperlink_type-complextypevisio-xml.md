---
title: Hyperlink_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 226af4fee615b0dc6ddc4d92d13aff6dd1fd4b19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805532"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="732dd-102">Hyperlink_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="732dd-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="732dd-103">型情報</span><span class="sxs-lookup"><span data-stu-id="732dd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="732dd-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="732dd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="732dd-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="732dd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="732dd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="732dd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="732dd-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="732dd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="732dd-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="732dd-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="732dd-109">定義</span><span class="sxs-lookup"><span data-stu-id="732dd-109">Definition</span></span>

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="732dd-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="732dd-110">Elements and attributes</span></span>

<span data-ttu-id="732dd-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="732dd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="732dd-112">子要素</span><span class="sxs-lookup"><span data-stu-id="732dd-112">Child elements</span></span>

|<span data-ttu-id="732dd-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="732dd-113">**Element**</span></span>|<span data-ttu-id="732dd-114">**型**</span><span class="sxs-lookup"><span data-stu-id="732dd-114">**Type**</span></span>|<span data-ttu-id="732dd-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="732dd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="732dd-116">Row</span><span class="sxs-lookup"><span data-stu-id="732dd-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="732dd-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="732dd-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="732dd-118">属性</span><span class="sxs-lookup"><span data-stu-id="732dd-118">Attributes</span></span>

<span data-ttu-id="732dd-119">なし。</span><span class="sxs-lookup"><span data-stu-id="732dd-119">None.</span></span>
  

