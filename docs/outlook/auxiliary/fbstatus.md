---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: 空き/予約済みブロックの空き/予約済みの状態の列挙です。
ms.openlocfilehash: 67d710f82856dc8ff4839c926018eef88d355f73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799316"
---
# <a name="fbstatus"></a><span data-ttu-id="d4945-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="d4945-103">FBStatus</span></span>

<span data-ttu-id="d4945-104">空き/予約済みブロックの空き/予約済みの状態の列挙です。</span><span class="sxs-lookup"><span data-stu-id="d4945-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d4945-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d4945-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="d4945-106">備考</span><span class="sxs-lookup"><span data-stu-id="d4945-106">Remarks</span></span>

<span data-ttu-id="d4945-107">時間帯の空き/予約済みの状態では、カレンダー上の表示方法を決定します。**空き**、**予定あり**、**仮承諾**、または**不在時の Office**です。</span><span class="sxs-lookup"><span data-stu-id="d4945-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4945-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4945-108">See also</span></span>

- [<span data-ttu-id="d4945-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="d4945-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="d4945-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="d4945-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)

