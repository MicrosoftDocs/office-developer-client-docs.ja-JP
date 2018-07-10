---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: レジストリ ストアに書き込むことによって、アカウント オブジェクトに変更をコミットします。
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799414"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="61112-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="61112-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="61112-104">レジストリ ストアに書き込むことによって、アカウント オブジェクトに変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="61112-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61112-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="61112-105">Quick info</span></span>

<span data-ttu-id="61112-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="61112-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="61112-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="61112-107">Parameters</span></span>

<span data-ttu-id="61112-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="61112-108">_dwFlags_</span></span>
  
> <span data-ttu-id="61112-109">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="61112-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="61112-110">OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。</span><span class="sxs-lookup"><span data-stu-id="61112-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="61112-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="61112-111">Return values</span></span>

|<span data-ttu-id="61112-112">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="61112-112">**HRESULT**</span></span>|<span data-ttu-id="61112-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="61112-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61112-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="61112-114">S_OK</span></span>  <br/> |<span data-ttu-id="61112-115">メソッドが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="61112-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="61112-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="61112-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="61112-117">指定されたアカウントを見つけることができません。</span><span class="sxs-lookup"><span data-stu-id="61112-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="61112-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="61112-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="61112-119">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="61112-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61112-120">注釈</span><span class="sxs-lookup"><span data-stu-id="61112-120">Remarks</span></span>

<span data-ttu-id="61112-121">[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウントのプロパティの値を変更した後は、このような変更を保存するのには**IOlkAccount::SaveChanges**を使用します。</span><span class="sxs-lookup"><span data-stu-id="61112-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61112-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="61112-122">See also</span></span>

- [<span data-ttu-id="61112-123">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="61112-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="61112-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="61112-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)
