---
title: RuleInfo_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0a0ac32729b83a5d648b2826bffe5a9df4d9fc0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806316"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="cf511-102">RuleInfo_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="cf511-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cf511-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cf511-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf511-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cf511-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cf511-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cf511-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cf511-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cf511-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cf511-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="cf511-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cf511-108">なし</span><span class="sxs-lookup"><span data-stu-id="cf511-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf511-109">定義</span><span class="sxs-lookup"><span data-stu-id="cf511-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf511-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cf511-110">Elements and attributes</span></span>

<span data-ttu-id="cf511-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf511-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cf511-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cf511-112">Child elements</span></span>

<span data-ttu-id="cf511-113">なし。</span><span class="sxs-lookup"><span data-stu-id="cf511-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf511-114">属性</span><span class="sxs-lookup"><span data-stu-id="cf511-114">Attributes</span></span>

|<span data-ttu-id="cf511-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="cf511-115">**Attribute**</span></span>|<span data-ttu-id="cf511-116">**型**</span><span class="sxs-lookup"><span data-stu-id="cf511-116">**Type**</span></span>|<span data-ttu-id="cf511-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="cf511-117">**Required**</span></span>|<span data-ttu-id="cf511-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="cf511-118">**Description**</span></span>|<span data-ttu-id="cf511-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="cf511-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf511-120">規則 Id</span><span class="sxs-lookup"><span data-stu-id="cf511-120">RuleID</span></span>  <br/> |<span data-ttu-id="cf511-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf511-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf511-122">必須</span><span class="sxs-lookup"><span data-stu-id="cf511-122">required</span></span>  <br/> ||<span data-ttu-id="cf511-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf511-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf511-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="cf511-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="cf511-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf511-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf511-126">必須</span><span class="sxs-lookup"><span data-stu-id="cf511-126">required</span></span>  <br/> ||<span data-ttu-id="cf511-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf511-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   
