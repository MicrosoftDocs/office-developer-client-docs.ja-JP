---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3cd1a19b23a3c4d3ff8a297881eb2b959585eb17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801496"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="bfa36-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="bfa36-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="bfa36-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfa36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfa36-105">プロファイル管理オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfa36-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfa36-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bfa36-106">Header file:</span></span>  <br/> |<span data-ttu-id="bfa36-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="bfa36-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="bfa36-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="bfa36-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bfa36-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bfa36-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bfa36-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bfa36-110">Called by:</span></span>  <br/> |<span data-ttu-id="bfa36-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="bfa36-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="bfa36-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="bfa36-112">Parameters</span></span>

 <span data-ttu-id="bfa36-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bfa36-113">_ulFlags_</span></span>
  
> <span data-ttu-id="bfa36-114">[in]サービスの関数のエントリのオプションを示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="bfa36-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="bfa36-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="bfa36-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="bfa36-116">[out]新しいプロファイルの管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bfa36-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bfa36-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bfa36-117">Return value</span></span>

<span data-ttu-id="bfa36-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfa36-118">S_OK</span></span> 
  
> <span data-ttu-id="bfa36-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="bfa36-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bfa36-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="bfa36-120">MFCMAPI reference</span></span>

<span data-ttu-id="bfa36-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="bfa36-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bfa36-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="bfa36-122">**File**</span></span>|<span data-ttu-id="bfa36-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="bfa36-123">**Function**</span></span>|<span data-ttu-id="bfa36-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="bfa36-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfa36-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="bfa36-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="bfa36-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="bfa36-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="bfa36-127">MFCMAPI では、 **MAPIAdminProfiles**メソッドを使用して、プロファイルの管理オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="bfa36-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfa36-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="bfa36-128">See also</span></span>



[<span data-ttu-id="bfa36-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="bfa36-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


<span data-ttu-id="bfa36-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bfa36-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
