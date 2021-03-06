---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: 完了する再配置を予定するまで待機し、結果を取得します。
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431002"
---
# <a name="iolkapptrebaserendrebaseappointments"></a>IOlkApptRebaser::EndRebaseAppointments

完了する再配置を予定するまで待機し、結果を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a>パラメーター

_pContext_
  
> [in]必要があります。[IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)への呼び出しから取得されたコンテキストへのポインター。
    
_phResult_
  
> [out]必要があります。再配置の操作の結果を取得するためには、 **HRESULT** へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

