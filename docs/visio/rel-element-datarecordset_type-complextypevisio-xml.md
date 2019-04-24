---
title: Rel 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: 関連付けられた recordset とデータバインド情報を持つパーツへのリレーションシップを指定します。
ms.openlocfilehash: ca3584cfa8f1791e126d867a541de1fe9ec4b354
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360159"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="84094-103">Rel 要素 (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="84094-103">Rel element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="84094-104">関連付けられた recordset とデータバインド情報を持つパーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="84094-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84094-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="84094-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84094-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="84094-106">**Element type**</span></span> <br/> |[<span data-ttu-id="84094-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="84094-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="84094-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="84094-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="84094-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="84094-109">**Schema file**</span></span> <br/> |<span data-ttu-id="84094-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="84094-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="84094-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="84094-111">**Document parts**</span></span> <br/> |<span data-ttu-id="84094-112">system.xml、masters、config.xml、pages、page # .xml、.master (.xml)</span><span class="sxs-lookup"><span data-stu-id="84094-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="84094-113">定義</span><span class="sxs-lookup"><span data-stu-id="84094-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="84094-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="84094-114">Elements and attributes</span></span>

<span data-ttu-id="84094-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84094-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="84094-116">親要素</span><span class="sxs-lookup"><span data-stu-id="84094-116">Parent elements</span></span>

|<span data-ttu-id="84094-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="84094-117">**Element**</span></span>|<span data-ttu-id="84094-118">**型**</span><span class="sxs-lookup"><span data-stu-id="84094-118">**Type**</span></span>|<span data-ttu-id="84094-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="84094-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="84094-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="84094-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="84094-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="84094-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="84094-122">図面に格納されている recordset の1つのインスタンスとデータバインド情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="84094-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="84094-123">子要素</span><span class="sxs-lookup"><span data-stu-id="84094-123">Child elements</span></span>

<span data-ttu-id="84094-124">なし。</span><span class="sxs-lookup"><span data-stu-id="84094-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84094-125">属性</span><span class="sxs-lookup"><span data-stu-id="84094-125">Attributes</span></span>

|<span data-ttu-id="84094-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="84094-126">**Attribute**</span></span>|<span data-ttu-id="84094-127">**型**</span><span class="sxs-lookup"><span data-stu-id="84094-127">**Type**</span></span>|<span data-ttu-id="84094-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="84094-128">**Required**</span></span>|<span data-ttu-id="84094-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="84094-129">**Description**</span></span>|<span data-ttu-id="84094-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="84094-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="84094-131">r: id</span><span class="sxs-lookup"><span data-stu-id="84094-131">r:id</span></span>  <br/> |<span data-ttu-id="84094-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="84094-132">xsd:string</span></span>  <br/> <span data-ttu-id="84094-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84094-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="84094-134">必須</span><span class="sxs-lookup"><span data-stu-id="84094-134">required</span></span>  <br/> |<span data-ttu-id="84094-135">パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="84094-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="84094-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="84094-136">"rId#"</span></span>  <br/> <span data-ttu-id="84094-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84094-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84094-138">解説</span><span class="sxs-lookup"><span data-stu-id="84094-138">Remarks</span></span>

<span data-ttu-id="84094-139">**r: id**属性の値は、 **ST_RelationshipID**型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="84094-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="84094-140">**ST_RelationshipID** type は、' rId # ' という形式で指定する必要があります。最後の文字は数字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="84094-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="84094-141">この数値は、 **Rel**要素のすべての兄弟要素の間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="84094-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="84094-142">ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 Part 1 の仕様](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84094-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

