---
title: '[TagName] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417911"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="8bea6-103">[TagName] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="8bea6-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="8bea6-104">アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。</span><span class="sxs-lookup"><span data-stu-id="8bea6-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8bea6-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="8bea6-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8bea6-106">注釈</span><span class="sxs-lookup"><span data-stu-id="8bea6-106">Remarks</span></span>

 <span data-ttu-id="8bea6-107">[Action Tags] セクションの [TagName] セルは、[Actions] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。</span><span class="sxs-lookup"><span data-stu-id="8bea6-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="8bea6-108">[Actions] セクションの行には、[tagname] セルがあり、このセルと同じ tagname セル値が指定されている行には、このアクションタグに対して実行するアクションが定義されています。</span><span class="sxs-lookup"><span data-stu-id="8bea6-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="8bea6-109">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8bea6-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8bea6-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="8bea6-110">Cell name:</span></span>  <br/> | <span data-ttu-id="8bea6-111">タグ.</span><span class="sxs-lookup"><span data-stu-id="8bea6-111">SmartTags.</span></span>  <span data-ttu-id="8bea6-112">*名前*です。TagName。 SmartTags</span><span class="sxs-lookup"><span data-stu-id="8bea6-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="8bea6-113">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="8bea6-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="8bea6-114">プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bea6-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8bea6-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8bea6-115">Section index:</span></span>  <br/> |<span data-ttu-id="8bea6-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="8bea6-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="8bea6-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8bea6-117">Row index:</span></span>  <br/> |<span data-ttu-id="8bea6-118">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="8bea6-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8bea6-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8bea6-119">Cell index:</span></span>  <br/> |<span data-ttu-id="8bea6-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="8bea6-120">**visSmartTagName**</span></span> <br/> |
   

