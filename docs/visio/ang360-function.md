---
title: ANG360 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: 角度の範囲を正規化します。
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160301"
---
# <a name="ang360-function"></a>ANG360 関数

角度の範囲を 0 = 結果 \< \< 2PI ラジアン (0 = 結果 \< \< 360 度) に正規化します。
  
## <a name="syntax"></a>構文

ANG360(***angle*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |正規化する角度を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

角度  *単位*  を使用して角度を指定しない場合は、ラジアンとして解釈されます。 angle  *を*  値に変換できない場合は、値#VALUE! を返します。 
  
## <a name="example-1"></a>例 1

ANG360(395 deg)
  
35°を返します
  
## <a name="example-2"></a>例 2

ANG360(-9.8 rad)
  
2.7664 ラジアンを返します
  
## <a name="example-3"></a>例 3

ANG360(45)
  
58.31° (1.0177 ラジアン) を返します
  

