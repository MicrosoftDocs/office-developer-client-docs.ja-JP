---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: IOlkAccount インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406200"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

[IOlkAccount](iolkaccount.md)インターフェイスによって割り当てられたメモリを解放します。 
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>パラメーター

_pv_
  
> [in]解放するメモリへのポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)によって割り当てられたメモリを解放するには、このメソッドを使用します (指定したアカウント プロパティの値がバイナリまたは文字列型の場合) と[IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)です。
  
## <a name="see-also"></a>関連項目

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

