---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801138"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="04b22-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="04b22-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="04b22-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04b22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04b22-105">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="04b22-105">Deprecated.</span></span> <span data-ttu-id="04b22-106">プロファイルのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="04b22-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="04b22-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="04b22-107">Parameters</span></span>

 <span data-ttu-id="04b22-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="04b22-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="04b22-109">[in]変更するパスワードに関連付けられているプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="04b22-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="04b22-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="04b22-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="04b22-111">[in]現在のパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="04b22-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="04b22-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="04b22-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="04b22-113">[in]新しいパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="04b22-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="04b22-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04b22-114">_ulFlags_</span></span>
  
> <span data-ttu-id="04b22-115">[in]渡された文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="04b22-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="04b22-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="04b22-116">The following flag can be set:</span></span>
    
<span data-ttu-id="04b22-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="04b22-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="04b22-118">プロファイル名とパスワード、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="04b22-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="04b22-119">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。</span><span class="sxs-lookup"><span data-stu-id="04b22-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04b22-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="04b22-120">Return value</span></span>

<span data-ttu-id="04b22-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="04b22-121">S_OK</span></span> 
  
> <span data-ttu-id="04b22-122">このメソッドが呼び出されると、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="04b22-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="04b22-123">ただし、動作も起こりません。</span><span class="sxs-lookup"><span data-stu-id="04b22-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04b22-124">備考</span><span class="sxs-lookup"><span data-stu-id="04b22-124">Remarks</span></span>

<span data-ttu-id="04b22-125">このメソッドを使用することはしません。</span><span class="sxs-lookup"><span data-stu-id="04b22-125">Do not use this method.</span></span> <span data-ttu-id="04b22-126">MAPI は、プロファイルのパスワードをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="04b22-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04b22-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="04b22-127">See also</span></span>



[<span data-ttu-id="04b22-128">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04b22-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
