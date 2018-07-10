---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800820"
---
# <a name="imapitableabort"></a><span data-ttu-id="404f3-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="404f3-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="404f3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="404f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="404f3-105">テーブルの現在進行中のすべての非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="404f3-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="404f3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="404f3-106">Parameters</span></span>

<span data-ttu-id="404f3-107">なし</span><span class="sxs-lookup"><span data-stu-id="404f3-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="404f3-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="404f3-108">Return value</span></span>

<span data-ttu-id="404f3-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="404f3-109">S_OK</span></span> 
  
> <span data-ttu-id="404f3-110">1 つまたは複数の非同期操作が中止されました。</span><span class="sxs-lookup"><span data-stu-id="404f3-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="404f3-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="404f3-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="404f3-112">非同期操作の進行中および停止することはできませんまたはが既に完了しました。</span><span class="sxs-lookup"><span data-stu-id="404f3-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="404f3-113">備考</span><span class="sxs-lookup"><span data-stu-id="404f3-113">Remarks</span></span>

<span data-ttu-id="404f3-114">**IMAPITable::Abort**メソッドは、実行中である非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="404f3-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="404f3-115">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="404f3-115">Notes to callers</span></span>

<span data-ttu-id="404f3-116">非同期操作が行われているについては、 [IMAPITable::GetStatus](imapitable-getstatus.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="404f3-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="404f3-117">**中止**すると、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドの呼び出しの処理が停止し、テーブルの状態は、**アボート**の呼び出しが処理されるときにあります。</span><span class="sxs-lookup"><span data-stu-id="404f3-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="404f3-118">**中止**すると、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドの呼び出しの処理が停止し、テーブルの並べ替え順序に影響がないと、 **SortTable**の呼び出しの前に、と同じままになります。</span><span class="sxs-lookup"><span data-stu-id="404f3-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="404f3-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="404f3-119">See also</span></span>



[<span data-ttu-id="404f3-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="404f3-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="404f3-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="404f3-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="404f3-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="404f3-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="404f3-123">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="404f3-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
