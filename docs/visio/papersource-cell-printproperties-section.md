---
title: '[PaperSource] セル ([PrintProperties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: 用紙の給紙方法を指定します。
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406760"
---
# <a name="papersource-cell-printproperties-section"></a>[PaperSource] セル ([PrintProperties] セクション)

用紙の給紙方法を指定します。 
  
## <a name="remarks"></a>注釈

この設定は、[**プリンターの設定**] ダイアログ ボックスの [**給紙**] の設定に対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**プリンターの設定**] タブで [**設定**] をクリックします)。
  
このセル内の数値は、Microsoft Windows wingdi.h ファイルのビン選択に対して定義された定数 (DMBIN のプレフィックス) にマップされます。たとえば、値 7 は値を表DMBIN_AUTO。 
  
別の数式または CellsU プロパティを使用したプログラムから名前によって **[PaperSource]** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PaperSource  <br/> |
   
プログラムからインデックスによって PaperSource セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

