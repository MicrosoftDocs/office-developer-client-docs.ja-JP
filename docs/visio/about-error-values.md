---
title: エラー値について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: エラー値は、誤った数式を含むセルに表示されます。
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423868"
---
# <a name="about-error-values"></a>エラー値について

エラー値は、誤った数式を含むセルに表示されます。
  
数式がエラー値を含むセルを参照すると、その数式にもエラー値が表示されます。ISERR、ISERRNA、ISERROR、または ISERRVALUE 関数を使用してエラー値を検索できます。
  
**エラー値**

||||
|:-----|:-----|:-----|
|**セルでの表示** <br/> |**数式に含まれているエラー** <br/> |**例** <br/> |
| #DIV/0!  <br/> |0 による除算  <br/> |10/0  <br/> |
| #VALUE!  <br/> | 間違ったタイプの引数またはオペランド。  <br/> | 5 + "House"  <br/> |
| #REF!  <br/> | 存在しないセルへの参照  <br/> | 存在しない別のセルを参照するセル  <br/> |
| #NUM!  <br/> | 無効な数値  <br/> | 負の数値の平方根  <br/> |
| #N/A!  <br/> | 使用できない値  <br/> | NA 関数  <br/> |
| #DIM!  <br/> | 次元の範囲を超える次元の値 (有効な指数は -128 \<= n \<= 127 の範囲の整数)  <br/> 不適切な操作で使用される次元の値  <br/> |1in^100 \* 1in^100 (結果は 1in^200 となり、次元の範囲を超える)  <br/> 5.2cm^1.5 (指数が整数ではない)  <br/> |
   

