---
title: '[EventDblClick] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: 図形をダブルクリックしたときに評価されるイベント セルです。
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805323"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="aae6c-103">[EventDblClick] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="aae6c-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="aae6c-104">図形をダブルクリックしたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="aae6c-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aae6c-105">備考</span><span class="sxs-lookup"><span data-stu-id="aae6c-105">Remarks</span></span>

<span data-ttu-id="aae6c-106">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="aae6c-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="aae6c-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって EventDblClick] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="aae6c-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aae6c-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="aae6c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="aae6c-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="aae6c-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="aae6c-110">プログラムから、インデックスによって [EventDblClick] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="aae6c-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aae6c-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="aae6c-111">Section index:</span></span>  <br/> |<span data-ttu-id="aae6c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aae6c-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aae6c-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="aae6c-113">Row index:</span></span>  <br/> |<span data-ttu-id="aae6c-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="aae6c-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="aae6c-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="aae6c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="aae6c-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="aae6c-116">**visEvtCellDblClick**</span></span> <br/> |
   
