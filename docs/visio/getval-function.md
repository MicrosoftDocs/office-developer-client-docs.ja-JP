---
title: GETVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: セルの値を取得し、セルの値が変更された場合、数式は再計算されません。
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416889"
---
# <a name="getval-function"></a>GETVAL 関数

セルの値を取得し、セルの値が変更された場合、数式は再計算されません。
  
## <a name="syntax"></a>構文

GETVAL(** *cellname* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |必須  <br/> |**String** <br/> |値を取得するセルの名前を指定します。  <br/> |
   
## <a name="example"></a>例

GETVAL(PinX) + GETVAL(PinY) + Width 
  
[PinX]、[PinY]、[Width] の各セルの値の合計を返します。 
  

