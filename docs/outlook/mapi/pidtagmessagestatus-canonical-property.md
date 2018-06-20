---
title: PidTagMessageStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 21336e158d21bba6c7204eb446df3efc80b70e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802999"
---
# <a name="pidtagmessagestatus-canonical-property"></a>PidTagMessageStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
コンテンツ テーブル内のメッセージの状態を定義するフラグの 32 ビットのビットマップが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MSG_STATUS  <br/> |
|識別子:  <br/> |0x0E17  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

コンテンツ テーブルと 1 つまたは複数の検索結果のテーブルにメッセージが存在し、メッセージの各インスタンスが別の状態を持つことができます。 このプロパティと見なすことが、メッセージ、内容のテーブル内の列のプロパティです。 
  
クライアント アプリケーションでは、このプロパティで次のフラグのいずれかを設定できます。 
  
MSGSTATUS_ANSWERED 
  
> メッセージは既に返信されています。 
    
MSGSTATUS_DELMARKED 
  
> メッセージは、それ以降の削除のマークされています。 
    
MSGSTATUS_DRAFT 
  
> メッセージは、ドラフトのリビジョンの状態です。 
    
MSGSTATUS_HIDDEN 
  
> メッセージは、宛先のフォルダーを表示から非表示にするのには。 
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージでは、宛先のフォルダーの表示で強調表示されます。 
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージは、ローカル クライアントにダウンロードすることがなくリモート メッセージ ストアを削除対象としてマークされています。 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロード用にマークされています。 
    
MSGSTATUS_TAGGED 
  
> クライアント定義の目的は、メッセージをタグ付けされました。
    
**MSGSTATUS_DELMARKED**、 **MSGSTATUS_HIDDEN**、 **MSGSTATUS_HIGHLIGHTED**、および**MSGSTATUS_TAGGED**のフラグは、クライアントによって定義されます。 トランスポートとストアのプロバイダーは、操作をしなくても、これらのビットを渡します。 
  
クライアントは、アプリケーションに適した任意の方法でこれらの値を解釈できます。 多数のクライアントがこのプロパティを使用する方法の 1 つでは、代表的なアイコンが削除対象としてマークされたメッセージを表示します。 
  
ビューアーがリモート クライアントを設定できます**MSGSTATUS_REMOTE_DELETE**または**MSGSTATUS_REMOTE_DOWNLOAD**メッセージをリモート トランスポート プロバイダーによって提供されたヘッダーのフォルダーにします。 クライアント アプリケーションでは、各メッセージをダウンロードするか、リモート メッセージ ストアを削除するかどうかを判断するには、このフォルダー内のメッセージのヘッダーを調べることができます。 [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)メソッドを使用して、適切なフラグを設定します。 **SetMessageStatus**は、このプロパティのフラグのいずれかを設定する唯一の方法[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用することはできません。 このプロパティを取得するためには、クライアントは、 [IMAPIProp::GetProps](imapiprop-getprops.md)ではなく、 [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)を呼び出します。
  
31 (0x80000000 から 0x10000) をこのプロパティの 16 ビットは個人間メッセージ (IPM) のクライアント アプリケーションで使用できます。 他のすべてのビットは、使用するため、MAPI ので予約されています上記の表で定義されていないものは、最初に 0 に設定する必要があり、その後変更されていません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
