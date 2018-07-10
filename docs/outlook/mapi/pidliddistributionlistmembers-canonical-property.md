---
title: PidLidDistributionListMembers の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c27513474048e9805bc29116aa094bc47f8f0cae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801871"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="edd68-103">PidLidDistributionListMembers の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="edd68-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="edd68-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edd68-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edd68-105">個人用配布リストのメンバーに対応するオブジェクトのエントリ Id の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="edd68-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edd68-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="edd68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edd68-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="edd68-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="edd68-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="edd68-108">Property set:</span></span>  <br/> |<span data-ttu-id="edd68-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="edd68-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="edd68-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="edd68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="edd68-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="edd68-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="edd68-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="edd68-112">Data type:</span></span>  <br/> |<span data-ttu-id="edd68-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="edd68-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="edd68-114">領域:</span><span class="sxs-lookup"><span data-stu-id="edd68-114">Area:</span></span>  <br/> |<span data-ttu-id="edd68-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="edd68-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edd68-116">備考</span><span class="sxs-lookup"><span data-stu-id="edd68-116">Remarks</span></span>

<span data-ttu-id="edd68-117">個人用配布リストのメンバーには、他の個人用配布リスト、連絡先、グローバル アドレス一覧のユーザーまたは配布リスト、または 1 回限りの電子メール アドレスに含まれている電子メールのアドレスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="edd68-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="edd68-118">各エントリ Id の形式は、 [MS-OXCDATA](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定されている、1 回限りのエントリ Id またはラップのエントリ Id のいずれかにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd68-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="edd68-119">このプロパティを設定するとき、クライアントまたはサーバーを保証しなければならないの合計サイズ 15,000 バイト未満です。</span><span class="sxs-lookup"><span data-stu-id="edd68-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="edd68-120">このプロパティは、個人用配布リストのメンバーに対応する 1 回限りのエントリ Id の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="edd68-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="edd68-121">これらの一時エントリ Id は、表示名と個人用配布リストのメンバーの電子メール アドレスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="edd68-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="edd68-122">**DispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) のプロパティの各エントリに対してこのプロパティ**dispidDLMembers**同期する必要があるクライアントまたはサーバーは、このプロパティを設定する場合は、内のエントリが存在する必要があります、**dispidDLOneOffMembers**内の同じ位置です。</span><span class="sxs-lookup"><span data-stu-id="edd68-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edd68-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="edd68-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edd68-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="edd68-124">Protocol specifications</span></span>

<span data-ttu-id="edd68-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd68-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd68-126">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="edd68-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edd68-127">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd68-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd68-128">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="edd68-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edd68-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="edd68-129">Header files</span></span>

<span data-ttu-id="edd68-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edd68-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="edd68-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="edd68-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edd68-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="edd68-132">See also</span></span>



[<span data-ttu-id="edd68-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="edd68-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edd68-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="edd68-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edd68-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="edd68-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edd68-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="edd68-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
