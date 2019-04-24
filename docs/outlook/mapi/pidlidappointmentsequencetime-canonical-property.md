---
title: PidLidAppointmentSequenceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSequenceTime
api_type:
- COM
ms.assetid: 0170bb9b-f43b-4089-9144-b8652c38f43d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d5daa2672fb0b392c4f01492c4dcd36bdac3ba2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345389"
---
# <a name="pidlidappointmentsequencetime-canonical-property"></a><span data-ttu-id="e833d-103">PidLidAppointmentSequenceTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e833d-103">PidLidAppointmentSequenceTime Canonical Property</span></span>

  
  
<span data-ttu-id="e833d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e833d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e833d-105">このプロパティが最後に変更された日付と時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="e833d-105">Specifies the date and time at which this property was last modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e833d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e833d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e833d-107">dispidApptSeqTime</span><span class="sxs-lookup"><span data-stu-id="e833d-107">dispidApptSeqTime</span></span>  <br/> |
|<span data-ttu-id="e833d-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="e833d-108">Property set:</span></span>  <br/> |<span data-ttu-id="e833d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e833d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e833d-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e833d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e833d-111">0x00008202</span><span class="sxs-lookup"><span data-stu-id="e833d-111">0x00008202</span></span>  <br/> |
|<span data-ttu-id="e833d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e833d-112">Data type:</span></span>  <br/> |<span data-ttu-id="e833d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e833d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e833d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e833d-114">Area:</span></span>  <br/> |<span data-ttu-id="e833d-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="e833d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e833d-116">解説</span><span class="sxs-lookup"><span data-stu-id="e833d-116">Remarks</span></span>

<span data-ttu-id="e833d-117">値は協定世界時 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e833d-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e833d-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e833d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e833d-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e833d-119">Protocol specifications</span></span>

<span data-ttu-id="e833d-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e833d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e833d-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e833d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e833d-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e833d-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e833d-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e833d-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e833d-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e833d-124">Header files</span></span>

<span data-ttu-id="e833d-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e833d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e833d-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e833d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e833d-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e833d-127">See also</span></span>



[<span data-ttu-id="e833d-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e833d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e833d-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e833d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e833d-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e833d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e833d-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e833d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

