---
title: PidTagMessageRecipientMe の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e8ae52df1dd9775f706e2b1b2dc8b17b1f47a0bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803008"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>PidTagMessageRecipientMe の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このメッセージング ユーザーが具体的には、プライマリ ()、CC (カーボン コピー)、またはこのメッセージのブラインド カーボン コピー (BCC) 受信者というし、配布リストの一部ではない場合、TRUE が格納されます。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|識別子:  <br/> |0x0059  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

このプロパティを確認するかどうかユーザー名に明示的に [受信者の一覧では、リスト内のすべてのエントリを検査せずに便利な方法を提供します。 値は**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) と**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) のプロパティと、[bcc] 情報の論理**OR**演算を表します (そうしないと表示されないのはプロパティ)。 
  
このプロパティは、受信したメッセージの受信確認の時点での自動処理を支援します。 トランスポート プロバイダーのオプションでは、このプロパティは FALSE が含まれて か、またはメッセージングのユーザーが受信者テーブルに直接表示されていない場合は含まれていません。 
  
配布リストの展開から得られるメッセージの配信は、このプロパティを設定するには発生しません。 受信者は明示的に指定する必要があります。 
  
未送信メッセージ一般には設定されませんこのプロパティ、 **PR_MESSAGE_CC_ME**、または**PR_MESSAGE_TO_ME**。 ユーザーがアクセスできる他のユーザーのプライベート、パブリック メッセージ ストアに、ディスク上のファイル ストアまたはその他の受信したメッセージ内に埋め込まれている、一般に含まれている値を設定したメッセージ内に存在する場合は、前回のトランスポート プロバイダーメッセージを配信します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
