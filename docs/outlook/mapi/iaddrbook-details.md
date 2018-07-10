---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fbe7f02555f76532896c951f50648c528c250a58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800390"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="d811a-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="d811a-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="d811a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d811a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d811a-105">特定のアドレス帳のエントリに関する詳細情報を表示するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d811a-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d811a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d811a-106">Parameters</span></span>

 <span data-ttu-id="d811a-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d811a-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d811a-108">[in]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d811a-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="d811a-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="d811a-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="d811a-110">[in][DISMISSMODELESS](dismissmodeless.md)のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d811a-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="d811a-111">このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d811a-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="d811a-112">MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じるとき**の詳細**] ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="d811a-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="d811a-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="d811a-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="d811a-114">[in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="d811a-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="d811a-115">このパラメーターは、 _ulFlags_パラメーターに DIALOG_SDI フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d811a-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d811a-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d811a-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="d811a-117">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="d811a-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d811a-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d811a-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="d811a-119">[in]詳細情報が表示されているエントリのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d811a-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="d811a-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="d811a-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="d811a-121">[in][LPFNBUTTON](lpfnbutton.md)関数のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d811a-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="d811a-122">**LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="d811a-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="d811a-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="d811a-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="d811a-124">[in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用されていたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d811a-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="d811a-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="d811a-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="d811a-126">[in]そのボタンは拡張可能な場合、[追加] ボタンに適用するテキストを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d811a-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="d811a-127">拡張ボタンを必要としない場合、 _lpszButtonText_パラメーターは NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d811a-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="d811a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d811a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="d811a-129">[in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d811a-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d811a-130">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d811a-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="d811a-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d811a-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="d811a-132">**詳細**が S_OK を返すことを示しますアドレスに実際に変更を加えた場合。それ以外の場合、**詳細**は、S_FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="d811a-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="d811a-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d811a-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d811a-134">Outlook 以外のクライアントでは常に表示は、一般的なアドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="d811a-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="d811a-135">このフラグは、DIALOG_SDI と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="d811a-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d811a-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="d811a-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="d811a-137">モードレスのバージョンの共通のアドレス] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="d811a-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d811a-138">Outlook 以外のクライアントでは、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d811a-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="d811a-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d811a-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d811a-140">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="d811a-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d811a-141">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d811a-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d811a-142">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d811a-142">Return value</span></span>

<span data-ttu-id="d811a-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="d811a-143">S_OK</span></span> 
  
> <span data-ttu-id="d811a-144">詳細] ダイアログ ボックスは、アドレス帳のエントリを正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="d811a-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d811a-145">備考</span><span class="sxs-lookup"><span data-stu-id="d811a-145">Remarks</span></span>

<span data-ttu-id="d811a-146">クライアント アプリケーションでは、アドレス帳の特定のエントリに関する詳細情報を提供するダイアログ ボックスを表示する**詳細**のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d811a-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="d811a-147">ボタンを追加する、クライアントの定義] ダイアログ ボックスに、 _lpfButtonCallback_、 _lpvButtonContext_、および_lpszButtonText_パラメーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d811a-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="d811a-148">ボタンがクリックされると、MAPI は、 _lpvButtonContext_のボタンとデータの両方のエントリ id を渡すこと_lpfButtonCallback_で指定されたコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d811a-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="d811a-149">場合は、[拡張] ボタンを使用する必要はありません、 _lpszButtonText_は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d811a-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="d811a-150">**詳細**は、Unicode 文字の文字列をサポートしています。Unicode 文字列は、[詳細] タブに表示される前に、マルチバイト文字 (MBCS) の文字列形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="d811a-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d811a-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="d811a-151">MFCMAPI reference</span></span>

<span data-ttu-id="d811a-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d811a-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d811a-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="d811a-153">**File**</span></span>|<span data-ttu-id="d811a-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="d811a-154">**Function**</span></span>|<span data-ttu-id="d811a-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="d811a-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d811a-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="d811a-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="d811a-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="d811a-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="d811a-158">MFCMAPI では、**詳細**メソッドを使用して、アドレス帳エントリの詳細情報を示すダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="d811a-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d811a-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="d811a-159">See also</span></span>



[<span data-ttu-id="d811a-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="d811a-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="d811a-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="d811a-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="d811a-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="d811a-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="d811a-163">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d811a-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="d811a-164">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d811a-164">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
