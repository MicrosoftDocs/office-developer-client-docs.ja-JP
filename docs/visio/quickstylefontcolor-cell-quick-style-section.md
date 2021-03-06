---
title: '[QuickStyleFontColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: 図形のテキストがアクティブなテーマから継承するクイック スタイルのフォントの色を、0 から 1 の整数で指定します。
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415027"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>[QuickStyleFontColor] セル ([クイック スタイル] セクション)

図形のテキストがアクティブなテーマから継承するクイック スタイルのフォントの色を、0 から 1 の整数で指定します。 
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形のテキストは [ダーク] のフォントの色を使用します。  <br/> |
|1  <br/> |図形のテキストは [ライト] のフォントの色を使用します。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFontColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleFontColor  <br/> |
   
プログラムから、インデックスによって [**QuickStyleFontColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleFontColor** <br/> |
   

