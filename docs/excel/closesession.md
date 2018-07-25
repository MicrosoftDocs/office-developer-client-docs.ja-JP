---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798775"
---
# <a name="closesession"></a>CloseSession

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
クラスターでセッションを終了します。
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>パラメーター

_SessionId_
  
> 閉じるセッションの ID。この値は、[OpenSession](opensession.md) で返された値に一致する必要があります。
    
## <a name="return-value"></a>戻り値

セッションが閉じられた場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、その他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。 
  
## <a name="see-also"></a>関連項目

- [OpenSession](opensession.md)
- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

