---
title: '[TagName] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: このアクションに関連付けられているアクション タグの名前を指定します。
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412717"
---
# <a name="tagname-cell-actions-section"></a>[TagName] セル ([Actions] セクション)

このアクションに関連付けられているアクション タグの名前を指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[Actions] セクションの [TagName] セルは、[Action Tags] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。 
  
- [アクション] 行の [TagName] セルが空白の場合、アクションはアクション タグ メニューではなく、ショートカット メニューに表示されます。
    
- [アクション] 行の [TagName] セルの値が [スマート タグ] 行の [TagName] セル値と一致する場合、アクションはアクション タグ メニューに表示されます。
    
- アクションの TagName セルに値があるが、図形タグ行の TagName 値と一致しない場合、そのアクションはアクション タグ メニューやショートカット メニューには表示されません。
    
- いくつかのスマート タグ行の [TagName] の値が同じ場合、すべてに同じアクションが表示されます。
    
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション。 *name*  .TagNamewhere アクション。  *name*  は [アクション] 行の名前です。  <br/> |
   
プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visActionTagName** <br/> |
   

