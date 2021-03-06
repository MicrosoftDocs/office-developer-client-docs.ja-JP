---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: 指定したアカウント プロパティの値を取得します。
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433739"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

指定したアカウント プロパティの値を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>パラメーター

_dwProp_
  
> [in]取得する account プロパティのプロパティ タグ。
    
_pVar_
  
> [out]指定したプロパティの値。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定したアカウントのプロパティが見つかりません。  <br/> |
|E_INVALIDARG  <br/> |無効なプロパティ タグが指定されています。  <br/> |
   
## <a name="remarks"></a>注釈

このメソッドが返された後、account プロパティの値がバイナリ型または文字列型の場合は [、IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して *pVar* を解放する必要があります。
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

