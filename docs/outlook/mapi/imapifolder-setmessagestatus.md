---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fcca6a7e8fa70a2df9042e8b3c2b28825cee9a7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800501"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="d5a48-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="d5a48-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="d5a48-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5a48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5a48-105">(たとえば、あるかどうかそのメッセージは削除対象としてマーク) は、メッセージに関連付けられたステータスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5a48-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="d5a48-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5a48-106">Parameters</span></span>

 <span data-ttu-id="d5a48-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d5a48-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d5a48-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="d5a48-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d5a48-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d5a48-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d5a48-110">[in]ステータスが設定されて、メッセージのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5a48-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="d5a48-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="d5a48-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="d5a48-112">[in]割り当てられる新しい状態です。</span><span class="sxs-lookup"><span data-stu-id="d5a48-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="d5a48-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="d5a48-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="d5a48-114">[in]新しい状態に適用され、フラグを設定することを示しますフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d5a48-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="d5a48-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d5a48-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d5a48-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="d5a48-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="d5a48-117">メッセージは、削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="d5a48-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="d5a48-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="d5a48-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="d5a48-119">メッセージは表示しません。</span><span class="sxs-lookup"><span data-stu-id="d5a48-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="d5a48-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="d5a48-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="d5a48-121">メッセージが表示されるが強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="d5a48-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="d5a48-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="d5a48-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="d5a48-123">メッセージは、ローカル クライアントにダウンロードすることがなくリモート メッセージ ストアを削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="d5a48-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="d5a48-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="d5a48-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="d5a48-125">メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロード用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="d5a48-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="d5a48-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="d5a48-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="d5a48-127">クライアント定義の目的は、メッセージをタグ付けされました。</span><span class="sxs-lookup"><span data-stu-id="d5a48-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="d5a48-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="d5a48-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="d5a48-129">[out]メッセージの前の状態へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5a48-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5a48-130">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d5a48-130">Return value</span></span>

<span data-ttu-id="d5a48-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5a48-131">S_OK</span></span> 
  
> <span data-ttu-id="d5a48-132">メッセージの状態が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="d5a48-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5a48-133">備考</span><span class="sxs-lookup"><span data-stu-id="d5a48-133">Remarks</span></span>

<span data-ttu-id="d5a48-134">**IMAPIFolder::SetMessageStatus**メソッドは、メッセージの状態を**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティに格納されている値に設定します。</span><span class="sxs-lookup"><span data-stu-id="d5a48-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d5a48-135">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="d5a48-135">Notes to implementers</span></span>

<span data-ttu-id="d5a48-136">メッセージのステータス ビットを設定、オフになっていると使用する方法によって異なります完全に、実装がビット 0 ~ 15 は予約されており、0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5a48-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="d5a48-137">このメソッドをリモート トランスポート プロバイダーの実装は、ここで説明するセマンティクスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5a48-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="d5a48-138">特別な考慮事項はありません。</span><span class="sxs-lookup"><span data-stu-id="d5a48-138">There are no special considerations.</span></span> <span data-ttu-id="d5a48-139">クライアントは、特定のメッセージがダウンロードするか、リモート メッセージ ストアから削除するのにことを示す MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE のビットを設定するのには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5a48-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="d5a48-140">リモート トランスポート プロバイダーは、関連する[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)メソッドを実装するためにはありません。</span><span class="sxs-lookup"><span data-stu-id="d5a48-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="d5a48-141">クライアントは、メッセージのステータスを確認するのにはフォルダーの内容のテーブルで検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5a48-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5a48-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d5a48-142">Notes to callers</span></span>

<span data-ttu-id="d5a48-143">メッセージの**PR_MSG_STATUS**プロパティを使用するには他のクライアントとメッセージのロックアウト操作をネゴシエートします。</span><span class="sxs-lookup"><span data-stu-id="d5a48-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="d5a48-144">ロックアウト ビットとビットを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5a48-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="d5a48-145">ロックアウト ビットが設定されているかどうかを確認するのには、 _lpulOldStatus_パラメーターでメッセージの状態の以前の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="d5a48-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="d5a48-146">_UlNewStatus_パラメーターで他のビットを使用して、ロックアウト ビットに干渉することがなくメッセージのステータスを追跡します。</span><span class="sxs-lookup"><span data-stu-id="d5a48-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5a48-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5a48-147">See also</span></span>



[<span data-ttu-id="d5a48-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="d5a48-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="d5a48-149">PidTagMessageStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="d5a48-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="d5a48-150">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d5a48-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
