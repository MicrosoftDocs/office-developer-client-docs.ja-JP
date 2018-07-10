---
title: '[X] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: X を表す-ローカル座標での接続ポイントの座標です。
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806805"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="1c651-103">[X] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="1c651-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="1c651-104">*X*を表す-ローカル座標での接続ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="1c651-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1c651-105">備考</span><span class="sxs-lookup"><span data-stu-id="1c651-105">Remarks</span></span>

<span data-ttu-id="1c651-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="1c651-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c651-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="1c651-107">Cell name:</span></span>  <br/> | <span data-ttu-id="1c651-108">ある*i* 、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="1c651-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1c651-109">プログラムから、インデックスによって [X] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c651-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c651-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1c651-110">Section index:</span></span>  <br/> |<span data-ttu-id="1c651-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="1c651-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="1c651-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1c651-112">Row index:</span></span>  <br/> |<span data-ttu-id="1c651-113">**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="1c651-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1c651-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1c651-114">Cell index:</span></span>  <br/> |<span data-ttu-id="1c651-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="1c651-115">**visX**</span></span> <br/> |
   
