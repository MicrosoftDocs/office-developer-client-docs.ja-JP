---
title: PidTagScheduleInfoDisallowRecurringAppts 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330101"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="10162-103">PidTagScheduleInfoDisallowRecurringAppts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10162-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="10162-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10162-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10162-105">TRUE が含まれている場合、定期的な予定への自動応答は辞退します。</span><span class="sxs-lookup"><span data-stu-id="10162-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10162-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="10162-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10162-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="10162-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="10162-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="10162-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10162-109">0x686e</span><span class="sxs-lookup"><span data-stu-id="10162-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="10162-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="10162-110">Data type:</span></span>  <br/> |<span data-ttu-id="10162-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="10162-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="10162-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="10162-112">Area:</span></span>  <br/> |<span data-ttu-id="10162-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="10162-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10162-114">解説</span><span class="sxs-lookup"><span data-stu-id="10162-114">Remarks</span></span>

<span data-ttu-id="10162-115">このプロパティは、 **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) プロパティの値が TRUE の場合にのみ意味があります。</span><span class="sxs-lookup"><span data-stu-id="10162-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="10162-116">このプロパティが存在しない場合は、定期的な会議を承諾する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="10162-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="10162-117">これは必須のプロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="10162-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10162-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="10162-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10162-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="10162-119">Protocol specifications</span></span>

<span data-ttu-id="10162-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10162-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10162-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="10162-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10162-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10162-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10162-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="10162-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="10162-124">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10162-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10162-125">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="10162-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10162-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="10162-126">Header files</span></span>

<span data-ttu-id="10162-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10162-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="10162-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="10162-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="10162-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="10162-129">Mapitags.h</span></span>
  
> <span data-ttu-id="10162-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10162-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10162-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="10162-131">See also</span></span>



[<span data-ttu-id="10162-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="10162-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10162-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10162-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10162-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="10162-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10162-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="10162-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

