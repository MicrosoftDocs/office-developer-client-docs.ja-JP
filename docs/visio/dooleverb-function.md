---
title: DOOLEVERB 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: OLE オブジェクトの動詞を実行します。
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435663"
---
# <a name="dooleverb-function"></a>DOOLEVERB 関数

OLE オブジェクトの動詞を実行します。
  
## <a name="syntax"></a>構文

DOOLEVERB(" ** *verb* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _"verb"_ <br/> |必須  <br/> |**String** <br/> |実行する動詞を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

以前のバージョンの Visio では、この関数は _DOOLEVERB に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example"></a>例

DOOLEVERB("edit")
  
OLE オブジェクト プログラムを実行し、リンクされた、または埋め込まれているオブジェクトを表示して編集できるようにします。
  

