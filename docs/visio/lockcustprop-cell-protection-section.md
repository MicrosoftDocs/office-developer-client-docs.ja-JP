---
title: '[LockCustProp] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: かどうかユーザーを追加、削除、したり、[図形データ] ウィンドウの [図形データの定義] ダイアログ ボックスまたはショート カット メニューを使用してユーザー インターフェイス (UI) 内の図形データの変更を決定します。
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805752"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="cc802-103">[LockCustProp] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="cc802-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="cc802-104">かどうかユーザーを追加、削除、したり、[**図形データ**] ウィンドウの [**図形データの定義**] ダイアログ ボックスまたはショート カット メニューを使用してユーザー インターフェイス (UI) 内の図形データの変更を決定します。</span><span class="sxs-lookup"><span data-stu-id="cc802-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="cc802-105">**値**</span><span class="sxs-lookup"><span data-stu-id="cc802-105">**Value**</span></span>|<span data-ttu-id="cc802-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="cc802-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc802-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="cc802-107">TRUE</span></span>  <br/> |<span data-ttu-id="cc802-108">[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**のコマンドは無効です。</span><span class="sxs-lookup"><span data-stu-id="cc802-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="cc802-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="cc802-109">FALSE</span></span>  <br/> |<span data-ttu-id="cc802-110">[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**コマンドが有効になっている (既定値)。</span><span class="sxs-lookup"><span data-stu-id="cc802-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc802-111">注釈</span><span class="sxs-lookup"><span data-stu-id="cc802-111">Remarks</span></span>

<span data-ttu-id="cc802-112">この値が TRUE の場合でも、図形データ項目の値は変更できます。また、[シェイプシート] ウィンドウの [図形データ] セクションも変更できます。</span><span class="sxs-lookup"><span data-stu-id="cc802-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="cc802-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockCustProp] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="cc802-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc802-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="cc802-114">Cell name:</span></span>  <br/> |<span data-ttu-id="cc802-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="cc802-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="cc802-116">プログラムから、インデックスによって [LockCustProp] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="cc802-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc802-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc802-117">Section index:</span></span>  <br/> |<span data-ttu-id="cc802-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc802-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cc802-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc802-119">Row index:</span></span>  <br/> |<span data-ttu-id="cc802-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="cc802-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="cc802-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc802-121">Cell index:</span></span>  <br/> |<span data-ttu-id="cc802-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="cc802-122">**visLockCustProp**</span></span> <br/> |
   
