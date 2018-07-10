---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 468dfd634c4aaf18b019d06975ec9066c9d5f7a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801512"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="f610d-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="f610d-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="f610d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f610d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f610d-105">通知の MAPIOFFLINE_NOTIFY_TYPE では、接続状態の変更を実行しようとしていますが行われて、または完了した場合を識別します。</span><span class="sxs-lookup"><span data-stu-id="f610d-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f610d-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f610d-106">Quick info</span></span>

<span data-ttu-id="f610d-107">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f610d-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="f610d-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="f610d-108">See also</span></span>



[<span data-ttu-id="f610d-109">オフラインの状態の API について</span><span class="sxs-lookup"><span data-stu-id="f610d-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="f610d-110">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="f610d-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f610d-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="f610d-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)
