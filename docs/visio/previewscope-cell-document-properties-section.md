---
title: '[PreviewScope] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: 図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426507"
---
# <a name="previewscope-cell-document-properties-section"></a>[PreviewScope] セル ([Document Properties] セクション)

図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。
  
|**値**|**プレビューの範囲**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 最初のページ  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | なし  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | すべてのページ  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>注釈

この値は、[プロパティ] ダイアログボックスの [概要] タブで設定することもできます **([Office]** ボタンをクリックし、[情報] タブをクリックし、[ドキュメントのプロパティ] をクリックし、[詳細プロパティ] をクリック **します**)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PreviewScope] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PreviewScope  <br/> |
   
プログラムから、インデックスによって [PreviewScope] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocPreviewScope** <br/> |
   

