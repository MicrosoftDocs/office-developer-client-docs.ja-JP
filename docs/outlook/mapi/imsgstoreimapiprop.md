---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 426333e6e2624adcd7cb6bc6dc4982b3d1ef1999
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801028"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="7e3a1-103">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7e3a1-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="7e3a1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e3a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e3a1-105">メッセージ情報を格納して、メッセージおよびフォルダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e3a1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7e3a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e3a1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e3a1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7e3a1-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7e3a1-109">メッセージ ストアのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="7e3a1-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="7e3a1-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e3a1-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7e3a1-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="7e3a1-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-112">Called by:</span></span>  <br/> |<span data-ttu-id="7e3a1-113">クライアント アプリケーションでは、MAPI スプーラーを無効、および MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3a1-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="7e3a1-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7e3a1-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="7e3a1-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="7e3a1-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7e3a1-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="7e3a1-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="7e3a1-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="7e3a1-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="7e3a1-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="7e3a1-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7e3a1-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7e3a1-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7e3a1-121">アドバイス</span><span class="sxs-lookup"><span data-stu-id="7e3a1-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="7e3a1-122">メッセージ ・ ストアに影響を与える特定のイベントの通知を受け取ることを登録します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-123">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="7e3a1-124">**IMsgStore::Advise**メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="7e3a1-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="7e3a1-126">メッセージ ストアの同じエントリを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7e3a1-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="7e3a1-128">フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="7e3a1-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="7e3a1-130">特定のメッセージ クラスの着信メッセージの送信先として、フォルダーを確立します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="7e3a1-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="7e3a1-132">または、指定したメッセージ クラスの既定値として受信したメッセージの送信先には、メッセージ ストアのフォルダーが表示されるように設定されているフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="7e3a1-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="7e3a1-134">受信フォルダーのテーブル、テーブルのすべてのメッセージ ストアの受信フォルダーに関する情報へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="7e3a1-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="7e3a1-136">メッセージ ・ ストアの通常のログオフを有効にします。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="7e3a1-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="7e3a1-138">発信キューからメッセージを削除しようとしています。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="7e3a1-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="7e3a1-140">発信キュー テーブル、メッセージ ストアの送信キュー内のすべてのメッセージに関する情報が含まれているテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="7e3a1-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="7e3a1-142">ロックまたはメッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="7e3a1-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="7e3a1-144">メッセージ ストア プロバイダーは、送信されたメッセージの処理を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="7e3a1-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="7e3a1-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="7e3a1-146">新しいメッセージが到着したメッセージ ・ ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="7e3a1-147">**必要なプロパティ**</span><span class="sxs-lookup"><span data-stu-id="7e3a1-147">**Required properties**</span></span>|<span data-ttu-id="7e3a1-148">**アクセス レベル**</span><span class="sxs-lookup"><span data-stu-id="7e3a1-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e3a1-149">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-150">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="7e3a1-151">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-152">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="7e3a1-153">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-154">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="7e3a1-155">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-156">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="7e3a1-157">**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-158">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="7e3a1-159">**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-160">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="7e3a1-161">**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-162">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="7e3a1-163">**PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e3a1-164">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="7e3a1-165">次のプロパティは、メッセージ ストアの個人間メッセージ (IPM) のことです。</span><span class="sxs-lookup"><span data-stu-id="7e3a1-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="7e3a1-166">**PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7e3a1-167">**PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7e3a1-168">**PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7e3a1-169">**PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e3a1-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7e3a1-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="7e3a1-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="7e3a1-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="7e3a1-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e3a1-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e3a1-172">See also</span></span>



[<span data-ttu-id="7e3a1-173">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7e3a1-173">MAPI Properties</span></span>](mapi-properties.md)
