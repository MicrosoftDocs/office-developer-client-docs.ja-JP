---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415657"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ スレッド内のメッセージが属する場所を示します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>パラメーター

 _cbParent_
  
> [in]親会話インデックスのバイト数。
    
 _lpbParent_
  
> [in]親会話インデックス内のバイトへのポインター。 cbParent が 0 の  _場合は_ NULL になります。 
    
 _lpcbIndex_
  
> [out]呼び出しによって返される新しい会話インデックス内のバイト数へのポインター。 
    
 _lppbIndex_
  
> [out]呼び出しによって返される新しい会話インデックスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    

