---
title: PidTagReportTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 298c53e537819f800a3acc5cf07c01a7b9f978ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330150"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="3b0bc-103">PidTagReportTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b0bc-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="3b0bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b0bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b0bc-105">メッセージング システムがレポートを生成した日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b0bc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3b0bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b0bc-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="3b0bc-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="3b0bc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3b0bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b0bc-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="3b0bc-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="3b0bc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3b0bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b0bc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3b0bc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3b0bc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3b0bc-112">Area:</span></span>  <br/> |<span data-ttu-id="3b0bc-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="3b0bc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b0bc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3b0bc-114">Remarks</span></span>

<span data-ttu-id="3b0bc-115">このプロパティは、配信レポートと配信不能レポートの受信者ごとのプロパティと、読み取りレポートと非読み取りレポートのメッセージごとのプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3b0bc-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3b0bc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b0bc-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3b0bc-117">Protocol specifications</span></span>

<span data-ttu-id="3b0bc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b0bc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b0bc-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b0bc-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b0bc-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b0bc-121">電子メール メッセージで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="3b0bc-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b0bc-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b0bc-123">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b0bc-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3b0bc-124">Header files</span></span>

<span data-ttu-id="3b0bc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b0bc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b0bc-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b0bc-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b0bc-127">Mapitags.h</span></span>
  
> <span data-ttu-id="3b0bc-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3b0bc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b0bc-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b0bc-129">See also</span></span>



[<span data-ttu-id="3b0bc-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3b0bc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b0bc-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b0bc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b0bc-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3b0bc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b0bc-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3b0bc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

