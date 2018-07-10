---
title: Paragraph_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: 4d15d262d66a2d247aa432d08b22e6fe3a460e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805989"
---
# <a name="paragraphtype-complextype-visio-xml"></a><span data-ttu-id="bf526-102">Paragraph_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="bf526-102">Paragraph_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bf526-103">型情報</span><span class="sxs-lookup"><span data-stu-id="bf526-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf526-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="bf526-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bf526-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bf526-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bf526-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bf526-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bf526-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="bf526-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bf526-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="bf526-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf526-109">定義</span><span class="sxs-lookup"><span data-stu-id="bf526-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bf526-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bf526-110">Elements and attributes</span></span>

<span data-ttu-id="bf526-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf526-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bf526-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bf526-112">Child elements</span></span>

|<span data-ttu-id="bf526-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="bf526-113">**Element**</span></span>|<span data-ttu-id="bf526-114">**型**</span><span class="sxs-lookup"><span data-stu-id="bf526-114">**Type**</span></span>|<span data-ttu-id="bf526-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf526-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf526-116">Row</span><span class="sxs-lookup"><span data-stu-id="bf526-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="bf526-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="bf526-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bf526-118">属性</span><span class="sxs-lookup"><span data-stu-id="bf526-118">Attributes</span></span>

<span data-ttu-id="bf526-119">なし。</span><span class="sxs-lookup"><span data-stu-id="bf526-119">None.</span></span>
  
