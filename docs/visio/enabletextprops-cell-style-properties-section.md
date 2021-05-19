---
title: '[EnableTextProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: スタイルにテキストのプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 3f1d87316955b4e6e40cea16634cff7645a720fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419262"
---
# <a name="enabletextprops-cell-style-properties-section"></a><span data-ttu-id="85da2-103">[EnableTextProps] セル ([Style Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="85da2-103">EnableTextProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="85da2-104">スタイルにテキストのプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="85da2-104">Determines whether a style includes text properties.</span></span>
  
|<span data-ttu-id="85da2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="85da2-105">**Value**</span></span>|<span data-ttu-id="85da2-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="85da2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85da2-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="85da2-107">TRUE</span></span>  <br/> |<span data-ttu-id="85da2-108">テキストのプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="85da2-108">Include text properties.</span></span>  <br/> |
|<span data-ttu-id="85da2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="85da2-109">FALSE</span></span>  <br/> |<span data-ttu-id="85da2-110">テキストのプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="85da2-110">Exclude text properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85da2-111">注釈</span><span class="sxs-lookup"><span data-stu-id="85da2-111">Remarks</span></span>

<span data-ttu-id="85da2-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableTextProps] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="85da2-112">To get a reference to the EnableTextProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85da2-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="85da2-113">Cell name:</span></span>  <br/> |<span data-ttu-id="85da2-114">EnableTextProps</span><span class="sxs-lookup"><span data-stu-id="85da2-114">EnableTextProps</span></span>  <br/> |
   
<span data-ttu-id="85da2-115">プログラムから、インデックスによって [EnableTextProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="85da2-115">To get a reference to the EnableTextProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85da2-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="85da2-116">Section index:</span></span>  <br/> |<span data-ttu-id="85da2-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="85da2-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="85da2-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="85da2-118">Row index:</span></span>  <br/> |<span data-ttu-id="85da2-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="85da2-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="85da2-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="85da2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="85da2-121">**visStyleIncludesText**</span><span class="sxs-lookup"><span data-stu-id="85da2-121">**visStyleIncludesText**</span></span> <br/> |
   

