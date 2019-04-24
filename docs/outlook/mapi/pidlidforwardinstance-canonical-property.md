---
title: PidLidForwardInstance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357772"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="0c496-103">PidLidForwardInstance 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c496-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="0c496-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c496-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c496-105">会議出席依頼が定期的なアイテムに対する例外を表しており、開催者によって送信される招待ではなく、(開催者によって転送された場合でも) 転送されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="0c496-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c496-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0c496-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c496-107">dispidfwrdinstance</span><span class="sxs-lookup"><span data-stu-id="0c496-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="0c496-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="0c496-108">Property set:</span></span>  <br/> |<span data-ttu-id="0c496-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0c496-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0c496-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0c496-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0c496-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="0c496-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="0c496-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0c496-112">Data type:</span></span>  <br/> |<span data-ttu-id="0c496-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0c496-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0c496-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="0c496-114">Area:</span></span>  <br/> |<span data-ttu-id="0c496-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="0c496-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c496-116">解説</span><span class="sxs-lookup"><span data-stu-id="0c496-116">Remarks</span></span>

<span data-ttu-id="0c496-117">このプロパティの値が FALSE の場合、会議出席依頼は転送されたインスタンスではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="0c496-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="0c496-118">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="0c496-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c496-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0c496-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c496-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0c496-120">Protocol specifications</span></span>

<span data-ttu-id="0c496-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c496-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c496-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c496-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c496-123">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c496-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c496-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c496-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c496-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0c496-125">Header files</span></span>

<span data-ttu-id="0c496-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c496-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c496-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c496-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c496-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c496-128">See also</span></span>



[<span data-ttu-id="0c496-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0c496-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c496-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c496-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c496-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c496-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c496-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c496-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

