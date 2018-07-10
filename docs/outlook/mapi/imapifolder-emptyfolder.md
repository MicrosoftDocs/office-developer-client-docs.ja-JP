---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7d8653b8f0cb2196319c4a9c2b4bca89c8be5a24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800499"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="75165-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="75165-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="75165-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75165-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75165-105">フォルダー自体を削除することがなく、フォルダーからすべてのメッセージとサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="75165-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="75165-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="75165-106">Parameters</span></span>

 <span data-ttu-id="75165-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="75165-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="75165-108">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="75165-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="75165-109">_UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="75165-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="75165-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="75165-110">_lpProgress_</span></span>
  
> <span data-ttu-id="75165-111">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="75165-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="75165-112">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="75165-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="75165-113">_UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="75165-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="75165-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75165-114">_ulFlags_</span></span>
  
> <span data-ttu-id="75165-115">[in]フォルダーを空にする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="75165-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="75165-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="75165-116">The following flags can be set:</span></span>
    
<span data-ttu-id="75165-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="75165-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="75165-118">メッセージに関連付けられているコンテンツが含まれるサブフォルダーを含めて、すべてのサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="75165-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="75165-119">DEL_ASSOCIATED フラグでは、呼び出しは最上位のフォルダーに対してのみ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="75165-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="75165-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="75165-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="75165-121">ソフト削除されたものも含めて、すべてのメッセージを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="75165-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="75165-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="75165-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="75165-123">操作の進行中に進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="75165-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75165-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="75165-124">Return value</span></span>

<span data-ttu-id="75165-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="75165-125">S_OK</span></span> 
  
> <span data-ttu-id="75165-126">フォルダーが正常に空になった。</span><span class="sxs-lookup"><span data-stu-id="75165-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="75165-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="75165-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="75165-128">呼び出しが成功したが、フォルダーが完全に空になりません。</span><span class="sxs-lookup"><span data-stu-id="75165-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="75165-129">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75165-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="75165-130">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="75165-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="75165-131">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="75165-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75165-132">備考</span><span class="sxs-lookup"><span data-stu-id="75165-132">Remarks</span></span>

<span data-ttu-id="75165-133">**IMAPIFolder::EmptyFolder**メソッドは、フォルダー自体を削除することがなくすべてのフォルダーの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="75165-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="75165-134">**EmptyFolder**の呼び出し、中に送信されたメッセージは削除されません。</span><span class="sxs-lookup"><span data-stu-id="75165-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="75165-135">関連のフォルダーの内容には、フォームの定義を含めることも、ビュー、ルール、カスタム フォーム、およびカスタム ソリューションのストレージの説明に使用したメッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="75165-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="75165-136">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="75165-136">Notes to implementers</span></span>

<span data-ttu-id="75165-137">フォルダーに送信されたメッセージの[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)メソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="75165-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="75165-138">送信されたメッセージは削除されません。</span><span class="sxs-lookup"><span data-stu-id="75165-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="75165-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="75165-139">Notes to callers</span></span>

<span data-ttu-id="75165-140">次の条件下で、これらの戻り値を期待してください。</span><span class="sxs-lookup"><span data-stu-id="75165-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="75165-141">**条件**</span><span class="sxs-lookup"><span data-stu-id="75165-141">**Condition**</span></span>|<span data-ttu-id="75165-142">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="75165-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75165-143">**EmptyFolder**では、フォルダーを空にしました。</span><span class="sxs-lookup"><span data-stu-id="75165-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="75165-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="75165-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="75165-145">**EmptyFolder**は、完全にフォルダーを空にできませんでした。</span><span class="sxs-lookup"><span data-stu-id="75165-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="75165-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="75165-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="75165-147">**EmptyFolder**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="75165-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="75165-148">エラー値</span><span class="sxs-lookup"><span data-stu-id="75165-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="75165-149">**EmptyFolder**が完了することではない場合と仮定しないでその作業は実行されませんでした。</span><span class="sxs-lookup"><span data-stu-id="75165-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="75165-150">**EmptyFolder**はエラーが発生する前にフォルダーの内容の一部を削除することにされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="75165-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="75165-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="75165-151">MFCMAPI reference</span></span>

<span data-ttu-id="75165-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="75165-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="75165-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="75165-153">**File**</span></span>|<span data-ttu-id="75165-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="75165-154">**Function**</span></span>|<span data-ttu-id="75165-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="75165-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="75165-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="75165-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="75165-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="75165-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="75165-158">MFCMAPI では、 **IMAPIFolder::EmptyFolder**メソッドを使用して、指定したフォルダーの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="75165-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75165-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="75165-159">See also</span></span>



[<span data-ttu-id="75165-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="75165-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="75165-161">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="75165-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="75165-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="75165-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="75165-163">エラー処理のためのマクロを使用してください。</span><span class="sxs-lookup"><span data-stu-id="75165-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
