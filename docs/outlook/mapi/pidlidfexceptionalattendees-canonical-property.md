---
title: PidLidFExceptionalAttendees 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 544b5b5ac945eeedf787af0e311491da1f9d0217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327476"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="a3384-103">PidLidFExceptionalAttendees 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a3384-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="a3384-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3384-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3384-105">このプロパティが1つ以上の例外を持つ定期的な予定表オブジェクトであるかどうか、および少なくとも1つの例外が埋め込まれたメッセージに、少なくとも1つの [受信者] 行があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a3384-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3384-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a3384-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3384-107">dispidfexceptionalattendees 者</span><span class="sxs-lookup"><span data-stu-id="a3384-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="a3384-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a3384-108">Property set:</span></span>  <br/> |<span data-ttu-id="a3384-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a3384-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a3384-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a3384-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a3384-111">0x0000822b</span><span class="sxs-lookup"><span data-stu-id="a3384-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="a3384-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a3384-112">Data type:</span></span>  <br/> |<span data-ttu-id="a3384-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a3384-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a3384-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a3384-114">Area:</span></span>  <br/> |<span data-ttu-id="a3384-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="a3384-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3384-116">解説</span><span class="sxs-lookup"><span data-stu-id="a3384-116">Remarks</span></span>

<span data-ttu-id="a3384-117">値が FALSE の場合、またはこのプロパティが指定されていない場合は、calendar オブジェクトが例外を持たないか、または埋め込みメッセージに [受信者行] が含まれていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="a3384-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a3384-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a3384-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3384-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a3384-119">Protocol specifications</span></span>

<span data-ttu-id="a3384-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3384-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3384-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a3384-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3384-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3384-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3384-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a3384-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3384-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a3384-124">Header files</span></span>

<span data-ttu-id="a3384-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3384-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3384-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a3384-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3384-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3384-127">See also</span></span>



[<span data-ttu-id="a3384-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a3384-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3384-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a3384-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3384-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a3384-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3384-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a3384-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

