---
title: '[Checked] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805025"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="bf73a-103">[Checked] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="bf73a-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="bf73a-104">ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bf73a-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bf73a-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="bf73a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="bf73a-106">**値**</span><span class="sxs-lookup"><span data-stu-id="bf73a-106">**Value**</span></span>|<span data-ttu-id="bf73a-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf73a-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf73a-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="bf73a-108">TRUE</span></span>  <br/> |<span data-ttu-id="bf73a-109">チェック マークが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bf73a-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="bf73a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="bf73a-110">FALSE</span></span>  <br/> |<span data-ttu-id="bf73a-111">チェック マークが付いていない (既定値) を表示します。</span><span class="sxs-lookup"><span data-stu-id="bf73a-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf73a-112">備考</span><span class="sxs-lookup"><span data-stu-id="bf73a-112">Remarks</span></span>

<span data-ttu-id="bf73a-113">取得するの [Checked] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf73a-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf73a-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="bf73a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="bf73a-115">アクションです。</span><span class="sxs-lookup"><span data-stu-id="bf73a-115">Actions.</span></span> <span data-ttu-id="bf73a-116">*名*です。オンになっているアクション。</span><span class="sxs-lookup"><span data-stu-id="bf73a-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="bf73a-117">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="bf73a-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="bf73a-118">プログラムから、インデックスによって [Checked] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf73a-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf73a-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bf73a-119">Section index:</span></span>  <br/> |<span data-ttu-id="bf73a-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="bf73a-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="bf73a-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bf73a-121">Row index:</span></span>  <br/> |<span data-ttu-id="bf73a-122">**visRowAction** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="bf73a-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="bf73a-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bf73a-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bf73a-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="bf73a-124">**visActionChecked**</span></span> <br/> |
   
