---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418289"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザー定義関数がクラスターで実行されているかどうかを示す値を返します。 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>パラメーター

この関数には引数はありません。
  
## <a name="return-value"></a>戻り値

この関数が Excel プロセスで実行される場合、**xlTypeInt** 型の **XLOPER12** で 0 が返されます。関数がクラスター上で実行される場合、戻り値の型と値は、クラスター コネクタ プロバイダーによって決まります。
  
## <a name="requirements"></a>要件

この関数は、Xlcall.h ヘッダー ファイルで定義されます。
  
## <a name="see-also"></a>関連項目

- [クラスター セーフ関数](cluster-safe-functions.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

