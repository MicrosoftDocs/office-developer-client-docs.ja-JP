---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800027"
---
# <a name="fbadprop"></a><span data-ttu-id="bbd9f-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="bbd9f-103">FBadProp</span></span>

  
  
<span data-ttu-id="bbd9f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbd9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbd9f-105">指定されたプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbd9f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bbd9f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bbd9f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bbd9f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bbd9f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bbd9f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bbd9f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bbd9f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-110">Called by:</span></span>  <br/> |<span data-ttu-id="bbd9f-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bbd9f-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="bbd9f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="bbd9f-112">Parameters</span></span>

 <span data-ttu-id="bbd9f-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="bbd9f-113">_lpprop_</span></span>
  
> <span data-ttu-id="bbd9f-114">[in]検証するプロパティを定義する[SPropValue](spropvalue.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbd9f-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bbd9f-115">Return value</span></span>

<span data-ttu-id="bbd9f-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="bbd9f-116">TRUE</span></span> 
  
> <span data-ttu-id="bbd9f-117">指定されたプロパティが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="bbd9f-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="bbd9f-118">FALSE</span></span> 
  
> <span data-ttu-id="bbd9f-119">指定したプロパティは、無効です。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbd9f-120">備考</span><span class="sxs-lookup"><span data-stu-id="bbd9f-120">Remarks</span></span>

<span data-ttu-id="bbd9f-121">サービス プロバイダーは、プロパティを設定する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドへの呼び出しの準備など、いくつかの理由の**FBadProp**関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="bbd9f-122">**FBadProp**は、プロパティの型によって指定されたプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="bbd9f-123">たとえば、プロパティがブール値の場合は、 **FBadProp** sures の値が TRUE または false を指定します。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="bbd9f-124">プロパティがバイナリの場合は、 **FBadProp**のポインターとサイズを確認、正しく割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bbd9f-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbd9f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbd9f-125">See also</span></span>



[<span data-ttu-id="bbd9f-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="bbd9f-126">FBadPropTag</span></span>](fbadproptag.md)
