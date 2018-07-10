---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801274"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="2ae93-103">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ae93-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="2ae93-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ae93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ae93-105">トランスポート プロバイダーを MAPI スプーラーのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ae93-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2ae93-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ae93-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="2ae93-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="2ae93-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="2ae93-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2ae93-109">トランスポート ログオン オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2ae93-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="2ae93-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2ae93-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ae93-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2ae93-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="2ae93-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2ae93-112">Called by:</span></span>  <br/> |<span data-ttu-id="2ae93-113">MAPI スプーラーを無効</span><span class="sxs-lookup"><span data-stu-id="2ae93-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="2ae93-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="2ae93-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2ae93-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="2ae93-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="2ae93-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="2ae93-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2ae93-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="2ae93-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2ae93-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="2ae93-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2ae93-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="2ae93-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="2ae93-120">トランスポート プロバイダーを処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="2ae93-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="2ae93-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="2ae93-122">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="2ae93-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="2ae93-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="2ae93-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="2ae93-124">トランスポート プロバイダーが通知を要求するイベントの発生を通知します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-125">アイドル</span><span class="sxs-lookup"><span data-stu-id="2ae93-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="2ae93-126">システムがアイドル状態、優先度の低い操作を実行するトランスポート プロバイダーを有効にすることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="2ae93-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="2ae93-128">ログオフ処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="2ae93-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="2ae93-130">MAPI スプーラーがメッセージを配信するトランスポート プロバイダーを持っていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="2ae93-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="2ae93-132">トランスポート プロバイダーは、MAPI スプーラーに送信メッセージの処理が完了したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-133">ポール</span><span class="sxs-lookup"><span data-stu-id="2ae93-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="2ae93-134">トランスポート プロバイダーが 1 つまたは複数の受信メッセージを受信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="2ae93-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="2ae93-136">MAPI スプーラーをトランスポート プロバイダーからの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="2ae93-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="2ae93-138">トランスポート プロバイダーの状態のオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2ae93-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="2ae93-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="2ae93-140">トランスポート プロバイダーの外部の状況をチェックします。</span><span class="sxs-lookup"><span data-stu-id="2ae93-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="2ae93-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="2ae93-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="2ae93-142">要求がトランスポート プロバイダーは、すべての保留の受信または送信メッセージを即座に配信します。</span><span class="sxs-lookup"><span data-stu-id="2ae93-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ae93-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ae93-143">See also</span></span>



[<span data-ttu-id="2ae93-144">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2ae93-144">MAPI Interfaces</span></span>](mapi-interfaces.md)
