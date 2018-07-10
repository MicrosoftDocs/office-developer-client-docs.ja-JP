---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fa439d0a6fa59bac787f09c3f894a750948a0a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800541"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="b09a7-103">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b09a7-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="b09a7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b09a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b09a7-105">フォームの定義には特定のプロパティには、クライアント アプリケーション アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="b09a7-106">フォームの情報を保持する別のオブジェクトに、フォーム ライブラリのプロバイダーは、フォームをアクティブにすることがなくクライアントにフォームを記述できます。</span><span class="sxs-lookup"><span data-stu-id="b09a7-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b09a7-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b09a7-107">Header file:</span></span>  <br/> |<span data-ttu-id="b09a7-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b09a7-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b09a7-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="b09a7-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b09a7-110">フォーム オブジェクトの情報</span><span class="sxs-lookup"><span data-stu-id="b09a7-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="b09a7-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b09a7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b09a7-112">フォーム ライブラリのプロバイダー</span><span class="sxs-lookup"><span data-stu-id="b09a7-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="b09a7-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b09a7-113">Called by:</span></span>  <br/> |<span data-ttu-id="b09a7-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b09a7-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="b09a7-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="b09a7-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b09a7-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="b09a7-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="b09a7-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="b09a7-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b09a7-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="b09a7-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="b09a7-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="b09a7-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="b09a7-120">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="b09a7-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b09a7-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="b09a7-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b09a7-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="b09a7-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="b09a7-123">フォームを使用するプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="b09a7-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="b09a7-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="b09a7-125">フォームを使用する動詞の完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="b09a7-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="b09a7-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="b09a7-127">フォームのアイコンのプロパティからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="b09a7-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="b09a7-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="b09a7-129">構成ファイル内の特定のフォームの説明を保存します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="b09a7-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="b09a7-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="b09a7-131">特定のフォームがインストールされているフォームのコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b09a7-132">備考</span><span class="sxs-lookup"><span data-stu-id="b09a7-132">Remarks</span></span>

<span data-ttu-id="b09a7-133">MapiForm.h ヘッダー ファイルで定義されているほとんどのインタ フェースとは異なり、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しを通じてほとんどのフォームの情報をエクスポートするため**IMAPIFormInfo**を[IMAPIProp](imapipropiunknown.md)インターフェイスから継承します。</span><span class="sxs-lookup"><span data-stu-id="b09a7-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b09a7-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="b09a7-134">See also</span></span>



[<span data-ttu-id="b09a7-135">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b09a7-135">MAPI Interfaces</span></span>](mapi-interfaces.md)
