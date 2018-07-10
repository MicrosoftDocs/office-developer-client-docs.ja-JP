---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 87be00bce55fabda6271b472a9e5c446aaf8054a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801033"
---
# <a name="imslogonadvise"></a><span data-ttu-id="dcd61-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="dcd61-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="dcd61-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcd61-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcd61-105">メッセージ ・ ストア内の変更についての通知のメッセージ ストア プロバイダー オブジェクトに登録します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="dcd61-106">メッセージ ・ ストアに登録済みのオブジェクトの変更に関する通知が送付されます。</span><span class="sxs-lookup"><span data-stu-id="dcd61-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="dcd61-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="dcd61-107">Parameters</span></span>

 <span data-ttu-id="dcd61-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dcd61-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="dcd61-109">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="dcd61-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dcd61-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dcd61-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="dcd61-111">[in]通知を生成する対象のオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dcd61-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="dcd61-112">このオブジェクトには、フォルダー、メッセージ、またはメッセージ ・ ストア内の他の任意のオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="dcd61-113">また、MAPI、 _cbEntryID_パラメーターを 0 に設定し、 **null**の場合、 _lpEntryID_、アドバイズ シンクは全体のメッセージ ・ ストアへの変更についての通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="dcd61-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="dcd61-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="dcd61-115">[in]MAPI が通知を生成するオブジェクトに対して発生する通知イベントの種類のイベント マスクです。</span><span class="sxs-lookup"><span data-stu-id="dcd61-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="dcd61-116">マスクは、特定のケースをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-116">The mask filters specific cases.</span></span> <span data-ttu-id="dcd61-117">各イベントの種類には、イベントに関する追加情報が含まれていることに関連付けられている構造体があります。</span><span class="sxs-lookup"><span data-stu-id="dcd61-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="dcd61-118">次の表に、可能性のあるイベントの種類と、それらに対応する構造体を示します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="dcd61-119">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="dcd61-119">**Notification event type**</span></span>|<span data-ttu-id="dcd61-120">**対応する構造体**</span><span class="sxs-lookup"><span data-stu-id="dcd61-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dcd61-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="dcd61-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="dcd61-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="dcd61-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="dcd61-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="dcd61-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="dcd61-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="dcd61-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="dcd61-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="dcd61-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="dcd61-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="dcd61-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="dcd61-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="dcd61-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="dcd61-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="dcd61-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="dcd61-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="dcd61-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="dcd61-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="dcd61-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="dcd61-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="dcd61-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="dcd61-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="dcd61-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="dcd61-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="dcd61-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="dcd61-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="dcd61-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="dcd61-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="dcd61-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="dcd61-140">[in]アドバイズ シンクについては、通知が要求されたセッション オブジェクトのイベントが発生したときに呼び出されるオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dcd61-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="dcd61-141">このアドバイズ シンク オブジェクトが既に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcd61-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="dcd61-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="dcd61-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="dcd61-143">[out]成功時に、通知の登録のための接続数を格納する変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dcd61-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="dcd61-144">接続数は、0 以外の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcd61-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dcd61-145">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dcd61-145">Return value</span></span>

<span data-ttu-id="dcd61-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="dcd61-146">S_OK</span></span> 
  
> <span data-ttu-id="dcd61-147">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="dcd61-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dcd61-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dcd61-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dcd61-149">MAPI または 1 つまたは複数のサービス プロバイダーによっては、操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="dcd61-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dcd61-150">備考</span><span class="sxs-lookup"><span data-stu-id="dcd61-150">Remarks</span></span>

<span data-ttu-id="dcd61-151">メッセージ ストア プロバイダーは、通知のコールバック オブジェクトを登録するのには**IMSLogon::Advise**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="dcd61-152">指定したオブジェクトに変更が発生するたびに、プロバイダーはどのようなイベント マスク ビットが設定されて、 _ulEventMask_パラメーターであり、したがってどのような種類の変更が発生したを確認します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="dcd61-153">ビットが設定されている場合、プロバイダーはイベントを通知する_lpAdviseSink_パラメーターで指定されたアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="dcd61-154">**OnNotify**ルーチンに渡された通知の構造体のデータでは、イベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="dcd61-155">**OnNotify**への呼び出しは、オブジェクトを変更するための呼び出し時に、後でいつでもでも発生します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="dcd61-156">複数の実行スレッドをサポートしているシステムでは、任意のスレッドで**OnNotify**への呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="dcd61-157">**OnNotify**使用時に発生する可能性があります呼び出しを安全に処理するには、クライアント アプリケーションは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="dcd61-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="dcd61-158">_LpAdviseSink_へのポインターのコピーを保持する**アドバイス**のニーズを実装しているメッセージ ストア プロバイダーのシンク オブジェクトの案内通知を行うには、これを行うには、プロバイダーは、 [IMSLogon::Unadvise](imslogon-unadvise.md)メソッドを呼び出して、通知の登録をキャンセルするまで、オブジェクトを指すポインターを維持するためにアドバイズ シンクの[IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="dcd61-159">**アドバイズ**実装する必要があります通知の登録に接続番号を割り当てるし、 _lpulConnection_パラメーターに返す前に、この接続の数で**AddRef**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="dcd61-160">**Unadvise**が呼び出されるまでに接続の数を解放する必要があります、登録がキャンセルされると、前に、サービス プロバイダーは、アドバイズ シンク オブジェクトをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="dcd61-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="dcd61-161">**Advise**への呼び出しが成功した後、 **Unadvise**と呼ばれる前に、アドバイズ シンク オブジェクトを解放するためプロバイダーを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcd61-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="dcd61-162">そのため、プロバイダーする必要がありますリリースのアドバイズ シンク オブジェクト**アドバイズ**が返されると、それの特定の長期的な使用がある場合を除き、します。</span><span class="sxs-lookup"><span data-stu-id="dcd61-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="dcd61-163">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dcd61-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dcd61-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="dcd61-164">See also</span></span>



[<span data-ttu-id="dcd61-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dcd61-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="dcd61-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="dcd61-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="dcd61-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="dcd61-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="dcd61-168">�ʒm</span><span class="sxs-lookup"><span data-stu-id="dcd61-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="dcd61-169">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcd61-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)
