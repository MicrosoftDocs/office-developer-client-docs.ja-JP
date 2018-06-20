---
title: 状態を同期します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804075"
---
# <a name="synchronize-state"></a>状態を同期します。

  
  
**適用されます**: Outlook 
  
 このトピックでは、レプリケーションの状態マシンの同期状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC** <br/> |
|関連するデータ構造体。  <br/> |**[同期](sync.md)** <br/> |
|この状態。  <br/> |[アイドル状態](idle-state.md) <br/> |
|この状態。  <br/> |[階層の状態をダウンロード](download-hierarchy-state.md)[内容の状態を同期](synchronize-contents-state.md)[階層の状態をアップロード](upload-hierarchy-state.md)、またはアイドル状態  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態では、同期を開始します。 ローカル ストアは、ここからアップロードまたはダウンロードの状態に移行できます。 ローカル ストアは、フォルダー階層をサーバーにアップロードするアップロード階層状態に移行できるなど、階層を最初にアップロードしてからダウンロードして階層、サーバーから完全な同期を実行できます。
  
この状態の時に Outlook は、Outlook がその他の状態の時に変更を表示するようにローカル ストアへのパスに関連付けられている**同期**データ構造体を初期化します。 
  
クライアントが、[in] 設定の**同期**Outlook の他の状態を処理する方法を指示するメンバーです。 たとえば、クライアントは**UPS_UPLOAD_ONLY**と**UPS_THESE_FOLDERS**に*ulFlags*を設定することができ、アップロードされるとこれらのフォルダーのみを Outlook に指示するのにはフォルダーのエントリ id の一覧には、 *pel* 。 この状態が終了すると、ローカル ストアは、アイドル状態に戻ります。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)
