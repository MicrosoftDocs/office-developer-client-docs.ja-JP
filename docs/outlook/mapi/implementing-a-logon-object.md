---
title: ログオン オブジェクトを実装します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800911"
---
# <a name="implementing-a-logon-object"></a><span data-ttu-id="0d622-103">ログオン オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="0d622-103">Implementing a Logon Object</span></span>

  
  
<span data-ttu-id="0d622-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d622-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d622-105">すべてのアドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、 [IABProvider::Logon](iabprovider-logon.md)、 [IMSProvider::Logon](imsprovider-logon.md)、または[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の実装の一部としてのログオン オブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="0d622-105">Every address book, message store, and transport provider instantiates a logon object as part of its implementation of [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md).</span></span> <span data-ttu-id="0d622-106">ログオン オブジェクトでは、MAPI クライアントの要求のためのメソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="0d622-106">Logon objects implement methods that help MAPI service client requests.</span></span> <span data-ttu-id="0d622-107">サービス プロバイダーの種類によっては、ログオン オブジェクトは次のインターフェイスのいずれかでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0d622-107">Depending on your type of service provider, your logon object will support one of the following interfaces.</span></span> 
  
|<span data-ttu-id="0d622-108">**ログオン オブジェクトのインタ フェース**</span><span class="sxs-lookup"><span data-stu-id="0d622-108">**Logon object interface**</span></span>|<span data-ttu-id="0d622-109">**サービス プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="0d622-109">**Service provider**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d622-110">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d622-110">IABLogon : IUnknown</span></span>](iablogoniunknown.md) <br/> |<span data-ttu-id="0d622-111">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0d622-111">Address book provider</span></span>  <br/> |
|[<span data-ttu-id="0d622-112">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d622-112">IMSLogon : IUnknown</span></span>](imslogoniunknown.md) <br/> |<span data-ttu-id="0d622-113">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0d622-113">Message store provider</span></span>  <br/> |
|[<span data-ttu-id="0d622-114">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d622-114">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md) <br/> |<span data-ttu-id="0d622-115">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0d622-115">Transport provider</span></span>  <br/> |
   
<span data-ttu-id="0d622-116">アドレス帳とメッセージ ・ ストア プロバイダーの実装次の機能で、ログオン オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0d622-116">Address book and message store providers implement the following features in their logon objects:</span></span>
  
- <span data-ttu-id="0d622-117">イベント通知 (**アドバイズ**と**Unadvise**メソッド) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0d622-117">Support for event notification (**Advise** and **Unadvise** methods).</span></span> <span data-ttu-id="0d622-118">イベント通知の詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-118">For an overview of event notification, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="0d622-119">ログオン オブジェクトの通知をサポートの詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-119">For more information about supporting notification in your logon object, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
    
- <span data-ttu-id="0d622-120">(**CompareEntryIDs**メソッド) エントリ識別子を比較します。</span><span class="sxs-lookup"><span data-stu-id="0d622-120">Entry identifier comparison (**CompareEntryIDs** method).</span></span> <span data-ttu-id="0d622-121">エントリ id の詳細については、 [MAPI エントリの識別子](mapi-entry-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-121">For general information about entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span> <span data-ttu-id="0d622-122">**CompareEntryIDs**メソッドをログオン オブジェクトのエントリ id を比較することに関する詳細については、[オブジェクトへのアクセスをサポートしているとの比較](supporting-object-access-and-comparison.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-122">For more information about comparing entry identifiers in your logon object's **CompareEntryIDs** method, see [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).</span></span>
    
- <span data-ttu-id="0d622-123">追加のエラー情報 (**GetLastError**メソッド) にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0d622-123">Access to additional error information (**GetLastError** method).</span></span> <span data-ttu-id="0d622-124">MAPI でのエラー処理の詳細については、 [MAPI でエラーが処理](error-handling-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-124">For more information about handling errors in MAPI, see [Error Handling in MAPI](error-handling-in-mapi.md).</span></span> 
    
- <span data-ttu-id="0d622-125">サービス プロバイダー (**OpenEntry**メソッド) が実装されているオブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0d622-125">Access to objects implemented by the service provider (**OpenEntry** method).</span></span> <span data-ttu-id="0d622-126">詳細については、[オブジェクトへのアクセスをサポートしているとの比較](supporting-object-access-and-comparison.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-126">For more information, see [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).</span></span>
    
- <span data-ttu-id="0d622-127">状態オブジェクト (**OpenStatusEntry**メソッド) にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0d622-127">Access to a status object (**OpenStatusEntry** method).</span></span> <span data-ttu-id="0d622-128">ステータス オブジェクトの詳細については、 [MAPI オブジェクトのステータス](mapi-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-128">For general information about status objects, see [MAPI Status Objects](mapi-status-objects.md).</span></span> <span data-ttu-id="0d622-129">状態オブジェクトを実装する詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-129">For specific information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span>
    
- <span data-ttu-id="0d622-130">ログオフ プロセス (**ログオフ**の方法)。</span><span class="sxs-lookup"><span data-stu-id="0d622-130">A logoff process (**Logoff** method).</span></span> <span data-ttu-id="0d622-131">詳細については、[シャット ダウン、サービス ・ プロバイダー](shutting-down-a-service-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-131">For more information, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
    
<span data-ttu-id="0d622-132">プロバイダーが、アドレス帳プロバイダーの場合は、以下の方法と関連する機能も実装します。</span><span class="sxs-lookup"><span data-stu-id="0d622-132">If your provider is an address book provider, you will also implement the following methods and associated features:</span></span>
  
- <span data-ttu-id="0d622-133">[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)の新しい受信者を作成するためにサポートしているテンプレートの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d622-133">[IABLogon::GetOneOffTable](iablogon-getoneofftable.md) to provide a listing of the templates that you support for creating new recipients.</span></span> <span data-ttu-id="0d622-134">詳細については、[一時テーブル](one-off-tables.md)または[一時テーブル プロバイダーを実装する](implementing-a-provider-one-off-table.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-134">For more information, see [One-Off Tables](one-off-tables.md) or [Implementing a Provider One-Off Table](implementing-a-provider-one-off-table.md).</span></span>
    
- <span data-ttu-id="0d622-135">データが含まれる受信者の実装へのアクセスを提供する[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)は、ホストのアドレス帳に存在します。</span><span class="sxs-lookup"><span data-stu-id="0d622-135">[IABLogon::OpenTemplateID](iablogon-opentemplateid.md) to provide access to the implementation of a recipient whose data resides in a host address book provider.</span></span> <span data-ttu-id="0d622-136">詳細については、[外部のアドレス帳プロバイダーとしての機能](acting-as-a-foreign-address-book-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-136">For more information, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span> 
    
- <span data-ttu-id="0d622-137">[IABLogon::PrepareRecips](iablogon-preparerecips.md)の適切なプロパティが受信者のリスト内の受信者のすべての利用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d622-137">[IABLogon::PrepareRecips](iablogon-preparerecips.md) to ensure that the appropriate properties are available for all of the recipients in a recipient list.</span></span> <span data-ttu-id="0d622-138">詳細については、 [IABLogon::PrepareRecips](iablogon-preparerecips.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-138">For more information, see [IABLogon::PrepareRecips](iablogon-preparerecips.md).</span></span> 
    
<span data-ttu-id="0d622-139">トランスポート プロバイダーのログオン オブジェクトを実装して、 [IXPLogon: IUnknown](ixplogoniunknown.md)、サービス ・ プロバイダーの他の型によって実装されているログオン オブジェクトとはまったく異なります。</span><span class="sxs-lookup"><span data-stu-id="0d622-139">A transport provider's logon object, which implements [IXPLogon : IUnknown](ixplogoniunknown.md), is quite different from the logon objects implemented by the other types of service providers.</span></span> <span data-ttu-id="0d622-140">他のログオン オブジェクトと共通の 2 つのみの機能がある: [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md)メソッドを通じて状態オブジェクト、および[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)メソッドからのログオフ操作へのアクセス。</span><span class="sxs-lookup"><span data-stu-id="0d622-140">It has only two features in common with the other logon objects: access to a status object through the [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) method and a logoff operation through the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> <span data-ttu-id="0d622-141">トランスポート プロバイダーは、そのログオン オブジェクトで次の独自の機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="0d622-141">Transport providers implement the following unique features in their logon objects:</span></span> 
  
- <span data-ttu-id="0d622-142">([IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッド) のアドレスの種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="0d622-142">Registration for address types ([IXPLogon::AddressTypes](ixplogon-addresstypes.md) method).</span></span> <span data-ttu-id="0d622-143">アドレスの種類を登録の詳細については、[トランスポート プロバイダーおよび MAPI スプーラーの運用モデル](transport-provider-and-mapi-spooler-operational-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-143">For more information about registering an address type, see [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).</span></span>
    
- <span data-ttu-id="0d622-144">メッセージの転送 ([IXPLogon::StartMessage](ixplogon-startmessage.md)、 [IXPLogon::EndMessage](ixplogon-endmessage.md)、および[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッド) をコントロールできます。</span><span class="sxs-lookup"><span data-stu-id="0d622-144">Control of message transmission ([IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md), and [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods).</span></span> <span data-ttu-id="0d622-145">詳細については、[メッセージ受信モデル](message-reception-model.md)、 [MAPI スプーラーと対話する](interacting-with-the-mapi-spooler.md)、および[メッセージの送信モデル](message-submission-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-145">For more information, see [Message Reception Model](message-reception-model.md), [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md), and [Message Submission Model](message-submission-model.md).</span></span>
    
- <span data-ttu-id="0d622-146">内部状態の検証 ([IXPLogon::ValidateState](ixplogon-validatestate.md)メソッド)。</span><span class="sxs-lookup"><span data-stu-id="0d622-146">Internal state validation ([IXPLogon::ValidateState](ixplogon-validatestate.md) method).</span></span> 
    
- <span data-ttu-id="0d622-147">([IXPLogon::FlushQueues](ixplogon-flushqueues.md)メソッド) を必要に応じてメッセージをアップロードまたはダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="0d622-147">Ability to download or upload messages on demand ([IXPLogon::FlushQueues](ixplogon-flushqueues.md) method).</span></span> <span data-ttu-id="0d622-148">詳細については、 [FlushQueues メソッドを実装する](implementing-the-flushqueues-method.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-148">For more information, see [Implementing the FlushQueues Method](implementing-the-flushqueues-method.md).</span></span>
    
- <span data-ttu-id="0d622-149">保留中のメッセージ ([IXPLogon::Poll](ixplogon-poll.md)メソッド) を照会する機能です。</span><span class="sxs-lookup"><span data-stu-id="0d622-149">Ability to query for pending messages ([IXPLogon::Poll](ixplogon-poll.md) method).</span></span> <span data-ttu-id="0d622-150">詳細については、[メッセージ受信のモデル](message-reception-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d622-150">For more information, see [Message Reception Model](message-reception-model.md).</span></span>
    
- <span data-ttu-id="0d622-151">アイドル状態の検出 ([IXPLogon::Idle](ixplogon-idle.md)メソッド)。</span><span class="sxs-lookup"><span data-stu-id="0d622-151">Idle state detection ([IXPLogon::Idle](ixplogon-idle.md) method).</span></span> 
    
- <span data-ttu-id="0d622-152">MAPI スプーラーを無効 ([IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッド) との相互作用します。</span><span class="sxs-lookup"><span data-stu-id="0d622-152">Interaction with the MAPI spooler ([IXPLogon::TransportNotify](ixplogon-transportnotify.md) method).</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0d622-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d622-153">See also</span></span>



[<span data-ttu-id="0d622-154">サービス プロバイダーへのログオンを実装します。</span><span class="sxs-lookup"><span data-stu-id="0d622-154">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)
