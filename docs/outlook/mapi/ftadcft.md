---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800138"
---
# <a name="ftadcft"></a><span data-ttu-id="5e80f-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="5e80f-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="5e80f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e80f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e80f-105">キャリー フラグを使用して必要に応じて、別の 1 つの符号なし 64 ビット整数を追加します。</span><span class="sxs-lookup"><span data-stu-id="5e80f-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e80f-106">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="5e80f-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e80f-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e80f-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e80f-108">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5e80f-108">Called by:</span></span>  <br/> |<span data-ttu-id="5e80f-109">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5e80f-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="5e80f-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e80f-110">Parameters</span></span>

 <span data-ttu-id="5e80f-111">_ft1_</span><span class="sxs-lookup"><span data-stu-id="5e80f-111">_ft1_</span></span>
  
> <span data-ttu-id="5e80f-112">[in]追加する最初の符号なし 64 ビット整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="5e80f-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="5e80f-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="5e80f-113">_ft2_</span></span>
  
> <span data-ttu-id="5e80f-114">[in]追加する 2 番目の符号なし 64 ビット整数を格納する FILETIME 構造体。</span><span class="sxs-lookup"><span data-stu-id="5e80f-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="5e80f-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="5e80f-115">_pwCarry_</span></span>
  
> <span data-ttu-id="5e80f-116">[in, out オプション]入力では、着信へのポインターは、フラグを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e80f-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="5e80f-117">出力では、追加の実行結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e80f-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="5e80f-118">このパラメーターは、実行結果が必要でない場合、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5e80f-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e80f-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5e80f-119">Return value</span></span>

<span data-ttu-id="5e80f-120">**FtAdcFt**関数は、2 つの整数の合計を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="5e80f-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="5e80f-121">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="5e80f-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="5e80f-122">、合計の実行結果が含まれる**pwCarry**が NULL 以外の場合は、0 または 1 のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="5e80f-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5e80f-123">備考</span><span class="sxs-lookup"><span data-stu-id="5e80f-123">Remarks</span></span>

<span data-ttu-id="5e80f-124">_PwCarry_が NULL の場合に、 **FtAdcFt**関数を**FtAddFt**と同じです。</span><span class="sxs-lookup"><span data-stu-id="5e80f-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="5e80f-125">_PwCarry_が NULL でない場合は 0 ポイント、 **FtAdcFt**は、 **FtAddFt**を返す同じ**FILETIME**値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e80f-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e80f-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e80f-126">See also</span></span>



[<span data-ttu-id="5e80f-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="5e80f-127">FtAddFt</span></span>](ftaddft.md)
