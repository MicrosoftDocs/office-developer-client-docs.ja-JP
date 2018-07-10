---
title: PidLidReminderTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6e74dbb1f8e0e64feb2c86eb04e146e201089a4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802138"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="e576d-103">PidLidReminderTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e576d-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="e576d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e576d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e576d-105">アラームの初期のシグナルの時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="e576d-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e576d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e576d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e576d-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="e576d-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="e576d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e576d-108">Property set:</span></span>  <br/> |<span data-ttu-id="e576d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e576d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e576d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e576d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e576d-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="e576d-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="e576d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e576d-112">Data type:</span></span>  <br/> |<span data-ttu-id="e576d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e576d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e576d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e576d-114">Area:</span></span>  <br/> |<span data-ttu-id="e576d-115">アラーム</span><span class="sxs-lookup"><span data-stu-id="e576d-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e576d-116">備考</span><span class="sxs-lookup"><span data-stu-id="e576d-116">Remarks</span></span>

<span data-ttu-id="e576d-117">カレンダー オブジェクトは、このプロパティは、予定の開始時刻である場合、あるユーザーは、遅延時間で表します。</span><span class="sxs-lookup"><span data-stu-id="e576d-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="e576d-118">クライアントは、世界協定時刻 (UTC) で値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e576d-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e576d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e576d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e576d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e576d-120">Protocol specifications</span></span>

<span data-ttu-id="e576d-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e576d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e576d-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e576d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e576d-123">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e576d-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e576d-124">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e576d-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e576d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e576d-125">Header files</span></span>

<span data-ttu-id="e576d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e576d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e576d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e576d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e576d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e576d-128">See also</span></span>



[<span data-ttu-id="e576d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e576d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e576d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e576d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e576d-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e576d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e576d-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e576d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
