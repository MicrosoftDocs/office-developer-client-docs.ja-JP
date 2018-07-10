---
title: PidTag7BitDisplayName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4ae7645e45efb461ac53b6718569d909cec76504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802404"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="440dc-103">PidTag7BitDisplayName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="440dc-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="440dc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="440dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="440dc-105">メッセージング ユーザーの名前の 7 ビット ASCII 表現が含まれています。</span><span class="sxs-lookup"><span data-stu-id="440dc-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="440dc-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="440dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="440dc-107">PR_7BIT_DISPLAY_NAME、PR_7BIT_DISPLAY_NAME_A、PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="440dc-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="440dc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="440dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="440dc-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="440dc-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="440dc-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="440dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="440dc-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="440dc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="440dc-112">領域:</span><span class="sxs-lookup"><span data-stu-id="440dc-112">Area:</span></span>  <br/> |<span data-ttu-id="440dc-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="440dc-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="440dc-114">備考</span><span class="sxs-lookup"><span data-stu-id="440dc-114">Remarks</span></span>

<span data-ttu-id="440dc-115">これらのプロパティは、7 ビットの文字セットに**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティをマップします。</span><span class="sxs-lookup"><span data-stu-id="440dc-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="440dc-116">インターネットや特定の X.400 リンクなど、いくつかのメッセージング システムでは、7 ビット ASCII の 128 文字コード セットに制限されます。</span><span class="sxs-lookup"><span data-stu-id="440dc-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="440dc-117">このようなメッセージング システムへのゲートウェイは、これを取得するには、直接の[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)メソッドを呼び出すことによって、パフォーマンスを向上することができますプロパティは、コード変換のための余分な処理を回避します。</span><span class="sxs-lookup"><span data-stu-id="440dc-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="440dc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="440dc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="440dc-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="440dc-119">Protocol specifications</span></span>

<span data-ttu-id="440dc-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="440dc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="440dc-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="440dc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="440dc-122">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="440dc-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="440dc-123">プロパティとユーザー、連絡先、グループ、およびリソースのリストに対する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="440dc-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="440dc-124">[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="440dc-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="440dc-125">NSPI サーバーとクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="440dc-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="440dc-126">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="440dc-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="440dc-127">クライアントとサーバー間でデータを転送するために使用される順序とデータのフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="440dc-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="440dc-128">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="440dc-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="440dc-129">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="440dc-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="440dc-130">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="440dc-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="440dc-131">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="440dc-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="440dc-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="440dc-132">Header files</span></span>

<span data-ttu-id="440dc-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="440dc-133">Mapitags.h</span></span>
  
> <span data-ttu-id="440dc-134">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="440dc-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="440dc-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="440dc-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="440dc-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="440dc-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="440dc-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="440dc-137">See also</span></span>



[<span data-ttu-id="440dc-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="440dc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="440dc-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="440dc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="440dc-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="440dc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="440dc-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="440dc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
