---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3cf8ad3966c44add3fd85b9f1adf677039bfce15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800619"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="8c39b-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8c39b-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="8c39b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c39b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c39b-105">オフライン オブジェクトの現在のオンラインまたはオフラインの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="8c39b-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="8c39b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8c39b-106">Parameters</span></span>

 <span data-ttu-id="8c39b-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="8c39b-107">_pulState_</span></span>
  
> <span data-ttu-id="8c39b-108">[out]オンラインまたはオフラインの現在の状態がオフラインのオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="8c39b-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="8c39b-109">これら 2 つの値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c39b-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="8c39b-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="8c39b-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="8c39b-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="8c39b-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="8c39b-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c39b-112">See also</span></span>



[<span data-ttu-id="8c39b-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="8c39b-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="8c39b-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8c39b-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="8c39b-115">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="8c39b-115">MAPI Constants</span></span>](mapi-constants.md)

