---
title: '[NoLiveDynamics] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: 図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421481"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>[NoLiveDynamics] セル ([Miscellaneous] セクション)

図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 操作中に図形は動的に更新されません。  <br/> |
| FALSE  <br/> | 操作中に図形は動的に更新されます。  <br/> |
   
## <a name="remarks"></a>注釈

ライブ ダイナミクスを無効にして、2 次元 (2-D) 図形をサイズ変更または回転すると、選択ボックスが表示されます。図形が 1 次元 (1-D) の場合は、ビジュアル フィードバックは [DynFeedback] セルの値に基づいて行われます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoLiveDynamics] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | NoLiveDynamics  <br/> |
   
プログラムから、インデックスによって [NoLiveDynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNoLiveDynamics** <br/> |
   

