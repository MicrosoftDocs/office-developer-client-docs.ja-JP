---
title: '[PageScale] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: 現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405535"
---
# <a name="pagescale-cell-page-properties-section"></a>[PageScale] セル ([Page Properties] セクション)

現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
  
## <a name="remarks"></a>注釈

[PageScale] セルの値は、[**ページ設定**] ダイアログ ボックスの [**図面縮尺**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。このセルの値は、[**既定の縮尺**] ボックスまたは [**縮尺を指定**] ボックスに表示される 2 つの数値のうち最初の部分に当たる数値であり、[**図面縮尺**] で選択した図面縮尺の設定に応じて異なります。たとえば、図面に建築系縮尺を選択すると、ページの図面縮尺は 3/32 インチ = 1 フィート 0 インチになります。この場合 [PageScale] セルの値は 0.0938 インチ (または 3/32 インチ) になり、[DrawingScale] セルの値は 1 フィートになります。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageScale] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PageScale  <br/> |
   
プログラムから、インデックスによって [PageScale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageScale** <br/> |
   

