---
title: HELP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: '[検索] ボックスに指定されたキーワードを含む HTML ヘルプ ファイルを開きます。'
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431338"
---
# <a name="help-function"></a>HELP 関数

[検索] ボックスに指定されたキーワードを含む HTML  *ヘルプ*  ファイルを **開** きます。 
  
## <a name="syntax"></a>構文

HELP(" ** *filename.chm!keyword* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _filename.chm!キーワード_ <br/> |必須  <br/> |**String** <br/> | ヘルプ ファイルの名前と検索対象のキーワードを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

キーワードを  *指定しない*  場合、HELP 関数はヘルプ ファイルのコンテンツ ページを開きます。 
  
## <a name="example"></a>例

HELP("visio.chm!shapesheet") 
  
Visio ヘルプ ファイルを開き、キーワード "shapesheet" を含むトピックの一覧を表示します。 
  

