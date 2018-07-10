---
title: Scratch_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 973a0db86eec553c7a728095e28735d4cdb91041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806346"
---
# <a name="scratchtype-complextype-visio-xml"></a><span data-ttu-id="23857-102">Scratch_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="23857-102">Scratch_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23857-103">型情報</span><span class="sxs-lookup"><span data-stu-id="23857-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23857-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="23857-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23857-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="23857-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23857-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23857-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23857-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="23857-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23857-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="23857-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23857-109">定義</span><span class="sxs-lookup"><span data-stu-id="23857-109">Definition</span></span>

```XML
          <xs:complexType name="Scratch_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ScratchRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23857-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="23857-110">Elements and attributes</span></span>

<span data-ttu-id="23857-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23857-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23857-112">子要素</span><span class="sxs-lookup"><span data-stu-id="23857-112">Child elements</span></span>

|<span data-ttu-id="23857-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="23857-113">**Element**</span></span>|<span data-ttu-id="23857-114">**型**</span><span class="sxs-lookup"><span data-stu-id="23857-114">**Type**</span></span>|<span data-ttu-id="23857-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="23857-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23857-116">Row</span><span class="sxs-lookup"><span data-stu-id="23857-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="23857-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="23857-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23857-118">属性</span><span class="sxs-lookup"><span data-stu-id="23857-118">Attributes</span></span>

<span data-ttu-id="23857-119">なし。</span><span class="sxs-lookup"><span data-stu-id="23857-119">None.</span></span>
  
