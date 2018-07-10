---
title: '[NoCtlHandles] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: 選択した図形のコントロール ハンドルの表示/非表示を切り替えます。
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805915"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a><span data-ttu-id="eb264-103">[NoCtlHandles] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="eb264-103">NoCtlHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="eb264-104">選択した図形のコントロール ハンドルの表示/非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="eb264-104">Switches the display of control handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="eb264-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eb264-105">**Value**</span></span>|<span data-ttu-id="eb264-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb264-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eb264-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eb264-107">TRUE</span></span>  <br/> | <span data-ttu-id="eb264-108">図形を選択するときにコントロール ハンドルが表示されません。</span><span class="sxs-lookup"><span data-stu-id="eb264-108">Control handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="eb264-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eb264-109">FALSE</span></span>  <br/> | <span data-ttu-id="eb264-110">図形を選択するときにコントロール ハンドルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb264-110">Control handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb264-111">備考</span><span class="sxs-lookup"><span data-stu-id="eb264-111">Remarks</span></span>

<span data-ttu-id="eb264-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[NoCtlHandles] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="eb264-112">To get a reference to the NoCtlHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb264-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="eb264-113">Cell name:</span></span>  <br/> | <span data-ttu-id="eb264-114">NoCtlHandles</span><span class="sxs-lookup"><span data-stu-id="eb264-114">NoCtlHandles</span></span>  <br/> |
   
<span data-ttu-id="eb264-115">プログラムから、インデックスによって [NoCtlHandles] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb264-115">To get a reference to the NoCtlHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb264-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb264-116">Section index:</span></span>  <br/> |<span data-ttu-id="eb264-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb264-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb264-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb264-118">Row index:</span></span>  <br/> |<span data-ttu-id="eb264-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="eb264-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="eb264-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb264-120">Cell index:</span></span>  <br/> |<span data-ttu-id="eb264-121">**visNoCtlHandles**</span><span class="sxs-lookup"><span data-stu-id="eb264-121">**visNoCtlHandles**</span></span> <br/> |
   
