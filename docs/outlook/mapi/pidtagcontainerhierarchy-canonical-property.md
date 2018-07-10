---
title: PidTagContainerHierarchy の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 691c5977092b5e2ca6b453209982dd1333a6df89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802605"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="aeeea-103">PidTagContainerHierarchy の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="aeeea-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="aeeea-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aeeea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aeeea-105">埋め込まれた階層テーブル オブジェクトに関する情報を提供、子コンテナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="aeeea-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aeeea-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="aeeea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aeeea-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="aeeea-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="aeeea-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aeeea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aeeea-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="aeeea-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="aeeea-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="aeeea-110">Data type:</span></span>  <br/> |<span data-ttu-id="aeeea-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="aeeea-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="aeeea-112">領域:</span><span class="sxs-lookup"><span data-stu-id="aeeea-112">Area:</span></span>  <br/> |<span data-ttu-id="aeeea-113">Container</span><span class="sxs-lookup"><span data-stu-id="aeeea-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aeeea-114">備考</span><span class="sxs-lookup"><span data-stu-id="aeeea-114">Remarks</span></span>

<span data-ttu-id="aeeea-115">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="aeeea-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="aeeea-116">**PT_OBJECT**の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) IID_IMAPITable のインタ フェース識別子を要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeeea-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="aeeea-117">サービス プロバイダーする必要がありますに報告して、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドが設定されているが報告したことができます (オプション)、または設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="aeeea-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="aeeea-118">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeeea-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="aeeea-119">詳細については、[階層テーブル](hierarchy-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aeeea-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="aeeea-120">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))、このプロパティは、使用状況と似ています。</span><span class="sxs-lookup"><span data-stu-id="aeeea-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="aeeea-121">いくつかの MAPI プロパティは、テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aeeea-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="aeeea-122">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="aeeea-122">**Property**</span></span>|<span data-ttu-id="aeeea-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="aeeea-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aeeea-124">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aeeea-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aeeea-125">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="aeeea-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="aeeea-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="aeeea-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="aeeea-127">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="aeeea-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="aeeea-128">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aeeea-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aeeea-129">関連付けられているコンテンツ」テーブル</span><span class="sxs-lookup"><span data-stu-id="aeeea-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="aeeea-130">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aeeea-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aeeea-131">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="aeeea-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="aeeea-132">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aeeea-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aeeea-133">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="aeeea-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="aeeea-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aeeea-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aeeea-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aeeea-135">Protocol specifications</span></span>

<span data-ttu-id="aeeea-136">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aeeea-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aeeea-137">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="aeeea-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aeeea-138">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aeeea-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aeeea-139">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="aeeea-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="aeeea-140">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aeeea-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aeeea-141">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="aeeea-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aeeea-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aeeea-142">Header files</span></span>

<span data-ttu-id="aeeea-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aeeea-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="aeeea-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aeeea-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="aeeea-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aeeea-145">Mapitags.h</span></span>
  
> <span data-ttu-id="aeeea-146">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aeeea-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aeeea-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="aeeea-147">See also</span></span>



[<span data-ttu-id="aeeea-148">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aeeea-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aeeea-149">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aeeea-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aeeea-150">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="aeeea-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aeeea-151">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="aeeea-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
