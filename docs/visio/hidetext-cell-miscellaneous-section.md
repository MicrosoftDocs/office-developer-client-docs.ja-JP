---
title: '[HideText] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: 図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425485"
---
# <a name="hidetext-cell-miscellaneous-section"></a>[HideText] セル ([Miscellaneous] セクション)

図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | テキストは表示されず、印刷もされません。  <br/> |
| FALSE  <br/> | テキストは表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または CellsU プロパティを使用したプログラムから名前によって **[HideText]** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | HideText  <br/> |
   
プログラムからインデックスによって [HideText] セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visHideText** <br/> |
   

