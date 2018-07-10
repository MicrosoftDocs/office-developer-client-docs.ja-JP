---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800825"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="bebeb-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="bebeb-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="bebeb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bebeb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bebeb-105">MAPI 経由の通知を受信するアドバイズ シンクを登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bebeb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bebeb-106">Parameters</span></span>

 <span data-ttu-id="bebeb-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="bebeb-107">_lpKey_</span></span>
  
> <span data-ttu-id="bebeb-108">[in]アドバイズのソース オブジェクトを表す通知キーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bebeb-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="bebeb-109">_LpKey_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bebeb-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="bebeb-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="bebeb-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="bebeb-111">[in]呼び出し元に興味を持って登録に含めることが通知イベントの種類を示す値のマスク。</span><span class="sxs-lookup"><span data-stu-id="bebeb-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="bebeb-112">次の値は、有効です。</span><span class="sxs-lookup"><span data-stu-id="bebeb-112">The following values are valid:</span></span>
    
 <span data-ttu-id="bebeb-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="bebeb-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="bebeb-114">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="bebeb-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="bebeb-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="bebeb-116">プロバイダーを格納する特定のアドレス帳またはメッセージに特定のイベントに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="bebeb-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="bebeb-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="bebeb-118">新しいメッセージの到着の通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="bebeb-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="bebeb-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="bebeb-120">新しいオブジェクトの作成についての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="bebeb-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="bebeb-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="bebeb-122">コピーされているオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="bebeb-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="bebeb-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="bebeb-124">削除されているオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="bebeb-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="bebeb-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="bebeb-126">変更されているオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="bebeb-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="bebeb-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="bebeb-128">移動されるオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="bebeb-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="bebeb-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="bebeb-130">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="bebeb-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bebeb-131">_ulFlags_</span></span>
  
> <span data-ttu-id="bebeb-132">[in]通知がどのように行われるかを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="bebeb-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="bebeb-133">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="bebeb-133">The following flag can be set:</span></span>
    
<span data-ttu-id="bebeb-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="bebeb-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="bebeb-135">**通知**がアドバイズ シンクに必要なすべての呼び出しをする必要がありますこのアドバイズ シンクに通知を生成する[IMAPISupport::Notify](imapisupport-notify.md)メソッドを呼び出すと、呼び出し元に返す前にします。</span><span class="sxs-lookup"><span data-stu-id="bebeb-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="bebeb-136">このフラグが設定されていない場合の通知は非同期な購読があり、それらのプロセスが CPU の制御を取得するときに起動しているプロセスのコールバックがキューに入れられました。</span><span class="sxs-lookup"><span data-stu-id="bebeb-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="bebeb-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="bebeb-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="bebeb-138">[in]アドバイズ シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bebeb-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="bebeb-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="bebeb-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="bebeb-140">[out]登録を表す、0 以外の接続数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bebeb-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bebeb-141">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bebeb-141">Return value</span></span>

<span data-ttu-id="bebeb-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="bebeb-142">S_OK</span></span> 
  
> <span data-ttu-id="bebeb-143">通知の登録に成功しました。</span><span class="sxs-lookup"><span data-stu-id="bebeb-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bebeb-144">備考</span><span class="sxs-lookup"><span data-stu-id="bebeb-144">Remarks</span></span>

<span data-ttu-id="bebeb-145">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::Subscribe**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="bebeb-146">サービス プロバイダーでは、 **Subscribe**を呼び出してから通知を管理するために MAPI を使用して**アドバイズ**メソッドのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="bebeb-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bebeb-147">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bebeb-147">Notes to callers</span></span>

<span data-ttu-id="bebeb-148">MAPI サポート メソッドを使用して、通知のため、オブジェクトの通知を生成する必要がありますアドバイスのソースのためのキーを作成します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="bebeb-149">キーの値は一意である必要があり、簡単に再生成される、オブジェクトが変更されるたびにします。</span><span class="sxs-lookup"><span data-stu-id="bebeb-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="bebeb-150">MAPI では、通知キーを使用して、対応するアドバイスのソースの[HrAllocAdviseSink](hrallocadvisesink.md)関数により登録されている任意のコールバック関数を検索します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="bebeb-151">アドバイズ対応するソースの通知を生成する必要がありますたびに、このキーを**IMAPISupport::Notify**に渡します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="bebeb-152">NOTIFY_SYNC フラグでは、後続の呼び出しへの**通知**の動作に影響します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="bebeb-153">NOTIFY_SYNC を設定すると、すべての必要な通知の送信が完了するまで**通知**が返されません。</span><span class="sxs-lookup"><span data-stu-id="bebeb-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="bebeb-154">NOTIFY_SYNC を設定しないと、**通知**はすべての通知を送信する前に返す可能性がある、非同期に動作します。</span><span class="sxs-lookup"><span data-stu-id="bebeb-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bebeb-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="bebeb-155">See also</span></span>



[<span data-ttu-id="bebeb-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="bebeb-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="bebeb-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bebeb-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bebeb-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="bebeb-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="bebeb-159">�ʒm</span><span class="sxs-lookup"><span data-stu-id="bebeb-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="bebeb-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="bebeb-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="bebeb-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bebeb-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
