---
title: NOT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: 論理式が FALSE の場合は TRUE (1) を返します。 それ以外の場合は、FALSE (0) を返します。
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413333"
---
# <a name="not-function"></a>NOT 関数

論理式が FALSE の場合は TRUE (1)  _を_ 返します。 それ以外の場合は、FALSE (0) を返します。 
  
## <a name="syntax"></a>構文

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |必須  <br/> |**String** <br/> |評価する論理式を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

Boolean
  
## <a name="example"></a>例

NOT(Height \> 0.75 in) 
  
Height が 0.75 インチ以下の場合は、1 を返します。Height が 0.75 インチより大きい場合は、0 を返します。 
  

