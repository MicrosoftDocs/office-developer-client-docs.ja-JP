---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800039"
---
# <a name="fbadproptag"></a><span data-ttu-id="35b5b-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="35b5b-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="35b5b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35b5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35b5b-105">指定されたプロパティ タグを検証します。</span><span class="sxs-lookup"><span data-stu-id="35b5b-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35b5b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="35b5b-106">Header file:</span></span>  <br/> |<span data-ttu-id="35b5b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="35b5b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="35b5b-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="35b5b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35b5b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35b5b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35b5b-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="35b5b-110">Called by:</span></span>  <br/> |<span data-ttu-id="35b5b-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="35b5b-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="35b5b-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="35b5b-112">Parameters</span></span>

 <span data-ttu-id="35b5b-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="35b5b-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="35b5b-114">[in]検証するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="35b5b-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35b5b-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="35b5b-115">Return value</span></span>

<span data-ttu-id="35b5b-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="35b5b-116">TRUE</span></span> 
  
> <span data-ttu-id="35b5b-117">指定されたプロパティ タグは、有効な MAPI プロパティ タグではありません。</span><span class="sxs-lookup"><span data-stu-id="35b5b-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="35b5b-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="35b5b-118">FALSE</span></span> 
  
> <span data-ttu-id="35b5b-119">指定されたプロパティ タグは、有効な MAPI プロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="35b5b-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35b5b-120">備考</span><span class="sxs-lookup"><span data-stu-id="35b5b-120">Remarks</span></span>

<span data-ttu-id="35b5b-121">**FBadPropTag**関数では、MAPI 定義に基づいて、指定されたプロパティ タグを検証します。</span><span class="sxs-lookup"><span data-stu-id="35b5b-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="35b5b-122">Sures プロパティの型は、MAPI によって定義された型のいずれかをその型のプロパティの識別子が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="35b5b-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35b5b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="35b5b-123">See also</span></span>



[<span data-ttu-id="35b5b-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="35b5b-124">FBadProp</span></span>](fbadprop.md)
