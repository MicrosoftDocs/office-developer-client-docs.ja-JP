---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: 指定したエラーのメッセージ文字列を取得します。
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431702"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

指定したエラーのメッセージ文字列を取得します。 
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkErrorUnknown」を参照してください](iolkerrorunknown.md)。
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>パラメーター

_hr_
  
> [in]参照するエラー コード。
    
_ppwszError_
  
> [out]hr に対応  *するエラー*  メッセージです。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)

