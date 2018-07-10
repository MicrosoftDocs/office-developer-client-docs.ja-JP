---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800136"
---
# <a name="ftmuldw"></a><span data-ttu-id="bb89f-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="bb89f-103">FtMulDw</span></span>

  
  
<span data-ttu-id="bb89f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb89f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb89f-105">32 ビットの符号なし整数を符号なしの 64 ビット整数を乗算します。</span><span class="sxs-lookup"><span data-stu-id="bb89f-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb89f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bb89f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb89f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bb89f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bb89f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="bb89f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bb89f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bb89f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bb89f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bb89f-110">Called by:</span></span>  <br/> |<span data-ttu-id="bb89f-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bb89f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="bb89f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="bb89f-112">Parameters</span></span>

 <span data-ttu-id="bb89f-113">_べき乗_</span><span class="sxs-lookup"><span data-stu-id="bb89f-113">_Multiplier_</span></span>
  
> <span data-ttu-id="bb89f-114">[in]マルチ プライアで 32 ビットの符号なし整数を含むダブル ワード。</span><span class="sxs-lookup"><span data-stu-id="bb89f-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="bb89f-115">_被乗数_</span><span class="sxs-lookup"><span data-stu-id="bb89f-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="bb89f-116">[in]_乗数_パラメーターの値が乗算されます、64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="bb89f-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bb89f-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bb89f-117">Return value</span></span>

<span data-ttu-id="bb89f-118">**FtMulDw**関数は、2 つの整数の積を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="bb89f-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="bb89f-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="bb89f-119">The two input parameters remain unchanged.</span></span> 
  
