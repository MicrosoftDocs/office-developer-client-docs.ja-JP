---
title: '[Value] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: 対応するユーザー定義のセルの値を指定します。
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806754"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="3d454-103">[Value] セル ([User-Defined Cells] セクション)</span><span class="sxs-lookup"><span data-stu-id="3d454-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="3d454-104">対応するユーザー定義のセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d454-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d454-105">備考</span><span class="sxs-lookup"><span data-stu-id="3d454-105">Remarks</span></span>

<span data-ttu-id="3d454-106">別のセルでこの値を参照するには、行ラベル [User.Row] に入力したユーザー定義の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d454-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="3d454-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [値] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3d454-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d454-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="3d454-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3d454-109">ユーザーです。</span><span class="sxs-lookup"><span data-stu-id="3d454-109">User.</span></span>  <span data-ttu-id="3d454-110">*名*です。値の場所のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="3d454-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="3d454-111">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="3d454-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="3d454-112">プログラムから、インデックスによって [Value] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d454-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d454-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d454-113">Section index:</span></span>  <br/> |<span data-ttu-id="3d454-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="3d454-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="3d454-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d454-115">Row index:</span></span>  <br/> |<span data-ttu-id="3d454-116">**visRowUser** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="3d454-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3d454-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3d454-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3d454-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="3d454-118">**visUserValue**</span></span> <br/> |
   
