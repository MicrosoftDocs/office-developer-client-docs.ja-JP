---
title: '[GlueType] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: 1-D 図形を別の図形に接着するときに静的接着 (点から点) と動的接着 (図形から図形) のどちらを使用するかを指定します。
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410673"
---
# <a name="gluetype-cell-glue-info-section"></a>[GlueType] セル ([Glue Info] セクション)

1-D 図形を別の図形に接着するときに静的接着 (点から点) と動的接着 (図形から図形) のどちらを使用するかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| &amp;H0  <br/> | 既定値です。動的コネクタの場合にだけ動的接着を使用します。それ以外の場合は静的接着を使用します。  <br/> |**visGlueTypeDefault** <br/> |
| &amp;H1  <br/> | 動的接着を使用します。  <br/> | Visio 2002 で廃止されました。  <br/> |
| &amp;H2  <br/> | 動的接着を使用します。  <br/> |**visGlueTypeWalking** <br/> |
| &amp;H4  <br/> | 動的接着を使用しません。  <br/> |**visGlueTypeNoWalking** <br/> |
| &amp;H8  <br/> | この 2-D 図形に対しては、動的接着による接続はできません。  <br/> |**visGlueTypeNoWalkingTo** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値が 1、2、または 3 の場合、次の操作のいずれかが行われたときに動的接着が使用されます。
  
- ユーザー インターフェイスを使用して図形が動的に接着される。
    
- プログラムを使用して別の図形の [PinX] セルまたは [PinY] セルに図形が接着される。
    
プログラムによって [PinX] または [PinY] 以外のセルに図形が接着される場合は、静的接着が使用されます。
  
この値を、動的接着を許可するものから禁止するものに変更しても、既存の動的接着が切り離されたり、変更されることはありません。[GlueType] セルで動的接着が無効になっている場合でも、プログラムからは動的接着を行うことができます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [GlueType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | GlueType  <br/> |
   
プログラムから、インデックスによって [GlueType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visGlueType** <br/> |
   

