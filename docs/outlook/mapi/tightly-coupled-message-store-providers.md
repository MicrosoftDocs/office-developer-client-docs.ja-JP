---
title: 密結合のメッセージ ストア プロバイダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 83ebb739302ca0e12604b9eaf854f273554826ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804101"
---
# <a name="tightly-coupled-message-store-providers"></a>密結合のメッセージ ストア プロバイダー

  
  
**適用されます**: Outlook 
  
メッセージ ストア プロバイダーは、トランスポート プロバイダーと密接に関連することができます。 ストア プロバイダーが、トランスポート プロバイダーは、プロセスをより効率的にメッセージを送受信するために通信できるように、2 つのプロバイダーを実装する MAPI サービス プロバイダーの手段が緊密に結び付けられます。 この方法の利点は、MAPI スプーラーを使用してではなく、相互に直接対話できる 2 つのサービス プロバイダーとパフォーマンスの向上が発生することです。 トランスポート プロバイダーにメッセージ ストア プロバイダーが密に結合するには、トランスポート プロバイダーでは、トランスポート プロバイダーの**PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) のプロパティで、メッセージ ストア プロバイダーのエントリの識別子を置く必要があります。MAPI 状態テーブル内の行です。 これにより、MAPI スプーラーを無効にして、トランスポート プロバイダーは、ストア プロバイダーに接続できます。
  
メッセージ ストア プロバイダーが密に結合する他のサービス プロバイダーの要件はありません。 メッセージ ストア プロバイダーと密に結合する最も一般的なサービス ・ プロバイダーは、トランスポート プロバイダーです。 これは、通常送信するようにし、メッセージの受信は、MAPI スプーラーを使用することがなく行うことができます。 たとえば、ユーザーは、送信メッセージを送信するときに結合されたメッセージ ストア プロバイダーおよびトランスポート プロバイダー送信ことができます直接。 結合されたサービス プロバイダーは、まず MAPI スプーラーに通知を処理し、MAPI スプーラーを無効するトランスポート プロバイダーは、メッセージ ストア プロバイダーからのメッセージを転送するプロセスを開始するまで待機し、新しいメッセージが表示されることはありません。 サーバー ベースのメッセージ ストアは、ユーザーのコンピューターとサーバー間のネットワーク トラフィックを最小限に抑えることで使用されているときに特別なメリットがあります。
  
一般に、サービス プロバイダーに緊密に結合する明確に定義されたプロシージャではありません。 ただし、次のガイドラインを使用する必要があります。
  
- サービス プロバイダーに緊密に結合するためにパフォーマンスがある場合は、結合度がこれらの部分とに関与している通常のプロセスからの MAPI サブシステムの一部を受け取ることに注意します。 これは、MAPI サブシステムの使用されていない部分があるが通常の相互作用をシミュレートする方法で、結合されたサービス プロバイダーでは、個々 の部品が相互にやり取りする必要があることを意味します。
    
- 密結合のサービス ・ プロバイダーは対話するとき、他の MAPI コンポーネントと、必要がありますまだ操作密に結合されていない場合と同じようにします。 ユーザーは、結合されたメッセージ ストア プロバイダーおよびトランスポート プロバイダーを使用して、既定のメッセージ ストアとしては、別のトランスポート プロバイダーを使用してメッセージを送信する場合など、ユーザーが外出先でコンピューターを実行し、リモート トランスポート pr に切り替えるときに発生することができます、ovider、緊密に結合されたサービス プロバイダーのメッセージ ストアの一部も協力し、MAPI スプーラー スタンドアロン メッセージ ストア プロバイダーの場合と同様です。
    
## <a name="see-also"></a>関連項目



[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)
