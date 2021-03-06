---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: 指定したカテゴリのアカウントの順序を取得します。
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424624"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

指定したカテゴリのアカウントの順序を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccountManager」を参照してください。](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>パラメーター

_pclsidCategory_
  
> [in]注文を取得するカテゴリ クラス ID。 値は、次のいずれかする必要があります。
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out]アカウントの数。 
    
_prgAccts_
  
> [out]アカウントの配列へのポインター。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

このメソッドを呼び出す前に、呼び出し元は配列ポインター  *prgAccts*  のみを割り当て  *、prgAccts*  が指す配列にはメモリを割り当てない。 このメソッドが返された後、呼び出し元は [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) を使用して  *prgAccts*  に割り当てられたメモリを解放する必要があります。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

