---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799488"
---
# <a name="iolkaccountnotify"></a><span data-ttu-id="73616-102">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="73616-102">IOlkAccountNotify</span></span>

<span data-ttu-id="73616-103">アカウントへの変更をクライアントにコールバックを提供します。</span><span class="sxs-lookup"><span data-stu-id="73616-103">Provides a callback to the client for changes to an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="73616-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="73616-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73616-105">継承します。</span><span class="sxs-lookup"><span data-stu-id="73616-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="73616-106">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="73616-106">IOlkErrorUnknown</span></span>](iolkerrorunknown.md) <br/> |
|<span data-ttu-id="73616-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="73616-107">Provided by:</span></span>  <br/> | <span data-ttu-id="73616-108">クライアント</span><span class="sxs-lookup"><span data-stu-id="73616-108">Client</span></span>  <br/> |
|<span data-ttu-id="73616-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="73616-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="73616-110">IID_IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="73616-110">IID_IOlkAccountNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="73616-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="73616-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="73616-112">Notify</span><span class="sxs-lookup"><span data-stu-id="73616-112">Notify</span></span>](iolkaccountnotify-notify.md) <br/> |<span data-ttu-id="73616-113">指定したアカウントへの変更がクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="73616-113">Notifies the client of changes to the specified account.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73616-114">備考</span><span class="sxs-lookup"><span data-stu-id="73616-114">Remarks</span></span>

<span data-ttu-id="73616-115">このインターフェイスは、通知を設定するときに、 [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="73616-115">This interface is passed to [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) when setting up notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73616-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="73616-116">See also</span></span>

- [<span data-ttu-id="73616-117">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="73616-117">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="73616-118">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="73616-118">Constants (Account management API)</span></span>](constants-account-management-api.md)
