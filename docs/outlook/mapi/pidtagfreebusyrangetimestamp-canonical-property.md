---
title: PidTagFreeBusyRangeTimestamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24c3369d1d6db4977d26e4d31678a4f2cc5808a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316178"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="3216e-103">PidTagFreeBusyRangeTimestamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3216e-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="3216e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3216e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3216e-105">データが公開された時刻を格納します。</span><span class="sxs-lookup"><span data-stu-id="3216e-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3216e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3216e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3216e-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="3216e-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="3216e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3216e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3216e-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="3216e-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="3216e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3216e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3216e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3216e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3216e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3216e-112">Area:</span></span>  <br/> |<span data-ttu-id="3216e-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="3216e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3216e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3216e-114">Remarks</span></span>

<span data-ttu-id="3216e-115">このプロパティは、協定世界時 (UTC) の 1601 年 1 月 1 日午前 0 時からの分数です。</span><span class="sxs-lookup"><span data-stu-id="3216e-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3216e-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3216e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3216e-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3216e-117">Protocol specifications</span></span>

<span data-ttu-id="3216e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3216e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3216e-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3216e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3216e-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3216e-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3216e-121">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="3216e-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3216e-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3216e-122">Header files</span></span>

<span data-ttu-id="3216e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3216e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3216e-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3216e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3216e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3216e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3216e-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3216e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3216e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="3216e-127">See also</span></span>



[<span data-ttu-id="3216e-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3216e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3216e-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3216e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3216e-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3216e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3216e-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3216e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

