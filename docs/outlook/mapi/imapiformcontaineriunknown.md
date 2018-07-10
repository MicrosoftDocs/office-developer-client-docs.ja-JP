---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800531"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="6be4d-103">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6be4d-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="6be4d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6be4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6be4d-105">フォーム ライブラリにフォームを管理します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-105">Manages forms in form libraries.</span></span> <span data-ttu-id="6be4d-106">このインターフェイスを使用して、アプリケーション固有のフォーム ライブラリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6be4d-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6be4d-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6be4d-107">Header file:</span></span>  <br/> |<span data-ttu-id="6be4d-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="6be4d-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6be4d-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="6be4d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="6be4d-110">フォームのコンテナー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6be4d-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="6be4d-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6be4d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="6be4d-112">フォーム ライブラリのプロバイダー</span><span class="sxs-lookup"><span data-stu-id="6be4d-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="6be4d-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6be4d-113">Called by:</span></span>  <br/> |<span data-ttu-id="6be4d-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6be4d-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="6be4d-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="6be4d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6be4d-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="6be4d-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="6be4d-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="6be4d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="6be4d-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="6be4d-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6be4d-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="6be4d-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6be4d-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="6be4d-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="6be4d-121">フォームのコンテナーには、フォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="6be4d-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="6be4d-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="6be4d-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="6be4d-123">特定のフォームは、フォームのコンテナーから削除します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="6be4d-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="6be4d-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="6be4d-125">フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="6be4d-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="6be4d-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="6be4d-127">フォームのコンテナー内のフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="6be4d-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="6be4d-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="6be4d-129">フォームのコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="6be4d-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="6be4d-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="6be4d-131">フォームのコンテナーの表示名を返します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="6be4d-132">発生しました</span><span class="sxs-lookup"><span data-stu-id="6be4d-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="6be4d-133">フォームのコンテナー オブジェクトに発生する前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="6be4d-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6be4d-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="6be4d-134">See also</span></span>



[<span data-ttu-id="6be4d-135">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6be4d-135">MAPI Interfaces</span></span>](mapi-interfaces.md)
