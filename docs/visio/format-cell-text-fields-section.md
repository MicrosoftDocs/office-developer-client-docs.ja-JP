---
title: '[Format] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805441"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="676e9-103">[Format] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="676e9-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="676e9-104">テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。</span><span class="sxs-lookup"><span data-stu-id="676e9-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="676e9-105">備考</span><span class="sxs-lookup"><span data-stu-id="676e9-105">Remarks</span></span>

<span data-ttu-id="676e9-106">Type] セルの値が 0、2、5、6、または 7 の場合 (文字列、数値、日付または時刻、期間、または通貨、それぞれ)、データの種類に適した書式形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="676e9-106">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type.</span></span> <span data-ttu-id="676e9-107">たとえば、番号 12.43 in」# # 4 UU」の図の書式設定が書式設定します。</span><span class="sxs-lookup"><span data-stu-id="676e9-107">For example, the format picture "# #/4 UU" formats the number 12.43 in.</span></span> <span data-ttu-id="676e9-108">12 2/4 インチです。</span><span class="sxs-lookup"><span data-stu-id="676e9-108">as 12 2/4 INCHES.</span></span> <span data-ttu-id="676e9-109">図の書式設定を指定する方法の詳細については、[書式形式について](about-format-pictures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="676e9-109">For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="676e9-p102">数値 ([Type] セル = 2) は寸法、スカラー、角度、日付、時刻、通貨を表現できます。入力した数値が常に日付、時刻、または通貨として評価されるようにするには、[Format] セルに、書式形式ではなく DATETIME 関数または CY 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="676e9-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="676e9-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Format] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="676e9-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="676e9-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="676e9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="676e9-114">Fields.Format [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="676e9-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="676e9-115">プログラムから、インデックスによって [Format] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="676e9-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="676e9-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="676e9-116">Section index:</span></span>  <br/> |<span data-ttu-id="676e9-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="676e9-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="676e9-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="676e9-118">Row index:</span></span>  <br/> |<span data-ttu-id="676e9-119">**visRowField** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="676e9-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="676e9-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="676e9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="676e9-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="676e9-121">**visFieldFormat**</span></span> <br/> |
   
