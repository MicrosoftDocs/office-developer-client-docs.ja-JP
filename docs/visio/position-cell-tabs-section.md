---
title: '[Position] セル ([Tabs] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409931"
---
# <a name="position-cell-tabs-section"></a>[Position] セル ([Tabs] セクション)

タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Position] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | タブ。  *ij*            は  *、i*  と  *j*  = <1>、2、3..です。  <br/> |
   
プログラムから、インデックスによって [Position] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTab** <br/> |
| 行インデックス:  <br/> |**visRowTab**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> | (*j*  *3) + **visTabPos** <br/> |
   

