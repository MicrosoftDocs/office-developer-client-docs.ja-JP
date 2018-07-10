---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801255"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="cc620-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="cc620-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="cc620-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc620-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc620-105">トランスポート プロバイダーが 1 つまたは複数の受信メッセージを受信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="cc620-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="cc620-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cc620-106">Parameters</span></span>

 <span data-ttu-id="cc620-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="cc620-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="cc620-108">[out]受信メッセージの存在を示す値。</span><span class="sxs-lookup"><span data-stu-id="cc620-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="cc620-109">0 以外の値は、受信メッセージがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="cc620-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc620-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cc620-110">Return value</span></span>

<span data-ttu-id="cc620-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc620-111">S_OK</span></span> 
  
> <span data-ttu-id="cc620-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cc620-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc620-113">����</span><span class="sxs-lookup"><span data-stu-id="cc620-113">Remarks</span></span>

<span data-ttu-id="cc620-114">MAPI スプーラーは、トランスポート プロバイダーは、新しいメッセージは、プロバイダーの LOGON_SP_POLL を渡すことによってフラグが[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の呼び出しにポーリングする必要がありますを示す場合は、定期的に**IXPLogon::Poll**メソッドを呼び出しますセッションの開始時の方法です。</span><span class="sxs-lookup"><span data-stu-id="cc620-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="cc620-115">トランスポート プロバイダーは、1 つを使用する必要がある**ポーリング**呼び出しへの応答としてまたはより受信メッセージの処理では、MAPI スプーラーを入手することは、プロバイダーの最初のプロセスからを許可する[IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドを呼び出す場合は、受信します。メッセージ。</span><span class="sxs-lookup"><span data-stu-id="cc620-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="cc620-116">トランスポート プロバイダーは、0 以外の値を_lpulIncoming_パラメーターに値を設定することにより受信メッセージを示します。</span><span class="sxs-lookup"><span data-stu-id="cc620-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc620-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc620-117">See also</span></span>



[<span data-ttu-id="cc620-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="cc620-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="cc620-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="cc620-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="cc620-120">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc620-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)
