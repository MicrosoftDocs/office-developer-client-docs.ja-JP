---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801142"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="24532-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="24532-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="24532-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24532-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24532-105">メッセージ サービスからサービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="24532-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="24532-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="24532-106">Parameters</span></span>

 <span data-ttu-id="24532-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="24532-107">_lpUID_</span></span>
  
> <span data-ttu-id="24532-108">[で [チェック アウト]削除するプロバイダーを表す一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="24532-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24532-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="24532-109">Return value</span></span>

<span data-ttu-id="24532-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="24532-110">S_OK</span></span> 
  
> <span data-ttu-id="24532-111">プロバイダーは、メッセージ サービスから正しく削除されました。</span><span class="sxs-lookup"><span data-stu-id="24532-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="24532-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="24532-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="24532-113">_LpUID_パラメーターで指定された**MAPIUID**が認識されませんでした。</span><span class="sxs-lookup"><span data-stu-id="24532-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="24532-114">備考</span><span class="sxs-lookup"><span data-stu-id="24532-114">Remarks</span></span>

<span data-ttu-id="24532-115">**IProviderAdmin::DeleteProvider**メソッドは、メッセージ サービスのサービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="24532-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="24532-116">**DeleteProvider**は、アクティブなサービスのプロバイダーが登録されている識別子のセットを_lpUID_で指定された**MAPIUID**構造を照合することによって削除するのにはサービス ・ プロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="24532-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="24532-117">メッセージ サービスのほとんどは、プロバイダー プロファイルを使用している間に削除するには許可されません。</span><span class="sxs-lookup"><span data-stu-id="24532-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="24532-118">削除するプロバイダーを使用している場合**DeleteProvider**はすぐに削除する代わりに削除のマークが付けし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="24532-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="24532-119">プロバイダーが使用されていないがときに、削除されます。</span><span class="sxs-lookup"><span data-stu-id="24532-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="24532-120">**DeleteProvider**は、プロバイダーがサービスから削除される前に、メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="24532-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="24532-121">_UlContext_パラメーターは、MSG_SERVICE_PROVIDER_DELETE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="24532-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="24532-122">メッセージ サービスのエントリ ポイント関数は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24532-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="24532-123">サービス プロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="24532-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="24532-124">サービス プロバイダーのプロファイル セクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="24532-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="24532-125">プロバイダーが削除された後、メッセージ サービスのエントリ ポイント関数は再び呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="24532-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24532-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="24532-126">See also</span></span>



[<span data-ttu-id="24532-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="24532-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="24532-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="24532-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="24532-129">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="24532-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
