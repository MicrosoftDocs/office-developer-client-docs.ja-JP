---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801505"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="4fd80-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="4fd80-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="4fd80-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fd80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fd80-105">既存のセッションのコンテキストでは、フォーム ライブラリのプロバイダー オブジェクトの[IMAPIFormMgr](imapiformmgriunknown.md)インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="4fd80-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fd80-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4fd80-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fd80-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="4fd80-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4fd80-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4fd80-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4fd80-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4fd80-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4fd80-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4fd80-110">Called by:</span></span>  <br/> |<span data-ttu-id="4fd80-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4fd80-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="4fd80-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="4fd80-112">Parameters</span></span>

 <span data-ttu-id="4fd80-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="4fd80-113">_pSession_</span></span>
  
> <span data-ttu-id="4fd80-114">[in]クライアント アプリケーションによって使用中のセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4fd80-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="4fd80-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="4fd80-115">_ppmgr_</span></span>
  
> <span data-ttu-id="4fd80-116">[out]返される**IMAPIFormMgr**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4fd80-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4fd80-117">Return value</span><span class="sxs-lookup"><span data-stu-id="4fd80-117">Return value</span></span>

<span data-ttu-id="4fd80-118">なし。</span><span class="sxs-lookup"><span data-stu-id="4fd80-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fd80-119">備考</span><span class="sxs-lookup"><span data-stu-id="4fd80-119">Remarks</span></span>

<span data-ttu-id="4fd80-120">クライアント アプリケーションを**MAPIOpenFormMgr**関数の呼び出しを行った後のほとんどのフォームに関連する操作が行わフォーム ライブラリ プロバイダーまたはフォーム ライブラリ プロバイダーによって返されるインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="4fd80-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="4fd80-121">**IMAPIFormMgr**インターフェイスは、メッセージ ハンドラーを使用し、メッセージ クラスとフォーム ライブラリの間での解決策を実行するクライアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="4fd80-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4fd80-122">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="4fd80-122">MFCMAPI reference</span></span>

<span data-ttu-id="4fd80-123">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4fd80-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4fd80-124">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="4fd80-124">**File**</span></span>|<span data-ttu-id="4fd80-125">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="4fd80-125">**Function**</span></span>|<span data-ttu-id="4fd80-126">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="4fd80-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4fd80-127">MainDlg.cpp は、フォームを選択できるように、フォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="4fd80-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="4fd80-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="4fd80-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="4fd80-129">MFCMAPI では、 **MAPIOpenFormMgr**メソッドを使用して、フォームを選択できるように、フォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="4fd80-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fd80-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fd80-130">See also</span></span>



<span data-ttu-id="4fd80-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4fd80-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
