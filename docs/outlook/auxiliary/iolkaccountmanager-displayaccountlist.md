---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: '[アカウント設定] または [新しいアカウントの追加] ダイアログボックスを表示します。'
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322065"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="259e8-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="259e8-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="259e8-104">[**アカウント設定**] または [**新しいアカウントの追加**] ダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="259e8-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="259e8-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="259e8-105">Quick info</span></span>

<span data-ttu-id="259e8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="259e8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a><span data-ttu-id="259e8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="259e8-107">Parameters</span></span>

<span data-ttu-id="259e8-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="259e8-108">_hwnd_</span></span>
  
> <span data-ttu-id="259e8-109">順番表示されるダイアログボックスがモーダルであるウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="259e8-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="259e8-110">0の場合があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-110">May be zero.</span></span>
    
<span data-ttu-id="259e8-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="259e8-111">_dwFlags_</span></span>
  
> <span data-ttu-id="259e8-112">順番表示の動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="259e8-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="259e8-113">**ACCTUI_NO_WARNING**-Outlook が再起動されるまで変更が有効にならないという警告は表示されません。</span><span class="sxs-lookup"><span data-stu-id="259e8-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="259e8-114">アプリケーションが Outlook .exe でインプロセスで実行されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="259e8-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="259e8-115">**ACCTUI_SHOW_DATA_TAB**— [**データ**] タブが選択された状態で [**アカウント設定**] ダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="259e8-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="259e8-116">**ACCTUI_SHOW_ACCTWIZARD**が設定されていない場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="259e8-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="259e8-117">**ACCTUI_SHOW_ACCTWIZARD**-[**新しいアカウントの追加**] ダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="259e8-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="259e8-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="259e8-118">_wszTitle_</span></span>
  
> <span data-ttu-id="259e8-119">順番このパラメーターは使用されておらず、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="259e8-120">_ccategories_</span><span class="sxs-lookup"><span data-stu-id="259e8-120">_cCategories_</span></span>
  
> <span data-ttu-id="259e8-121">順番このパラメーターは使用されておらず、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="259e8-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="259e8-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="259e8-123">順番このパラメーターは使用されておらず、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="259e8-124">_pclsidtype_</span><span class="sxs-lookup"><span data-stu-id="259e8-124">_pclsidType_</span></span>
  
> <span data-ttu-id="259e8-125">順番このパラメーターは使用されておらず、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="259e8-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="259e8-126">Return values</span></span>

|<span data-ttu-id="259e8-127">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="259e8-127">**HRESULT**</span></span>|<span data-ttu-id="259e8-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="259e8-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="259e8-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="259e8-129">S_OK</span></span>  <br/> |<span data-ttu-id="259e8-130">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="259e8-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="259e8-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="259e8-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="259e8-132">ダイアログボックスを作成できませんでした。</span><span class="sxs-lookup"><span data-stu-id="259e8-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="259e8-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="259e8-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="259e8-134">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="259e8-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="259e8-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="259e8-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="259e8-136">[**新しいアカウントの追加**] ダイアログボックスでエラーが返されました。</span><span class="sxs-lookup"><span data-stu-id="259e8-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="259e8-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="259e8-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="259e8-138">_ccategories_、 _rgclsidCategories_、または_pclsidtype_パラメーターが NULL ではない。</span><span class="sxs-lookup"><span data-stu-id="259e8-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="259e8-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="259e8-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="259e8-140">[**アカウント設定**] ダイアログボックスでエラーが返されました。</span><span class="sxs-lookup"><span data-stu-id="259e8-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="259e8-141">解説</span><span class="sxs-lookup"><span data-stu-id="259e8-141">Remarks</span></span>

<span data-ttu-id="259e8-142">_ccategories_、 _rgclsidCategories_、 _pclsidtype_パラメーターは、現時点では使用されておらず、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="259e8-143">_wszTitle_は使用されず、NULL でもある必要があります。</span><span class="sxs-lookup"><span data-stu-id="259e8-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

