---
title: '[UIVisibility] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806742"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="3819a-103">[UIVisibility] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3819a-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="3819a-104">ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3819a-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="3819a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3819a-105">**Value**</span></span>|<span data-ttu-id="3819a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3819a-106">**Description**</span></span>|<span data-ttu-id="3819a-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="3819a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3819a-108">0</span><span class="sxs-lookup"><span data-stu-id="3819a-108">0</span></span>  <br/> |<span data-ttu-id="3819a-109">UI 内にページ名を表示します (既定値)。</span><span class="sxs-lookup"><span data-stu-id="3819a-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="3819a-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="3819a-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="3819a-111">1</span><span class="sxs-lookup"><span data-stu-id="3819a-111">1</span></span>  <br/> |<span data-ttu-id="3819a-112">UI 内にページ名を表示しません。</span><span class="sxs-lookup"><span data-stu-id="3819a-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="3819a-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="3819a-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3819a-114">備考</span><span class="sxs-lookup"><span data-stu-id="3819a-114">Remarks</span></span>

<span data-ttu-id="3819a-115">UIVisibility セルを**visUIVHidden**に設定すると、ページでページ名を含む文字列が表示される UI の任意の場所に表示できなくなります。</span><span class="sxs-lookup"><span data-stu-id="3819a-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="3819a-116">などのページが、**ドローイング エクスプ ローラー]** または [ページ] タブのオプションとして表示はされません。</span><span class="sxs-lookup"><span data-stu-id="3819a-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="3819a-117">ページのアクセスは可能ただし、ページ名、たとえば、 **[印刷**] コマンドが含まれていないオートメーションまたは UI パスを使用する場合。</span><span class="sxs-lookup"><span data-stu-id="3819a-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="3819a-118">このセルは、ドキュメントのページを使用UIVisibility のセルを**visUIVHidden**にデフォルトで設定しているマークアップ オーバーレイのページで使用するためのものではありませんし、変更しないようにします。</span><span class="sxs-lookup"><span data-stu-id="3819a-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3819a-119">ドキュメントの**印刷**] コマンドを非表示に使用すれば、背景ページ (**Type**プロパティは、 **visTypeBackground** ) で任意のページ (ページは印刷時に背景として使用するページは、背景上の図形の背景として使用されていません。印刷)。</span><span class="sxs-lookup"><span data-stu-id="3819a-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="3819a-120">ドキュメントの **[印刷**] コマンドは、インデックス付きのページでのみ機能し、背景ページのインデックスは作成されません。</span><span class="sxs-lookup"><span data-stu-id="3819a-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="3819a-121">取得する、[UIVisibility] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3819a-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3819a-122">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3819a-122">Cell name:</span></span>  <br/> |<span data-ttu-id="3819a-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="3819a-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="3819a-124">プログラムから、インデックスによって [UIVisibility] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3819a-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3819a-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3819a-125">Section index:</span></span>  <br/> |<span data-ttu-id="3819a-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3819a-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3819a-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3819a-127">Row index:</span></span>  <br/> |<span data-ttu-id="3819a-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="3819a-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="3819a-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3819a-129">Cell index:</span></span>  <br/> |<span data-ttu-id="3819a-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="3819a-130">**visPageUIVisibility**</span></span> <br/> |
   
