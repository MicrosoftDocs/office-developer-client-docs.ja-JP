---
title: THEMERESTORE 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: テーマを適用するときに図形のローカル書式の値を格納し、その後でユーザーがテーマを削除した場合にローカル書式を復元できます。
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404289"
---
# <a name="themerestore-function"></a>THEMERESTORE 関数

テーマを適用するときに図形のローカル書式の値を格納し、その後でユーザーがテーマを削除した場合にローカル書式を復元できます。
  
## <a name="syntax"></a>構文

THEMERESTORE()
  
## <a name="example"></a>例

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

現在のテーマを削除するときに、以前図形に適用された個別の塗りつぶしの色書式を復元します。
  

