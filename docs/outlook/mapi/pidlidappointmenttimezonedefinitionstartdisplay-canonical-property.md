---
title: PidLidAppointmentTimeZoneDefinitionStartDisplay の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801826"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="c99d7-103">PidLidAppointmentTimeZoneDefinitionStartDisplay の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c99d7-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="c99d7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c99d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c99d7-105">単独の予定または会議出席依頼の開始時刻を選択するために使用されるタイム ゾーンの説明を格納する[TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造体の保存形式に対応するストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c99d7-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c99d7-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c99d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c99d7-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="c99d7-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="c99d7-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c99d7-108">Property set:</span></span>  <br/> |<span data-ttu-id="c99d7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c99d7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c99d7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c99d7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c99d7-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="c99d7-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="c99d7-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c99d7-112">Data type:</span></span>  <br/> |<span data-ttu-id="c99d7-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c99d7-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c99d7-114">領域:</span><span class="sxs-lookup"><span data-stu-id="c99d7-114">Area:</span></span>  <br/> |<span data-ttu-id="c99d7-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="c99d7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c99d7-116">備考</span><span class="sxs-lookup"><span data-stu-id="c99d7-116">Remarks</span></span>

<span data-ttu-id="c99d7-117">2003 または以前のバージョンを Microsoft Office Outlook とソリューションにコラボレーション データ オブジェクト (CDO) 1.2.1 を置くし、Outlook または Microsoft Exchange Server では、予定表更新ツールを実行していないことは、シングル ・ インスタンスの終了時刻と開始時刻を格納します。予定および会議出席依頼で世界協定時刻 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="c99d7-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c99d7-118">これらのクライアントは、予定または会議出席依頼が作成されるタイム ゾーンの情報を格納していません。</span><span class="sxs-lookup"><span data-stu-id="c99d7-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="c99d7-119">、Microsoft Office Outlook 2007 と Outlook または Exchange Server の予定表更新ツールを実行している CDO 1.2.1 ベースのソリューションは、このプロパティを使用して、開始時刻のタイム ゾーンを格納するための Outlook のバージョン。</span><span class="sxs-lookup"><span data-stu-id="c99d7-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="c99d7-120">**DispidApptTZDefStartDisplay**プロパティは、元のタイム ゾーンでの予定または会議を示していますが予定されているを提供。</span><span class="sxs-lookup"><span data-stu-id="c99d7-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="c99d7-121">タイム ゾーンの規則を変更する場合に、開始時刻を調整する必要があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c99d7-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="c99d7-122">このプロパティが存在しない場合は、現在のローカル タイム ゾーンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="c99d7-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="c99d7-123">このプロパティは、表示目的でのみ使用されるが、定期的なアイテムの展開で使用されていません。</span><span class="sxs-lookup"><span data-stu-id="c99d7-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="c99d7-124">パーサーは、 **dispidApptTZDefStartDisplay**などのバイナリのプロパティへの取り組みのためのストリームに**TZDEFINITION**が引き続き発生する場合や、このプロパティから取得したストリームを読み取るとき注意が必要である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c99d7-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="c99d7-125">詳細については、[バイナリのプロパティをコミットするためのストリームに永続化する TZDEFINITION](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c99d7-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="c99d7-126">このプロパティは、 **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) のプロパティのタイム ゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="c99d7-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="c99d7-127">UTC からの開始日と時刻を表示のためのローカル タイム ゾーンに変換するのには、 **dispidApptTZDefStartDisplay**の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c99d7-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="c99d7-128">各**TZRULE**このプロパティで指定された、TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="c99d7-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="c99d7-129">たとえば、 **TZRULE**が有効なルールの場合は、 **TZRULE**フィールドの値必要があります「0x0002」です。それ以外の場合、"0x0000"である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c99d7-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c99d7-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c99d7-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c99d7-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c99d7-131">Protocol specifications</span></span>

<span data-ttu-id="c99d7-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c99d7-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c99d7-133">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照が用意されています。</span><span class="sxs-lookup"><span data-stu-id="c99d7-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="c99d7-134">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c99d7-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c99d7-135">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c99d7-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c99d7-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c99d7-136">Header files</span></span>

<span data-ttu-id="c99d7-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c99d7-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="c99d7-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c99d7-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c99d7-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="c99d7-139">See also</span></span>



[<span data-ttu-id="c99d7-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c99d7-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c99d7-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c99d7-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c99d7-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c99d7-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c99d7-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c99d7-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
