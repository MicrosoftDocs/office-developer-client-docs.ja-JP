---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ed3f793e4353cf78949a9df3a17dd3997a573f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800552"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="4f31e-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="4f31e-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="4f31e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f31e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f31e-105">フォームのメッセージ クラスに基づく新しいメッセージを作成するフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f31e-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="4f31e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4f31e-106">Parameters</span></span>

 <span data-ttu-id="4f31e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4f31e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4f31e-108">[in]フォームを開いたときに表示される進行状況のインジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4f31e-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="4f31e-109">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4f31e-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4f31e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f31e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4f31e-111">[in]フォームを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="4f31e-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="4f31e-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4f31e-112">The following flag can be set:</span></span>
    
<span data-ttu-id="4f31e-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4f31e-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4f31e-114">ステータスを指定するか、詳細についてはユーザーの入力を求めるのためのユーザー インターフェイスを表示します。</span><span class="sxs-lookup"><span data-stu-id="4f31e-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="4f31e-115">このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="4f31e-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="4f31e-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="4f31e-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="4f31e-117">[in]フォームを開くために使用されるフォームの情報オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f31e-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="4f31e-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="4f31e-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="4f31e-119">[in]作成されたフォーム オブジェクトを取得するインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f31e-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="4f31e-120">_RefiidToAsk_パラメーターを NULL にする必要がありますはできません。</span><span class="sxs-lookup"><span data-stu-id="4f31e-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="4f31e-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="4f31e-121">_ppvObj_</span></span>
  
> <span data-ttu-id="4f31e-122">[out]返されたインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f31e-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f31e-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4f31e-123">Return value</span></span>

<span data-ttu-id="4f31e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f31e-124">S_OK</span></span> 
  
> <span data-ttu-id="4f31e-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4f31e-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4f31e-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="4f31e-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="4f31e-127">フォーム オブジェクトでは、要求されたインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4f31e-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f31e-128">備考</span><span class="sxs-lookup"><span data-stu-id="4f31e-128">Remarks</span></span>

<span data-ttu-id="4f31e-129">フォームの閲覧者は、フォームのメッセージ クラスに基づく新しいメッセージを作成するフォームを開くに**IMAPIFormMgr::CreateForm**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4f31e-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="4f31e-130">**CreateForm**は、情報の指定されたフォーム オブジェクトの説明に従って、そのフォームに対するフォーム サーバーのインスタンスを作成することでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f31e-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="4f31e-131">必要な場合、 **CreateForm**は、フォームのサーバー コードをユーザーのディスクにダウンロードする[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4f31e-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="4f31e-132">_PfrminfoToActivate_パラメーターは、正しく解決されているフォーム情報オブジェクト] をポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f31e-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="4f31e-133">フォームを開いた後に、呼び出し元のフォーム ビューアーは[IPersistMessage](ipersistmessageiunknown.md)インターフェイスを使用してメッセージを設定する必要があり、フォームのビュー コンテキストを必要に応じて設定できます。</span><span class="sxs-lookup"><span data-stu-id="4f31e-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="4f31e-134">詳細については、[フォームのサーバーを起動する](launching-a-form-server.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f31e-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4f31e-135">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="4f31e-135">MFCMAPI reference</span></span>

<span data-ttu-id="4f31e-136">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4f31e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4f31e-137">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="4f31e-137">**File**</span></span>|<span data-ttu-id="4f31e-138">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="4f31e-138">**Function**</span></span>|<span data-ttu-id="4f31e-139">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="4f31e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f31e-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4f31e-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4f31e-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="4f31e-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="4f31e-142">MFCMAPI では、 **IMAPIFormMgr::CreateForm**メソッドを使用して、表示する前にフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f31e-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f31e-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f31e-143">See also</span></span>



[<span data-ttu-id="4f31e-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4f31e-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="4f31e-145">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f31e-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="4f31e-146">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f31e-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="4f31e-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4f31e-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="4f31e-148">フォームのサーバーを起動します。</span><span class="sxs-lookup"><span data-stu-id="4f31e-148">Launching a Form Server</span></span>](launching-a-form-server.md)
