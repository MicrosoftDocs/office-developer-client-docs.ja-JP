---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800464"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="c427f-103">IMAPIClientShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c427f-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="c427f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c427f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c427f-105">クライアント プロセスの高速シャット ダウンを実行するために MAPI クライアントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c427f-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c427f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c427f-106">Header file:</span></span>  <br/> |<span data-ttu-id="c427f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c427f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c427f-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="c427f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c427f-109">[IMAPISession](imapisessioniunknown.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c427f-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="c427f-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c427f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c427f-111">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="c427f-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="c427f-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c427f-112">Called by:</span></span>  <br/> |<span data-ttu-id="c427f-113">MAPI クライアント</span><span class="sxs-lookup"><span data-stu-id="c427f-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="c427f-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="c427f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c427f-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="c427f-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="c427f-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="c427f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c427f-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="c427f-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c427f-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="c427f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c427f-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c427f-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="c427f-120">クエリ、MAPI サブシステムの高速シャット ダウンをサポートして読み込まれている MAPI プロバイダーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="c427f-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="c427f-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="c427f-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="c427f-122">続行するのには MAPI クライアントの意図をシャット ダウンを示します。</span><span class="sxs-lookup"><span data-stu-id="c427f-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="c427f-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c427f-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="c427f-124">MAPI クライアントのクライアントのプロセスを即座に終了するという意図を示しています。</span><span class="sxs-lookup"><span data-stu-id="c427f-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c427f-125">備考</span><span class="sxs-lookup"><span data-stu-id="c427f-125">Remarks</span></span>

<span data-ttu-id="c427f-126">高速シャット ダウンでは、MAPI クライアントと、読み込まれている MAPI プロバイダーにすると、MAPI クライアントは、MAPI の設定とデータを保存するのにはアクティブな MAPI セッションを許可します。</span><span class="sxs-lookup"><span data-stu-id="c427f-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="c427f-127">これにより、MAPI クライアントをすべての外部参照を切断して、データの損失を発生させることがなく終了します。</span><span class="sxs-lookup"><span data-stu-id="c427f-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="c427f-128">高速シャット ダウンを行うに必要な MAPI クライアントでは、 **IMAPIClientShutdown**インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c427f-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="c427f-129">MAPI クライアントは、 [IMAPISession](imapisessioniunknown.md)オブジェクトの IUnknown::QueryInterface メソッドを呼び出して、このインターフェイスへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c427f-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="c427f-130">MAPI クライアントは、常に**IMAPIClientShutdown::QueryFastShutdown**メソッドを呼び出すことによって、高速シャット ダウンを開始します。</span><span class="sxs-lookup"><span data-stu-id="c427f-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="c427f-131">MAPI サブシステムは、読み込まれている MAPI プロバイダーがクライアントの高速シャット ダウンをサポートするかどうかを確認することによって、MAPI クライアントのクエリに応答します。</span><span class="sxs-lookup"><span data-stu-id="c427f-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="c427f-132">管理者は、高速シャット ダウンを続行するのには MAPI クライアントに必要なプロバイダーのサポートのレベルを判断するための Windows レジストリ設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c427f-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="c427f-133">詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c427f-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="c427f-134">高速シャット ダウンを続行するには、クライアントは、MAPI サブシステムにシャット ダウンするという意図を示すために**IMAPIClientShutdown::NotifyProcessShutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c427f-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="c427f-135">クライアントは、クライアント プロセスがすぐに終了することを示すために**IMAPIClientShutdown::DoFastShutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c427f-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="c427f-136">高速シャット ダウンの詳細については、[高速シャット ダウンの概要](fast-shutdown-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c427f-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="c427f-137">高速シャット ダウンが正常に実行する方法の詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c427f-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c427f-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="c427f-138">See also</span></span>



[<span data-ttu-id="c427f-139">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c427f-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="c427f-140">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="c427f-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
