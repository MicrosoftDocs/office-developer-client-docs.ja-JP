---
title: '[FillForegndTrans] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: 図形の塗りつぶしのパターンに対して、前景 (ストローク部分) に適用される透過性レベルを指定します。
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427851"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a>[FillForegndTrans] セル ([Fill Format] セクション)

図形の塗りつぶしのパターンに対して、前景 (ストローク部分) に適用される透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 ～ 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% 単位の値に丸められます。値 100% は完全な透明を表します。塗りつぶしが完全に透明な図形は、図面ページでは塗りつぶしがない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。
  
この値は、[**塗りつぶし**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックして、[**塗りつぶしのオプション**] をクリックします)。この値は、前景と背景の両方に対する塗りつぶしの透過性を制御します。これらの値を個別に設定するには、[シェイプシート] ウィンドウでそれぞれの値を入力する必要があります。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillForegndTrans] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |FillForegndTrans  <br/> |
   
プログラムから、インデックスによって [FillForegndTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillForegndTrans** <br/> |
   

