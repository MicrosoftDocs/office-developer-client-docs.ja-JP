---
title: '[DisplayMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: グループ図形とそのメンバーの表示方法を指定します。
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805231"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="3f3e9-103">[DisplayMode] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3f3e9-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="3f3e9-104">グループ図形とそのメンバーの表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="3f3e9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-105">**Value**</span></span>|<span data-ttu-id="3f3e9-106">**表示モード**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-106">**Display Mode**</span></span>|<span data-ttu-id="3f3e9-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f3e9-108">0</span><span class="sxs-lookup"><span data-stu-id="3f3e9-108">0</span></span>  <br/> |<span data-ttu-id="3f3e9-109">グループ図形とテキストを表示しません。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="3f3e9-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="3f3e9-111">1</span><span class="sxs-lookup"><span data-stu-id="3f3e9-111">1</span></span>  <br/> |<span data-ttu-id="3f3e9-112">メンバー図形の背後にグループ図形を表示します。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="3f3e9-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="3f3e9-114">2</span><span class="sxs-lookup"><span data-stu-id="3f3e9-114">2</span></span>  <br/> |<span data-ttu-id="3f3e9-115">メンバー図形の手前にグループ図形を表示します。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="3f3e9-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f3e9-117">備考</span><span class="sxs-lookup"><span data-stu-id="3f3e9-117">Remarks</span></span>

<span data-ttu-id="3f3e9-118">設定することもこの値、グループを選択すると [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**図形のデザイン**グループ**の動作**] をクリックし、**データをグループ化**] ボックスの一覧から表示モードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="3f3e9-119">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって DisplayMode] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f3e9-120">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3f3e9-120">Cell name:</span></span>  <br/> |<span data-ttu-id="3f3e9-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="3f3e9-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="3f3e9-122">プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f3e9-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f3e9-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f3e9-123">Section index:</span></span>  <br/> |<span data-ttu-id="3f3e9-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3f3e9-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f3e9-125">Row index:</span></span>  <br/> |<span data-ttu-id="3f3e9-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="3f3e9-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f3e9-127">Cell index:</span></span>  <br/> |<span data-ttu-id="3f3e9-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="3f3e9-128">**visGroupDisplayMode**</span></span> <br/> |
   
