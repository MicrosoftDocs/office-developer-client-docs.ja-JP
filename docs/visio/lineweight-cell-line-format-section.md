---
title: '[LineWeight] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: 図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805716"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="86287-104">[LineWeight] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="86287-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="86287-p102">図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86287-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86287-107">注釈</span><span class="sxs-lookup"><span data-stu-id="86287-107">Remarks</span></span>

<span data-ttu-id="86287-108">LineWeight の値を [**線**] ダイアログ ボックスで設定することも ([**ホーム**] タブの [**図形**] グループで、[**行**] をクリックして、[**太さ**] をポイントおよび**他の線**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="86287-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="86287-109">**Visio のオプション**] ダイアログ ボックスで指定したテキストの長さの単位を使用する測定単位を入力しない場合 (、[**ファイル**] タブをクリックし、[**オプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="86287-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="86287-110">線の太さは、図面の縮尺に依存しません。</span><span class="sxs-lookup"><span data-stu-id="86287-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="86287-111">図面縮尺を変更して、線の太さは変わりません。</span><span class="sxs-lookup"><span data-stu-id="86287-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="86287-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineWeight] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="86287-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86287-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="86287-113">Cell name:</span></span>  <br/> | <span data-ttu-id="86287-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="86287-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="86287-115">プログラムから、インデックスによって [LineWeight] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="86287-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86287-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="86287-116">Section index:</span></span>  <br/> |<span data-ttu-id="86287-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86287-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="86287-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="86287-118">Row index:</span></span>  <br/> |<span data-ttu-id="86287-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="86287-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="86287-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="86287-120">Cell index:</span></span>  <br/> |<span data-ttu-id="86287-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="86287-121">**visLineWeight**</span></span> <br/> |
   
