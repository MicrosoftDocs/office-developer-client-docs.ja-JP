---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800774"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="439ca-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="439ca-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="439ca-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="439ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="439ca-105">アドレス帳へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="439ca-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="439ca-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="439ca-106">Parameters</span></span>

 <span data-ttu-id="439ca-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="439ca-107">_lpInterface_</span></span>
  
> <span data-ttu-id="439ca-108">[in]アドレス帳にアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="439ca-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="439ca-109">有効な値は、NULL の場合、標準のアドレス帳のインターフェイス[IAddrBook](iaddrbookimapiprop.md)を示す、IID_IAddrBook です。</span><span class="sxs-lookup"><span data-stu-id="439ca-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="439ca-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="439ca-110">_ulFlags_</span></span>
  
> <span data-ttu-id="439ca-111">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="439ca-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="439ca-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="439ca-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="439ca-113">[out]アドレス帳へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="439ca-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="439ca-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="439ca-114">Return value</span></span>

<span data-ttu-id="439ca-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="439ca-115">S_OK</span></span> 
  
> <span data-ttu-id="439ca-116">アドレス帳へのアクセスが提供されました。</span><span class="sxs-lookup"><span data-stu-id="439ca-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="439ca-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="439ca-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="439ca-118">呼び出しが成功したが、1 つまたは複数のアドレス帳プロバイダーをロードできませんでした。</span><span class="sxs-lookup"><span data-stu-id="439ca-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="439ca-119">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="439ca-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="439ca-120">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="439ca-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="439ca-121">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="439ca-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="439ca-122">備考</span><span class="sxs-lookup"><span data-stu-id="439ca-122">Remarks</span></span>

<span data-ttu-id="439ca-123">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::OpenAddressBook**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="439ca-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="439ca-124">サービス プロバイダーでは、通常は、密結合のメッセージは、ストア、トランスポート プロバイダー、およびアドレス帳へのアクセスを取得する**OpenAddressBook**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="439ca-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="439ca-125">さまざまなメッセージング ユーザーは、表示するアドレス] ダイアログ ボックスの検索、アドレス帳コンテナーを開くことを含め、アドレス帳のタスクでは、 **IAddrBook**の戻り値のポインターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="439ca-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="439ca-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="439ca-126">Notes to callers</span></span>

 <span data-ttu-id="439ca-127">**OpenAddressBook**は、1 つまたは複数の現在のプロファイルで、アドレス帳プロバイダーを読み込めない場合、MAPI_W_ERRORS_RETURNED を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="439ca-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="439ca-128">この値は警告であり、呼び出しは成功として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="439ca-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="439ca-129">場合でも、すべてのアドレス帳プロバイダーは、読み込みに失敗しました、 **OpenAddressBook**が成功すると、 _lppAdrBook_パラメーターで MAPI_W_ERRORS_RETURNED と、 **IAddrBook**ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="439ca-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="439ca-130">**OpenAddressBook**は、常に**IAddrBook**の有効なポインターを返す、ために使用することが終了したら解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="439ca-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="439ca-131">1 つまたは複数のアドレス帳プロバイダーは、読み込みに失敗しました、する場合は、読み込まれなかったプロバイダーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を取得するのには[IMAPISupport::GetLastError](imapisupport-getlasterror.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="439ca-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="439ca-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="439ca-132">See also</span></span>



[<span data-ttu-id="439ca-133">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="439ca-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="439ca-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="439ca-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="439ca-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="439ca-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
