---
title: PidLidDistributionListOneOffMembers の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ae6202a1fdf7ec43bf2269236aa8120aa67e3c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801880"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="37aea-103">PidLidDistributionListOneOffMembers の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="37aea-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="37aea-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="37aea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="37aea-105">個人用配布リストのメンバーに対応する 1 回限りのエントリ Id の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="37aea-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37aea-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="37aea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37aea-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="37aea-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="37aea-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37aea-108">Property set:</span></span>  <br/> |<span data-ttu-id="37aea-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="37aea-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="37aea-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="37aea-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37aea-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="37aea-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="37aea-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="37aea-112">Data type:</span></span>  <br/> |<span data-ttu-id="37aea-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="37aea-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="37aea-114">領域:</span><span class="sxs-lookup"><span data-stu-id="37aea-114">Area:</span></span>  <br/> |<span data-ttu-id="37aea-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="37aea-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37aea-116">備考</span><span class="sxs-lookup"><span data-stu-id="37aea-116">Remarks</span></span>

<span data-ttu-id="37aea-117">これらの一時エントリ Id は、表示名と個人用配布リストのメンバーの電子メール アドレスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="37aea-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="37aea-118">**DispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) プロパティを使用して同期する必要があります、クライアントまたはサーバーは、このプロパティを設定する場合: [ **dispidDLOneOffMembers** ] プロパティのエントリごとに、必要がありますエントリと同じで**dispidDLMembers**プロパティに配置します。</span><span class="sxs-lookup"><span data-stu-id="37aea-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="37aea-119">**DispidDLOneOffMembers**を設定するとき、クライアントまたはサーバーする必要があることを確認の合計サイズ 15,000 バイト未満のサイズ。</span><span class="sxs-lookup"><span data-stu-id="37aea-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37aea-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="37aea-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37aea-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="37aea-121">Protocol specifications</span></span>

<span data-ttu-id="37aea-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37aea-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37aea-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="37aea-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37aea-124">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37aea-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37aea-125">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="37aea-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37aea-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="37aea-126">Header files</span></span>

<span data-ttu-id="37aea-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37aea-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="37aea-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="37aea-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37aea-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="37aea-129">See also</span></span>



[<span data-ttu-id="37aea-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="37aea-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37aea-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="37aea-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37aea-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="37aea-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37aea-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="37aea-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
