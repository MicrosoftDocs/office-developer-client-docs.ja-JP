---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419885"
---
# <a name="upread"></a>UPREAD

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロードの読み取り状態状態の間にアイテムの読み取り状態 [をアップロードする情報](upload-read-status-state.md)です。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>メンバー

 _pupre_
  
>  [out] **[UPREADE エントリの](upreade.md)** ベクトル。 
    
 _cEnt_
  
>  [out] **UPREADE エントリ** の数。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[UPREADE](upreade.md)

