---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800900"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="5fd74-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5fd74-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="5fd74-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fd74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fd74-105">すべてのメッセージのプロパティを保存し、メッセージを送信する準備が完了としてマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="5fd74-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5fd74-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5fd74-106">Parameters</span></span>

 <span data-ttu-id="5fd74-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5fd74-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5fd74-108">[in]メッセージの送信方法を制御するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5fd74-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="5fd74-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5fd74-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5fd74-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="5fd74-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="5fd74-111">MAPI では、すぐにメッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fd74-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="5fd74-112">このフラグは現在使用中です。</span><span class="sxs-lookup"><span data-stu-id="5fd74-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5fd74-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5fd74-113">Return value</span></span>

<span data-ttu-id="5fd74-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fd74-114">S_OK</span></span> 
  
> <span data-ttu-id="5fd74-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5fd74-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5fd74-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="5fd74-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="5fd74-117">メッセージの受信者テーブルは空です。</span><span class="sxs-lookup"><span data-stu-id="5fd74-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5fd74-118">備考</span><span class="sxs-lookup"><span data-stu-id="5fd74-118">Remarks</span></span>

<span data-ttu-id="5fd74-119">**IMessage::SubmitMessage**メソッドは、メッセージを送信する準備が完了としてをマークします。</span><span class="sxs-lookup"><span data-stu-id="5fd74-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="5fd74-120">MAPI は、メッセージを送信するためマークされている順序で基になるメッセージング システムに渡します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="5fd74-121">この機能では、しばらくの間は、基になるメッセージング システムにそれを担当するためにメッセージのメッセージ ストアに常に可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5fd74-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="5fd74-122">先に領収書の順序は、基になるメッセージング システムのコントロールし、メッセージの送信に使用された順序と必ずしも一致しません。</span><span class="sxs-lookup"><span data-stu-id="5fd74-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5fd74-123">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5fd74-123">Notes to implementers</span></span>

<span data-ttu-id="5fd74-124">保存し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティをチェックし、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="5fd74-125">MSGFLAG_RESEND フラグが設定されている場合は、 [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="5fd74-126">**PrepareSubmit**は、再送信メッセージ内の受信者のすべての受信者の種類および**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5fd74-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5fd74-127">Notes to callers</span></span>

<span data-ttu-id="5fd74-128">**SubmitMessage**が返されると、メッセージとその関連付けられているサブオブジェクトのメッセージをフォルダー、添付ファイル、ストリーム、テーブル、およびように無効になっています。</span><span class="sxs-lookup"><span data-stu-id="5fd74-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="5fd74-129">MAPI では、各自**が**メソッドを呼び出すことを除いて、これらのポインターをその他の操作は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="5fd74-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="5fd74-130">MAPI では、メッセージと関連付けられているすべてのサブオブジェクトを解放する必要があります**SubmitMessage**が呼び出された後になるよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="5fd74-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="5fd74-131">ただし、 **SubmitMessage**には、存在しないか無効な情報を示すエラー値が返された場合メッセージが開いたままになり、ポインターが有効なまま維持します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="5fd74-132">送信操作を取り消す場合に、取得し、メッセージの送信前にメッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティへのポインターを格納します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="5fd74-133">メッセージが送信された後、メッセージのエントリ id が無効になるためには、 **SubmitMessage**を呼び出す前に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fd74-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="5fd74-134">送信をキャンセルするには、このエントリの識別子を_lpEntryId_パラメーターをポイントし、 [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)をコールします。</span><span class="sxs-lookup"><span data-stu-id="5fd74-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5fd74-135">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="5fd74-135">MFCMAPI reference</span></span>

<span data-ttu-id="5fd74-136">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="5fd74-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5fd74-137">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="5fd74-137">**File**</span></span>|<span data-ttu-id="5fd74-138">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="5fd74-138">**Function**</span></span>|<span data-ttu-id="5fd74-139">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="5fd74-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5fd74-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5fd74-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="5fd74-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="5fd74-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="5fd74-142">MFCMAPI では、 **IMessage::SubmitMessage**メソッドを使用して、選択したメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="5fd74-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fd74-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fd74-143">See also</span></span>



[<span data-ttu-id="5fd74-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="5fd74-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="5fd74-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5fd74-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="5fd74-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5fd74-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
