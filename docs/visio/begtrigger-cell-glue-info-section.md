---
title: '[BegTrigger] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の始点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
ms.openlocfilehash: 5dec179f1847c30c6ef563d866360b6dd31a1d88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804794"
---
# <a name="begtrigger-cell-glue-info-section"></a>[BegTrigger] セル ([Glue Info] セクション)

アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の始点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
  
## <a name="remarks"></a>備考

動的接着を使用して 1 次元図形を別の図形に接着すると、接着先の図形の [EventXFMod] セルを参照する数式がアプリケーションによって生成されます。接着先の図形が変更されると、この図形の [EventXFMod] セルを参照するすべての数式 ([BegTrigger] セルの数式も含む) が再計算されます。1 次元図形の他の数式は [BegTrigger] セルを参照し、必要に応じて 1 次元図形の始点を移動したり、図形を変形します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[BegTrigger] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | BegTrigger  <br/> |
   
プログラムから、インデックスによって [BegTrigger] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGroup** <br/> |
| セル インデックス:  <br/> |**visBegTrigger** <br/> |
   
