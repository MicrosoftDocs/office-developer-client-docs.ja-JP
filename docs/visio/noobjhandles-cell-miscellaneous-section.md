---
title: '[NoObjHandles] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm730
localization_priority: Normal
ms.assetid: 8e1c8c8f-4ed0-0f53-f93f-3a264edc02bd
description: 選択した図形の選択ハンドルの表示/非表示を切り替えます。
ms.openlocfilehash: 8f812c2087870529cb65aa2e7d705171a5d4ca32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805947"
---
# <a name="noobjhandles-cell-miscellaneous-section"></a><span data-ttu-id="4632c-103">[NoObjHandles] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="4632c-103">NoObjHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="4632c-104">選択した図形の選択ハンドルの表示/非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="4632c-104">Switches the display of selection handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="4632c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4632c-105">**Value**</span></span>|<span data-ttu-id="4632c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4632c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4632c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4632c-107">TRUE</span></span>  <br/> | <span data-ttu-id="4632c-108">図形を選択するときに選択ハンドルが表示されません。</span><span class="sxs-lookup"><span data-stu-id="4632c-108">Selection handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="4632c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4632c-109">FALSE</span></span>  <br/> | <span data-ttu-id="4632c-110">図形を選択するときに選択ハンドルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4632c-110">Selection handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4632c-111">備考</span><span class="sxs-lookup"><span data-stu-id="4632c-111">Remarks</span></span>

<span data-ttu-id="4632c-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[NoObjHandles] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4632c-112">To get a reference to the NoObjHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4632c-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="4632c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4632c-114">NoObjHandles</span><span class="sxs-lookup"><span data-stu-id="4632c-114">NoObjHandles</span></span>  <br/> |
   
<span data-ttu-id="4632c-115">プログラムから、インデックスによって [NoObjHandles] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4632c-115">To get a reference to the NoObjHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4632c-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4632c-116">Section index:</span></span>  <br/> |<span data-ttu-id="4632c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4632c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4632c-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4632c-118">Row index:</span></span>  <br/> |<span data-ttu-id="4632c-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="4632c-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="4632c-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4632c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4632c-121">**visNoObjHandles**</span><span class="sxs-lookup"><span data-stu-id="4632c-121">**visNoObjHandles**</span></span> <br/> |
   
