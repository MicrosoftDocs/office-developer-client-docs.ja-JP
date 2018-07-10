---
title: PidLidSideEffects の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802161"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="3dc3d-103">PidLidSideEffects の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3dc3d-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="3dc3d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3dc3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3dc3d-105">メッセージ オブジェクトの処理方法によって、クライアント エンド ・ ユーザーの入力で動作している場合を制御します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3dc3d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3dc3d-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="3dc3d-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="3dc3d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3dc3d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3dc3d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3dc3d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3dc3d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3dc3d-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="3dc3d-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="3dc3d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3dc3d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3dc3d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3dc3d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="3dc3d-114">Area:</span></span>  <br/> |<span data-ttu-id="3dc3d-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="3dc3d-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3dc3d-116">備考</span><span class="sxs-lookup"><span data-stu-id="3dc3d-116">Remarks</span></span>

<span data-ttu-id="3dc3d-117">ビットごとまたは 0 個以上の以下のフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="3dc3d-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="3dc3d-118">**Name**</span></span>|<span data-ttu-id="3dc3d-119">**値**</span><span class="sxs-lookup"><span data-stu-id="3dc3d-119">**Value**</span></span>|<span data-ttu-id="3dc3d-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="3dc3d-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3dc3d-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="3dc3d-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="3dc3d-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="3dc3d-122">0x0001</span></span>  <br/> |<span data-ttu-id="3dc3d-123">削除するときに、メッセージ オブジェクトの追加の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="3dc3d-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="3dc3d-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="3dc3d-125">0x0008</span></span>  <br/> |<span data-ttu-id="3dc3d-126">UI は、メッセージ オブジェクトに関連付けられているではありません。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="3dc3d-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="3dc3d-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="3dc3d-128">0x0010</span></span>  <br/> |<span data-ttu-id="3dc3d-129">"IPF の**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) のプロパティを使用してフォルダーのオブジェクトに移動またはコピーするときは、メッセージ オブジェクトに追加の処理が必要。"注意してください。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="3dc3d-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="3dc3d-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="3dc3d-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="3dc3d-131">0x0020</span></span>  <br/> |<span data-ttu-id="3dc3d-132">別のフォルダーにコピーするとき、メッセージ オブジェクトに追加の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="3dc3d-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="3dc3d-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="3dc3d-134">0x0040</span></span>  <br/> |<span data-ttu-id="3dc3d-135">別のフォルダーに移動するときは、メッセージ オブジェクトの追加の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="3dc3d-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="3dc3d-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="3dc3d-137">0x0100</span></span>  <br/> |<span data-ttu-id="3dc3d-138">エンド ・ ユーザーに動詞を表示する場合、メッセージ オブジェクトに追加の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="3dc3d-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="3dc3d-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="3dc3d-140">0x0400</span></span>  <br/> |<span data-ttu-id="3dc3d-141">削除操作を元に戻すことはできません、"seOpenToDelete"が設定されていない限り、設定されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="3dc3d-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="3dc3d-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="3dc3d-143">0x0800</span></span>  <br/> |<span data-ttu-id="3dc3d-144">コピー操作を元に戻すことはできません、"seOpenTocopy"が設定されていない限り、設定されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="3dc3d-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="3dc3d-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="3dc3d-146">0x1000</span></span>  <br/> |<span data-ttu-id="3dc3d-147">移動操作を元に戻すことはできません、"seOpenToMove"が設定されていない限り、設定されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="3dc3d-148">seHasScript</span></span>  <br/> |<span data-ttu-id="3dc3d-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="3dc3d-149">0x2000</span></span>  <br/> |<span data-ttu-id="3dc3d-150">メッセージ オブジェクトには、エンド ・ ユーザーのスクリプトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="3dc3d-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="3dc3d-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="3dc3d-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="3dc3d-152">0x4000</span></span>  <br/> |<span data-ttu-id="3dc3d-153">追加の処理は、メッセージ オブジェクトを完全に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3dc3d-154">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3dc3d-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3dc3d-155">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3dc3d-155">Protocol specifications</span></span>

<span data-ttu-id="3dc3d-156">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3dc3d-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3dc3d-157">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3dc3d-158">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3dc3d-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3dc3d-159">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3dc3d-160">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3dc3d-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3dc3d-161">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3dc3d-162">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3dc3d-162">Header files</span></span>

<span data-ttu-id="3dc3d-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3dc3d-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="3dc3d-164">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3dc3d-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="3dc3d-165">See also</span></span>



[<span data-ttu-id="3dc3d-166">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3dc3d-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3dc3d-167">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3dc3d-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3dc3d-168">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3dc3d-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3dc3d-169">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3dc3d-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
