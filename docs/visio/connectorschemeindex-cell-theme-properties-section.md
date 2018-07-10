---
title: '[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48ab98bd-2966-443c-b3db-befeb271550f
description: 整数値で、図形に適用されているテーマのコネクタの設定を決定します。
ms.openlocfilehash: 3d918a7e8cc9c4134ccf25894367b24eaccf43b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805098"
---
# <a name="connectorschemeindex-cell-theme-properties-section"></a><span data-ttu-id="ea3e4-103">[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="ea3e4-103">ConnectorSchemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="ea3e4-104">整数値で、図形に適用されているテーマのコネクタの設定を決定します。</span><span class="sxs-lookup"><span data-stu-id="ea3e4-104">Determines the connector scheme of a theme that is applied to the shape, as an integer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ea3e4-105">備考</span><span class="sxs-lookup"><span data-stu-id="ea3e4-105">Remarks</span></span>

<span data-ttu-id="ea3e4-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ConnectorSchemeIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ea3e4-106">To get a reference to the **ConnectorSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea3e4-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="ea3e4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="ea3e4-108">ConnectorSchemeIndex</span><span class="sxs-lookup"><span data-stu-id="ea3e4-108">ConnectorSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="ea3e4-109">プログラムから、インデックスによって [ **ConnectorSchemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea3e4-109">To get a reference to the **ConnectorSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea3e4-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea3e4-110">Section index:</span></span>  <br/> |<span data-ttu-id="ea3e4-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ea3e4-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ea3e4-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea3e4-112">Row index:</span></span>  <br/> |<span data-ttu-id="ea3e4-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="ea3e4-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="ea3e4-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ea3e4-114">Cell index:</span></span>  <br/> |<span data-ttu-id="ea3e4-115">* * visConnectorSchemeIndex * *</span><span class="sxs-lookup"><span data-stu-id="ea3e4-115">**visConnectorSchemeIndex **</span></span> <br/> |
   
