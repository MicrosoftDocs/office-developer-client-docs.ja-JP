---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427739"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカル フォーム ライブラリへのインターフェイス ポインターを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _ppfcnt_
  
> [out]ローカル フォーム ライブラリ インターフェイスへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

ポインターが返されるインターフェイスは、サードパーティのインストール プログラムがアプリケーション固有のフォームをライブラリにインストールするために使用できます。プログラムは最初に MAPI にログオンする必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnMAPIOpenLocalFormContainer  <br/> |MFCMAPI は **MAPIOpenLocalFormContainer** メソッドを使用してローカル フォーム コンテナーを開き、新しいウィンドウでレンダリングします。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

