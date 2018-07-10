---
title: PidLidExceptionReplaceTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2292d53997fd4d54e9272789be83ea94a93c6a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801914"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="bef07-103">PidLidExceptionReplaceTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bef07-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="bef07-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bef07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bef07-105">内での定期的な例外を置き換えるときの日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="bef07-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bef07-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bef07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bef07-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="bef07-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="bef07-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="bef07-108">Property set:</span></span>  <br/> |<span data-ttu-id="bef07-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bef07-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bef07-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bef07-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bef07-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="bef07-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="bef07-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bef07-112">Data type:</span></span>  <br/> |<span data-ttu-id="bef07-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bef07-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bef07-114">領域:</span><span class="sxs-lookup"><span data-stu-id="bef07-114">Area:</span></span>  <br/> |<span data-ttu-id="bef07-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="bef07-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bef07-116">備考</span><span class="sxs-lookup"><span data-stu-id="bef07-116">Remarks</span></span>

<span data-ttu-id="bef07-117">値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bef07-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="bef07-118">このプロパティは、例外の添付オブジェクトを検索する特定のインスタンスを使用します。</span><span class="sxs-lookup"><span data-stu-id="bef07-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bef07-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bef07-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bef07-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bef07-120">Protocol specifications</span></span>

<span data-ttu-id="bef07-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef07-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef07-122">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bef07-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="bef07-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef07-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef07-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bef07-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bef07-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bef07-125">Header files</span></span>

<span data-ttu-id="bef07-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bef07-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bef07-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bef07-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bef07-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="bef07-128">See also</span></span>



[<span data-ttu-id="bef07-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bef07-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bef07-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bef07-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bef07-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bef07-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bef07-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bef07-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
