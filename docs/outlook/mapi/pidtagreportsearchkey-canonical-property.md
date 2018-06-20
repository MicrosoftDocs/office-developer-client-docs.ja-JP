---
title: PidTagReportSearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fa2770daf38fe93eb9fb69990eebc2a6fcfd6a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803356"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="6f13b-103">PidTagReportSearchKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6f13b-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="6f13b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f13b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f13b-105">このメッセージのレポートを取得する必要があります受信者の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f13b-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f13b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6f13b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f13b-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="6f13b-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="6f13b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6f13b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f13b-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="6f13b-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="6f13b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6f13b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f13b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f13b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f13b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6f13b-112">Area:</span></span>  <br/> |<span data-ttu-id="6f13b-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="6f13b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f13b-114">備考</span><span class="sxs-lookup"><span data-stu-id="6f13b-114">Remarks</span></span>

<span data-ttu-id="6f13b-115">このプロパティは、このメッセージに対して生成されたすべてのレポートを受信する送信者を委任した受信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="6f13b-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="6f13b-116">レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f13b-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="6f13b-117">設定されていない場合、レポートは、メッセージの送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="6f13b-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f13b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6f13b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f13b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6f13b-119">Protocol specifications</span></span>

<span data-ttu-id="6f13b-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f13b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f13b-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f13b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f13b-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f13b-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f13b-123">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6f13b-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f13b-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6f13b-124">Header files</span></span>

<span data-ttu-id="6f13b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f13b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f13b-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f13b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f13b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f13b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6f13b-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f13b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f13b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f13b-129">See also</span></span>



[<span data-ttu-id="6f13b-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f13b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f13b-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f13b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f13b-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6f13b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f13b-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6f13b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

