---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: 指定された空き時間情報データのブロック数をスキップします。
ms.openlocfilehash: 63f699d09e143a879702e8dc76beb8a969a77b82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799327"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="04e30-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="04e30-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="04e30-104">指定された空き時間情報データのブロック数をスキップします。</span><span class="sxs-lookup"><span data-stu-id="04e30-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="04e30-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="04e30-105">Quick info</span></span>

<span data-ttu-id="04e30-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04e30-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="04e30-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="04e30-107">Parameters</span></span>

<span data-ttu-id="04e30-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="04e30-108">_celt_</span></span>
  
>  <span data-ttu-id="04e30-109">[in]スキップするのには、空き/予約済みブロックの数。</span><span class="sxs-lookup"><span data-stu-id="04e30-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="04e30-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="04e30-110">Return values</span></span>

<span data-ttu-id="04e30-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="04e30-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04e30-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="04e30-112">See also</span></span>

- [<span data-ttu-id="04e30-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="04e30-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="04e30-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="04e30-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="04e30-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="04e30-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="04e30-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="04e30-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

