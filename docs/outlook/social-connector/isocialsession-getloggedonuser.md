---
title: ISocialSessionGetLoggedOnUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd6bdaf6-52d5-4308-9c3d-869f6e1a6608
description: ログオンユーザーを表す isocialprofile インターフェイスを取得します。
ms.openlocfilehash: 6c15d9d016f7445f8887f7d0fc87a1f36fb99b94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439906"
---
# <a name="isocialsessiongetloggedonuser"></a><span data-ttu-id="27569-103">ISocialSession::GetLoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="27569-103">ISocialSession::GetLoggedOnUser</span></span>

<span data-ttu-id="27569-104">ログオンユーザーを表す[isocialprofile](isocialprofileisocialperson.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="27569-104">Gets an [ISocialProfile](isocialprofileisocialperson.md) interface that represents the logged-on user.</span></span> 
  
```cpp
HRESULT _stdcall GetLoggedOnUser([out, retval] ISocialProfile** result);
```

## <a name="parameters"></a><span data-ttu-id="27569-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="27569-105">Parameters</span></span>

<span data-ttu-id="27569-106">_result_</span><span class="sxs-lookup"><span data-stu-id="27569-106">_result_</span></span>
  
> <span data-ttu-id="27569-107">読み上げiの式**alprofile**インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="27569-107">[out] An **ISocialProfile** interface.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="27569-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="27569-108">See also</span></span>

- [<span data-ttu-id="27569-109">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27569-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

