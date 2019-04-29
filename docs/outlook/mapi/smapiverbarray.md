---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433914"
---
# <a name="smapiverbarray"></a><span data-ttu-id="4abde-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="4abde-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="4abde-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4abde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4abde-105">MAPI 動詞を記述する[smapiverb](smapiverb.md)構造の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4abde-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4abde-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4abde-106">Header file:</span></span>  <br/> |<span data-ttu-id="4abde-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="4abde-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4abde-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="4abde-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="4abde-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="4abde-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="4abde-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="4abde-110">Members</span></span>

 <span data-ttu-id="4abde-111">**cforms**</span><span class="sxs-lookup"><span data-stu-id="4abde-111">**cForms**</span></span>
  
> <span data-ttu-id="4abde-112">配列内の動詞の数。</span><span class="sxs-lookup"><span data-stu-id="4abde-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="4abde-113">**aforminfo**</span><span class="sxs-lookup"><span data-stu-id="4abde-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="4abde-114">MAPI 動詞の配列。</span><span class="sxs-lookup"><span data-stu-id="4abde-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4abde-115">注釈</span><span class="sxs-lookup"><span data-stu-id="4abde-115">Remarks</span></span>

<span data-ttu-id="4abde-116">**SMAPIVerbArray**構造体は、 [imapiforminfo:: CalcVerbSet](imapiforminfo-calcverbset.md)メソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="4abde-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4abde-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="4abde-117">See also</span></span>



[<span data-ttu-id="4abde-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="4abde-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="4abde-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="4abde-119">MAPI Structures</span></span>](mapi-structures.md)

