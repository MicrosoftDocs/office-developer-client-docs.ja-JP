---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800550"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="7d101-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="7d101-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="7d101-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d101-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d101-105">フォームに独自のメッセージの競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d101-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="7d101-106">メッセージとは競合している場合は複数のユーザーによって同時に編集されましたが。</span><span class="sxs-lookup"><span data-stu-id="7d101-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="7d101-107">パブリック フォルダー内のメッセージに可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d101-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="7d101-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d101-108">Parameters</span></span>

 <span data-ttu-id="7d101-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="7d101-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="7d101-110">[in]フラグは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティ、メッセージの現在の状態を示すメッセージのコピーのビットマップへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7d101-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="7d101-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="7d101-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="7d101-112">[in]メッセージの状態に関する追加情報を提供するメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたクライアント定義またはプロバイダー定義のフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7d101-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="7d101-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="7d101-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="7d101-114">[in]メッセージのメッセージ クラスの名前を示す文字列です。</span><span class="sxs-lookup"><span data-stu-id="7d101-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="7d101-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="7d101-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="7d101-116">[in]メッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7d101-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="7d101-117">_PFolderFocus_パラメーターは、(たとえば、メッセージは、別のメッセージに埋め込まれている) 場合、このようなフォルダーが存在しない場合、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7d101-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7d101-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7d101-118">Return value</span></span>

<span data-ttu-id="7d101-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d101-119">S_OK</span></span> 
  
> <span data-ttu-id="7d101-120">フォームは、独自のメッセージの競合を処理しません。</span><span class="sxs-lookup"><span data-stu-id="7d101-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="7d101-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7d101-121">S_FALSE</span></span> 
  
> <span data-ttu-id="7d101-122">フォームは、独自のメッセージの競合を処理または対象の情報が渡されたメッセージは競合ではないです。</span><span class="sxs-lookup"><span data-stu-id="7d101-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d101-123">備考</span><span class="sxs-lookup"><span data-stu-id="7d101-123">Remarks</span></span>

<span data-ttu-id="7d101-124">フォーム ビューアーは、特定のフォームが独自のメッセージの競合を処理していないかどうかを検出する**IMAPIFormMgr::IsInConflict**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7d101-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="7d101-125">**IsInConflict**では、競合のフラグが存在する_ulMessageFlags_および_ulMessageStatus_パラメーターにビットマスクがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="7d101-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="7d101-126">競合のフラグが設定されている場合、 **IsInConflict**は、 _szMessageClass_パラメーターに渡されるメッセージ クラスを解決し、フォームは、独自の競合を処理しない場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="7d101-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="7d101-127">**IsInConflict**は、フォームは、独自の競合を処理する場合に S_FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="7d101-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="7d101-128">独自の競合を処理しないフォームでは、 [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)メソッドを使用して開く必要があり、既存のフォーム オブジェクトを再利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d101-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d101-129">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7d101-129">Notes to callers</span></span>

<span data-ttu-id="7d101-130">クライアント アプリケーションは、通常、フォルダー内の次または前のメッセージを 1 つのメッセージから、アプリケーションが移動するときに、競合に対処するあります。</span><span class="sxs-lookup"><span data-stu-id="7d101-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="7d101-131">メッセージが競合しているがそのメッセージのフォームのサーバーの競合を処理できる場合は、クライアント アプリケーションは、次または前のメッセージを表示するため、通常のコードを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d101-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="7d101-132">フォームのサーバーには、競合を処理できません、クライアント アプリケーションは必要がありますの次または前のメッセージのメッセージ クラスに気付いていなかったかのように進みます。</span><span class="sxs-lookup"><span data-stu-id="7d101-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d101-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d101-133">See also</span></span>



[<span data-ttu-id="7d101-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="7d101-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="7d101-135">PidTagMessageFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7d101-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="7d101-136">PidTagMessageStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7d101-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="7d101-137">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d101-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)
