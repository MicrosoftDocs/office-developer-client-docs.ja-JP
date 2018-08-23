---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 78ae0f78e154c17f774817238b2083d98a8fb809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584682"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
最後のエラーに関する情報を拡張します。
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
>  [in]エラー コードです。 
    
 _ulFlags_
  
>  [in]動作を変更するフラグです。 0 でなければなりません。 
    
 _lppMAPIError_
  
>  [out]エラーに関する拡張情報を格納する**MAPIERROR**構造体へのポインター。 **LPMAPIERROR**の型の定義の mapidefs.h を参照してください。 
    
## <a name="see-also"></a>関連項目



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI �萔](mapi-constants.md)

