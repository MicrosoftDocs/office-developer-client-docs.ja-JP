---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 69853dbec46b08c4dc402012fb7f1074f30ebf52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801076"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="9a3ff-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9a3ff-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="9a3ff-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a3ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a3ff-105">最後のエラーに関する情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="9a3ff-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="9a3ff-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a3ff-106">Parameters</span></span>

 <span data-ttu-id="9a3ff-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9a3ff-107">_hResult_</span></span>
  
>  <span data-ttu-id="9a3ff-108">[in]エラー コードです。</span><span class="sxs-lookup"><span data-stu-id="9a3ff-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="9a3ff-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a3ff-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="9a3ff-110">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="9a3ff-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="9a3ff-111">0 でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a3ff-111">This must be 0.</span></span> 
    
 <span data-ttu-id="9a3ff-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9a3ff-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="9a3ff-113">[out]エラーに関する拡張情報を格納する**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9a3ff-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="9a3ff-114">**LPMAPIERROR**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3ff-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9a3ff-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a3ff-115">See also</span></span>



[<span data-ttu-id="9a3ff-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="9a3ff-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="9a3ff-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="9a3ff-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="9a3ff-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="9a3ff-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="9a3ff-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="9a3ff-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="9a3ff-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="9a3ff-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="9a3ff-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="9a3ff-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="9a3ff-122">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a3ff-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="9a3ff-123">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9a3ff-123">MAPI Constants</span></span>](mapi-constants.md)
