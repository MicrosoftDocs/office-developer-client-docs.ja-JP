---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409693"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーを順番に閉じます。
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは、トランスポート プロバイダーのシャットダウンに成功しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、トランスポート プロバイダー オブジェクトを解放する前に **IXPProvider::Shutdown** メソッドを呼び出します。 Shutdown を **呼び出す** 前に、MAPI はプロバイダーのすべてのログオン オブジェクトを解放します。
  
## <a name="see-also"></a>関連項目



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

