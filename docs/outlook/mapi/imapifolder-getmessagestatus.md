---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800490"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="ad2e6-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ad2e6-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="ad2e6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad2e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad2e6-105">(たとえば、あるかどうかそのメッセージは削除対象としてマーク) は、特定のフォルダー内のメッセージに関連付けられたステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="ad2e6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ad2e6-106">Parameters</span></span>

 <span data-ttu-id="ad2e6-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad2e6-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ad2e6-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ad2e6-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad2e6-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ad2e6-110">[in]状態が取得したメッセージのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="ad2e6-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad2e6-111">_ulFlags_</span></span>
  
> <span data-ttu-id="ad2e6-112">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="ad2e6-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ad2e6-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="ad2e6-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="ad2e6-114">[out]メッセージのステータスを示すフラグのビットマスクへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="ad2e6-115">ビット 0 ~ 15 は予約されており、0 にする必要があります。31 までの 16 ビットは、実装固有の用途に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="ad2e6-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-116">The following flags can be set:</span></span>
    
<span data-ttu-id="ad2e6-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="ad2e6-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="ad2e6-118">メッセージは、削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="ad2e6-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="ad2e6-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="ad2e6-120">メッセージは表示しません。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="ad2e6-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="ad2e6-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="ad2e6-122">メッセージが表示されるが強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="ad2e6-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="ad2e6-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="ad2e6-124">メッセージは、ローカル クライアントにダウンロードすることがなくリモート メッセージ ストアを削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="ad2e6-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ad2e6-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ad2e6-126">メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロード用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="ad2e6-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="ad2e6-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="ad2e6-128">クライアント定義の目的は、メッセージをタグ付けされました。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad2e6-129">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ad2e6-129">Return value</span></span>

<span data-ttu-id="ad2e6-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad2e6-130">S_OK</span></span> 
  
> <span data-ttu-id="ad2e6-131">メッセージの状態が正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad2e6-132">備考</span><span class="sxs-lookup"><span data-stu-id="ad2e6-132">Remarks</span></span>

<span data-ttu-id="ad2e6-133">**IMAPIFolder::GetMessageStatus**メソッドは、メッセージのステータスを返します。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="ad2e6-134">メッセージの状態は、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ad2e6-135">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ad2e6-135">Notes to implementers</span></span>

<span data-ttu-id="ad2e6-136">メッセージのステータス ビットを設定、オフになっていると使用する方法によって異なります完全に、実装がビット 0 ~ 15 は予約されており、0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="ad2e6-137">IPM サブツリー内のメッセージを格納する場合、MAPI は IPM クライアントによってビット 16 ~ 31 の使用を予約します。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="ad2e6-138">他のサブツリー内のメッセージを格納する場合は、目的に合わせて 31 までからの 16 ビットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad2e6-139">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ad2e6-139">MFCMAPI reference</span></span>

<span data-ttu-id="ad2e6-140">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ad2e6-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad2e6-141">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ad2e6-141">**File**</span></span>|<span data-ttu-id="ad2e6-142">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ad2e6-142">**Function**</span></span>|<span data-ttu-id="ad2e6-143">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ad2e6-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad2e6-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ad2e6-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ad2e6-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="ad2e6-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="ad2e6-146">MFCMAPI では、 **IMAPIFolder::GetMessageStatus**メソッドを使用して、表示される次のメッセージのステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="ad2e6-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ad2e6-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ad2e6-148">OpenMessageNonModal と OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="ad2e6-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="ad2e6-149">MFCMAPI では、 **IMAPIFolder::GetMessageStatus**メソッドを使用して、フォームのビューアーでは、CMyMAPIFormViewer または[IMAPISession::ShowForm](imapisession-showform.md)に渡すことを表示するメッセージのステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ad2e6-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad2e6-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad2e6-150">See also</span></span>



[<span data-ttu-id="ad2e6-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ad2e6-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="ad2e6-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="ad2e6-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="ad2e6-153">PidTagMessageStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ad2e6-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="ad2e6-154">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ad2e6-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="ad2e6-155">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ad2e6-155">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
