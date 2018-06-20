---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800451"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**適用されます**: Outlook 
  
ボタン コントロールを有効または無効にするかどうかを示す値を取得します。
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulState_
  
> [out]ボタン コントロールの状態を示す値へのポインター。 次の値のいずれかが返されます。
    
MAPI_DISABLED 
  
> ボタン コントロールは無効になり、クリックすることはできません。 
    
MAPI_ENABLED 
  
> ボタン コントロールを有効にし、クリックすることができます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ボタン コントロールの状態が正常に取得しました。
    
## <a name="remarks"></a>Remarks

サービス プロバイダーでは、MAPI をボタン コントロールの状態を提供する**IMAPIControl::GetState**メソッドを実装します。 ボタンが有効の場合は、マウス クリックやキー入力に応答できます。 無効の場合ボタンは淡色表示とマウス クリックやキー入力に応答しません。 
  
**GetState**および他の実装方法の詳細については[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドは、[コントロール オブジェクトの実装](control-object-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl: IUnknown](imapicontroliunknown.md)
