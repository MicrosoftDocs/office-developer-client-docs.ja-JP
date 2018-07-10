---
title: '[PageHeight] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: 図面単位で表した印刷ページの高さを指定します。
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805955"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="cc527-103">[PageHeight] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="cc527-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="cc527-104">図面単位で表した印刷ページの高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="cc527-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc527-105">注釈</span><span class="sxs-lookup"><span data-stu-id="cc527-105">Remarks</span></span>

<span data-ttu-id="cc527-106">**[ページ設定**] ダイアログ ボックスの [**ページ サイズ**] タブで、ページの高さを設定することも ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**) または手動でマウスを使用してページ サイズを変更しています。</span><span class="sxs-lookup"><span data-stu-id="cc527-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="cc527-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageHeight] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="cc527-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc527-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="cc527-108">Cell name:</span></span>  <br/> |<span data-ttu-id="cc527-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="cc527-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="cc527-110">プログラムから、インデックスによって [PageHeight] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="cc527-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc527-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc527-111">Section index:</span></span>  <br/> |<span data-ttu-id="cc527-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc527-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cc527-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc527-113">Row index:</span></span>  <br/> |<span data-ttu-id="cc527-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="cc527-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="cc527-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cc527-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cc527-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="cc527-116">**visPageHeight**</span></span> <br/> |
   
