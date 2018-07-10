---
title: PidLidClipEnd の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1353289da2b428fb58adecc6f7830a2eea4b519a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801848"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="a7e9d-103">PidLidClipEnd の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a7e9d-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="a7e9d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7e9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7e9d-105">カレンダー オブジェクトのインスタンスを 1 つのイベントの終了日時に世界協定時刻 (UTC) を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7e9d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7e9d-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="a7e9d-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="a7e9d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-108">Property set:</span></span>  <br/> |<span data-ttu-id="a7e9d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a7e9d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a7e9d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a7e9d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a7e9d-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="a7e9d-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="a7e9d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-112">Data type:</span></span>  <br/> |<span data-ttu-id="a7e9d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a7e9d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a7e9d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="a7e9d-114">Area:</span></span>  <br/> |<span data-ttu-id="a7e9d-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="a7e9d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7e9d-116">備考</span><span class="sxs-lookup"><span data-stu-id="a7e9d-116">Remarks</span></span>

<span data-ttu-id="a7e9d-117">カレンダー オブジェクトのインスタンスを 1 つのイベントの終了日時を UTC で指定します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="a7e9d-118">定期的な一連のこのプロパティを指定の午前 0 時 (UTC) での定期的な系列の最後のインスタンスの日付に定期的に終了すると、大文字と小文字の値が 31 年 8 月をする必要がありますがあるない場合を除き、4500、午後 11 時 59 分</span><span class="sxs-lookup"><span data-stu-id="a7e9d-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="a7e9d-119">このプロパティの値は、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7e9d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a7e9d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7e9d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a7e9d-121">Protocol specifications</span></span>

<span data-ttu-id="a7e9d-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7e9d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7e9d-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7e9d-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7e9d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7e9d-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7e9d-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a7e9d-126">Header files</span></span>

<span data-ttu-id="a7e9d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7e9d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7e9d-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7e9d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a7e9d-129">See also</span></span>



[<span data-ttu-id="a7e9d-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7e9d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7e9d-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7e9d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7e9d-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a7e9d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7e9d-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a7e9d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
