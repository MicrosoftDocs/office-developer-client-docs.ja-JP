---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800084"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**適用されます**: Outlook 
  
メッセージの別のフォロー アップのステータスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>メンバー

 _flwupNone_
  
> フラグが指定されていません。
    
 _flwupComplete_
  
> メッセージは完了です。
    
 _flwupMarked_
  
> メッセージは、フラグを設定します。
    
 _flwupMAX_
  
> フォロー アップのためにサポートされている別の状態の数です。
    
## <a name="see-also"></a>関連項目



[PidTagFlagStatus の標準的なプロパティ](pidtagflagstatus-canonical-property.md)

