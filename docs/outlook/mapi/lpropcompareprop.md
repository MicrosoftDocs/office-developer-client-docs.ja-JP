---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801299"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="10c70-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="10c70-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="10c70-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10c70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10c70-105">等しいかどうかを確認するのには 2 つのプロパティの値を比較します。</span><span class="sxs-lookup"><span data-stu-id="10c70-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10c70-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="10c70-106">Header file:</span></span>  <br/> |<span data-ttu-id="10c70-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="10c70-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="10c70-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="10c70-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="10c70-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="10c70-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="10c70-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="10c70-110">Called by:</span></span>  <br/> |<span data-ttu-id="10c70-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="10c70-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="10c70-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="10c70-112">Parameters</span></span>

 <span data-ttu-id="10c70-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="10c70-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="10c70-114">[in][SPropValue](spropvalue.md)構造体を比較する最初のプロパティの値を定義することへのポインター。</span><span class="sxs-lookup"><span data-stu-id="10c70-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="10c70-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="10c70-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="10c70-116">[in]**SPropValue**構造体を比較する 2 番目のプロパティの値を定義することへのポインター。</span><span class="sxs-lookup"><span data-stu-id="10c70-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="10c70-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="10c70-117">Return value</span></span>

 <span data-ttu-id="10c70-118">**LPropCompareProp**では、ほとんどのプロパティの種類を次の値のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="10c70-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="10c70-119">0 より小さいによって値が指定されている場合、 _lpSPropValueA_パラメーターは、 _lpSPropValueB_パラメーターで指定されたよりも短い。</span><span class="sxs-lookup"><span data-stu-id="10c70-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="10c70-120">_LpSPropValueB_によって示されるよりも大きく、値が_lpSPropValueA_で示されている場合は 0 より大きい値です。</span><span class="sxs-lookup"><span data-stu-id="10c70-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="10c70-121">値が_lpSPropValueA_で示されている場合は 0 では、 _lpSPropValueB_によって示される値と等しい。</span><span class="sxs-lookup"><span data-stu-id="10c70-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="10c70-122">ブール値など、組み込みの順序がないプロパティの種類またはエラーの種類は、 **LPropCompareProp**関数は、2 つのプロパティの値が等しくない場合に未定義の値を返します。</span><span class="sxs-lookup"><span data-stu-id="10c70-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="10c70-123">この未定義の値は 0 以外の値と一貫性のある複数の呼び出し</span><span class="sxs-lookup"><span data-stu-id="10c70-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10c70-124">備考</span><span class="sxs-lookup"><span data-stu-id="10c70-124">Remarks</span></span>

<span data-ttu-id="10c70-125">のみを比較する 2 つのプロパティの型が同じ場合は、 **LPropCompareProp**関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="10c70-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="10c70-126">**LPropCompareProp**を呼び出す前にクライアント アプリケーションまたはサービス プロバイダーする必要があります最初にプロパティを取得、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しと比較するため。</span><span class="sxs-lookup"><span data-stu-id="10c70-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="10c70-127">クライアントまたはプロバイダーの呼び出し**LPropCompareProp**関数が最初にいることを確認するのにはプロパティ タグを確認すると、プロパティ値の比較は、有効です。</span><span class="sxs-lookup"><span data-stu-id="10c70-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="10c70-128">関数は、適切な値を返すプロパティの値を比較します。</span><span class="sxs-lookup"><span data-stu-id="10c70-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="10c70-129">プロパティの値が等しくない場合は、 **LPropCompareProp**は、どちらが大きい方を決定します。</span><span class="sxs-lookup"><span data-stu-id="10c70-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="10c70-130">**LPropCompareProp**を比較するプロパティは、同じオブジェクトに属している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="10c70-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  
