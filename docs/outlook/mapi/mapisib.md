---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801524"
---
# <a name="mapisib"></a><span data-ttu-id="281ff-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="281ff-103">MAPISIB</span></span>

  
  
<span data-ttu-id="281ff-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="281ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="281ff-105">この構造体は、 [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md)で使用されます。</span><span class="sxs-lookup"><span data-stu-id="281ff-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="281ff-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="281ff-106">Members</span></span>

 <span data-ttu-id="281ff-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="281ff-107">**ulSize**</span></span>
  
> <span data-ttu-id="281ff-108">構造体のサイズです。</span><span class="sxs-lookup"><span data-stu-id="281ff-108">The size of the structure.</span></span>
    
 <span data-ttu-id="281ff-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="281ff-109">**ulFlags**</span></span>
  
> <span data-ttu-id="281ff-110">同期の種類を示すフラグ。次の値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="281ff-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="281ff-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="281ff-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="281ff-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="281ff-112">0x00000200</span></span>  <br/> |<span data-ttu-id="281ff-113">(使用) では現在のサーバーにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="281ff-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="281ff-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="281ff-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="281ff-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="281ff-115">0x00000001</span></span>  <br/> |<span data-ttu-id="281ff-116">階層の変更内容をサーバーにプッシュします。</span><span class="sxs-lookup"><span data-stu-id="281ff-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="281ff-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="281ff-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="281ff-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="281ff-118">0x00000002</span></span>  <br/> |<span data-ttu-id="281ff-119">階層の変更内容をサーバーから取得します。</span><span class="sxs-lookup"><span data-stu-id="281ff-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="281ff-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="281ff-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="281ff-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="281ff-121">0x00000040</span></span>  <br/> |<span data-ttu-id="281ff-122">メッセージの変更をサーバーにプッシュします。</span><span class="sxs-lookup"><span data-stu-id="281ff-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="281ff-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="281ff-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="281ff-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="281ff-124">0x00000080</span></span>  <br/> |<span data-ttu-id="281ff-125">メッセージの変更をサーバーから取得します。</span><span class="sxs-lookup"><span data-stu-id="281ff-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="281ff-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="281ff-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="281ff-127">0x20000000 を設定</span><span class="sxs-lookup"><span data-stu-id="281ff-127">0x20000000</span></span>  <br/> |<span data-ttu-id="281ff-128">同期では、ユーザーによって開始され、優先順位が高い必要があります。</span><span class="sxs-lookup"><span data-stu-id="281ff-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="281ff-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="281ff-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="281ff-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="281ff-130">0x02000000</span></span>  <br/> |<span data-ttu-id="281ff-131">ヘッダーと本文のない完全同期させるだけ必要があります。</span><span class="sxs-lookup"><span data-stu-id="281ff-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="281ff-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="281ff-132">**psesSync**</span></span>
  
> <span data-ttu-id="281ff-133">[IN]MAPI セッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="281ff-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="281ff-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="281ff-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="281ff-135">[IN]進行状況を提供するインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="281ff-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="281ff-136">インターフェイスを照会するために使用できる[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="281ff-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="281ff-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="281ff-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="281ff-138">[OUT]作成されたスレッドが完了したときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="281ff-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="281ff-139">イベントが含まれているために、ポインターは有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="281ff-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="281ff-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="281ff-140">See also</span></span>



[<span data-ttu-id="281ff-141">IMAPISyncProgressCallback: IUnknown</span><span class="sxs-lookup"><span data-stu-id="281ff-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="281ff-142">IMAPISync: IUnknown</span><span class="sxs-lookup"><span data-stu-id="281ff-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
