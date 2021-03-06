---
title: '[BevelMaterialType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: ベベルが構成されるマテリアルの種類を指定します。
ms.openlocfilehash: b8efaa1f84594c803c79be02cd88dda1a5346dc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414586"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>[BevelMaterialType] セル ([ベベルのプロパティ] セクション)

ベベルが構成されるマテリアルの種類を指定します。 
  
|**説明**|**値**|
|:-----|:-----|
|0  <br/> |特別な材料なし  <br/> |
|1  <br/> |つや消し  <br/> |
|2  <br/> |つや消し (明るめ)  <br/> |
|3  <br/> |プラスチック  <br/> |
|4  <br/> |メタル  <br/> |
|5  <br/> |濃いエッジ  <br/> |
|6  <br/> |ぼかし  <br/> |
|7  <br/> |[Flat/なし]  <br/> |
|8  <br/> |ワイヤーフレーム  <br/> |
|9  <br/> |パウダー  <br/> |
|10  <br/> |透明パウダー  <br/> |
|11  <br/> |Clear  <br/> |
   
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素 **の N** 属性の値、または CellsU プロパティを使用するプログラムから、名前によって **[BevelMaterialType]** セルへの参照を取得するには、次の値を使用します。  
  
|||
|:-----|:-----|
| セル名:  <br/> | BevelMaterialType  <br/> |
   
プログラムからインデックスによって **[BevelMaterialType]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowBevelProperties** <br/> |
| セル インデックス:  <br/> |**visBevelMaterialType** <br/> |
   

