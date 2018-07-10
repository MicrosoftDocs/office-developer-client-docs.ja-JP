---
title: PidLidAppointmentNotAllowPropose の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentNotAllowPropose
api_type:
- COM
ms.assetid: 8be9e2aa-2dc1-406d-8864-7f556de22809
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 183c8eb5112fc35f088bc5c6ac11748e3449f15a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801725"
---
# <a name="pidlidappointmentnotallowpropose-canonical-property"></a><span data-ttu-id="a14cc-103">PidLidAppointmentNotAllowPropose の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a14cc-103">PidLidAppointmentNotAllowPropose Canonical Property</span></span>

  
  
<span data-ttu-id="a14cc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a14cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a14cc-105">出席者が会議の新しい日時を提案するために使用できないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-105">Indicates whether attendees are not allowed to propose a new date/time for the meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a14cc-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a14cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a14cc-107">dispidApptNotAllowPropose</span><span class="sxs-lookup"><span data-stu-id="a14cc-107">dispidApptNotAllowPropose</span></span>  <br/> |
|<span data-ttu-id="a14cc-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="a14cc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a14cc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a14cc-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a14cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a14cc-111">0x0000825A</span><span class="sxs-lookup"><span data-stu-id="a14cc-111">0x0000825A</span></span>  <br/> |
|<span data-ttu-id="a14cc-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="a14cc-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a14cc-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a14cc-114">領域:</span><span class="sxs-lookup"><span data-stu-id="a14cc-114">Area:</span></span>  <br/> |<span data-ttu-id="a14cc-115">会議</span><span class="sxs-lookup"><span data-stu-id="a14cc-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a14cc-116">備考</span><span class="sxs-lookup"><span data-stu-id="a14cc-116">Remarks</span></span>

<span data-ttu-id="a14cc-117">値 FALSE、またはこのプロパティがない場合は、出席者が新しい日時を提案するために許可されてことを示します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-117">A value of FALSE, or the absence of this property indicates that the attendees are allowed to propose a new date/time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a14cc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a14cc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a14cc-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a14cc-119">Protocol specifications</span></span>

<span data-ttu-id="a14cc-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a14cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a14cc-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a14cc-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a14cc-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a14cc-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a14cc-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a14cc-124">Header files</span></span>

<span data-ttu-id="a14cc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a14cc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a14cc-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a14cc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a14cc-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a14cc-127">See also</span></span>



[<span data-ttu-id="a14cc-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a14cc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a14cc-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a14cc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a14cc-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a14cc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a14cc-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a14cc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
