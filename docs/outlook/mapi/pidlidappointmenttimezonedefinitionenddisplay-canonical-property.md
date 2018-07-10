---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 119cd7edc5b9b615a39cea6aa1c405c396ce2afa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801813"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="8e8cf-103">PidLidAppointmentTimeZoneDefinitionEndDisplay の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8e8cf-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="8e8cf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e8cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e8cf-105">単独の予定または会議出席依頼の終了時刻が選択されているときに使用されるタイム ゾーンの説明を格納する[TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造体の保存形式に対応するストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e8cf-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e8cf-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="8e8cf-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="8e8cf-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e8cf-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8e8cf-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8e8cf-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8e8cf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e8cf-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="8e8cf-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="8e8cf-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e8cf-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8e8cf-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8e8cf-114">領域:</span><span class="sxs-lookup"><span data-stu-id="8e8cf-114">Area:</span></span>  <br/> |<span data-ttu-id="8e8cf-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="8e8cf-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e8cf-116">備考</span><span class="sxs-lookup"><span data-stu-id="8e8cf-116">Remarks</span></span>

<span data-ttu-id="8e8cf-117">2003 または以前のバージョンを Microsoft Office Outlook とソリューションにコラボレーション データ オブジェクト (CDO) 1.2.1 を置くし、Outlook または Microsoft Exchange Server では、予定表更新ツールを実行していないことは、シングル ・ インスタンスの終了時刻と開始時刻を格納します。予定および会議出席依頼で世界協定時刻 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8e8cf-118">これらのクライアントは、予定または会議出席依頼を作成する場所のタイム ゾーンの情報を格納していません。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="8e8cf-119">Outlook または Exchange Server の予定表を実行している Microsoft Office Outlook 2007 では、CDO 1.2.1 に基づくソリューションの以降の Microsoft Outlook のバージョンでは、終了時刻のタイム ゾーンを格納する使用**dispidApptTZDefEndDisplay**ツールを更新します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="8e8cf-120">**dispidApptTZDefEndDisplay**は、[スケジュールされた、タイム ゾーンの規則を変更する場合に、終了時刻を調整する必要があるかどうかを判断する元のタイム ゾーンで、予定または会議を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="8e8cf-121">このプロパティが存在しない場合は、 **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) のプロパティで指定されたタイム ゾーンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="8e8cf-122">**DispidApptTZDefStartDisplay**が存在しないか無効の場合は、現在のローカル タイム ゾーンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="8e8cf-123">**dispidApptTZDefEndDisplay**は、表示目的でのみ使用され、定期的なアイテムの展開で使用されていません。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="8e8cf-124">パーサーは、 **dispidApptTZDefEndDisplay**から取得したストリームを読み取るとき、または**dispidApptTZDefEndDisplay**などのバイナリのプロパティへの取り組みのためのストリームに**TZDEFINITION**が引き続き発生する場合注意が必要である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="8e8cf-125">詳細については、[バイナリのプロパティをコミットするためのストリームに永続化する TZDEFINITION](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="8e8cf-126">**dispidApptTZDefEndDisplay**は、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) のプロパティのタイム ゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="8e8cf-127">形式、制約、および**dispidApptTZDefEndDisplay**の計算は、 **dispidApptTZDefStartDisplay**プロパティで指定されたと同じです。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e8cf-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e8cf-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e8cf-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8e8cf-129">Protocol specifications</span></span>

<span data-ttu-id="8e8cf-130">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e8cf-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e8cf-131">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e8cf-132">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e8cf-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e8cf-133">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e8cf-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8e8cf-134">Header files</span></span>

<span data-ttu-id="8e8cf-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e8cf-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e8cf-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e8cf-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e8cf-137">See also</span></span>



[<span data-ttu-id="8e8cf-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e8cf-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e8cf-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e8cf-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e8cf-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8e8cf-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e8cf-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8e8cf-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
