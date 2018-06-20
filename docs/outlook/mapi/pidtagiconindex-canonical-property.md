---
title: PidTagIconIndex の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 83ab01363d478d197286bfa8f7b5b092a7ffd5a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802834"
---
# <a name="pidtagiconindex-canonical-property"></a>PidTagIconIndex の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
電子メールのオブジェクトのグループを表示するときに使用するアイコンを表す数字が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ICON_INDEX  <br/> |
|識別子:  <br/> |0x1080  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、存在する場合は、クライアントへのヒントです。 クライアントは、このプロパティの値を無視することがあります。 
  
|**メール アイテムの状態**|**アイコンのインデックス**|
|:-----|:-----|
|新着メール  <br/> |0 xffffffff  <br/> |
|投稿  <br/> |0x00000001  <br/> |
|その他  <br/> |0x00000003  <br/> |
|メールを読む  <br/> |0x00000100  <br/> |
|未読メ ー ル  <br/> |0x00000101  <br/> |
|送信されたメール  <br/> |0x00000102  <br/> |
|未送信メール  <br/> |0x00000103  <br/> |
|受信メール  <br/> |0x00000104  <br/> |
|返信メール  <br/> |0x00000105  <br/> |
|転送されたメール  <br/> |0x00000106  <br/> |
|リモート メール  <br/> |0x00000107  <br/> |
|メールの配信  <br/> |0x00000108  <br/> |
|メールを読む  <br/> |0x00000109  <br/> |
|配信不能メール  <br/> |0x0000010A  <br/> |
|Nonread メール  <br/> |0x0000010B  <br/> |
|Recall_S メール  <br/> |0x0000010C  <br/> |
|Recall_F メール  <br/> |0x0000010D  <br/> |
|メールの追跡  <br/> |0x0000010E  <br/> |
|Office メールから  <br/> |0x0000011B  <br/> |
|メールを取り消し  <br/> |0x0000011C  <br/> |
|メッセージの追跡  <br/> |0x00000130  <br/> |
|連絡先  <br/> |0x00000200  <br/> |
|配布リスト  <br/> |0x00000202  <br/> |
|付箋の青  <br/> |0x00000300  <br/> |
|付箋緑  <br/> |0x00000301  <br/> |
|付箋ピンク  <br/> |0x00000302  <br/> |
|付箋イエロー  <br/> |0x00000303  <br/> |
|付箋ホワイト  <br/> |0x00000304  <br/> |
|単独の予定  <br/> |0x00000400  <br/> |
|定期的な予定  <br/> |0x00000401  <br/> |
|単一インスタンスの会議  <br/> |0x00000402  <br/> |
|定期的な会議  <br/> |0x00000403  <br/> |
|会議出席依頼  <br/> |0x00000404  <br/> |
|承諾  <br/> |0x00000405  <br/> |
|辞退  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0x00000407  <br/> |
|キャンセル  <br/> |0x00000408  <br/> |
|更新された情報  <br/> |0x00000409  <br/> |
|タスクとタスク  <br/> |0x00000500  <br/> |
|定期的なタスクが割り当てられていません。  <br/> |0x00000501  <br/> |
|担当者のタスク  <br/> |0x00000502  <br/> |
|仕事を割り当てた人の作業  <br/> |0x00000503  <br/> |
|仕事の依頼  <br/> |0x00000504  <br/> |
|仕事の承諾  <br/> |0x00000505  <br/> |
|タスクの辞退  <br/> |0x00000506  <br/> |
|仕訳帳の会話  <br/> |0x00000601  <br/> |
|ジャーナルの電子メール メッセージ  <br/> |0x00000602  <br/> |
|仕訳帳の会議出席依頼  <br/> |0x00000603  <br/> |
|仕訳帳の会議の応答  <br/> |0x00000604  <br/> |
|仕訳帳の仕事の依頼  <br/> |0x00000606  <br/> |
|仕訳帳のタスクの応答  <br/> |0x00000607  <br/> |
|Journal ノート  <br/> |0x00000608  <br/> |
|仕訳帳の fax  <br/> |0x00000609  <br/> |
|仕訳帳の電話  <br/> |0x0000060A  <br/> |
|仕訳帳名  <br/> |0x0000060C  <br/> |
|Microsoft Office Word の仕訳帳  <br/> |0x0000060D  <br/> |
|Microsoft Office Excel の仕訳帳  <br/> |0x0000060E  <br/> |
|Microsoft Office PowerPoint の仕訳帳  <br/> |0x0000060F  <br/> |
|仕訳帳の Microsoft Office のアクセス  <br/> |0x00000610  <br/> |
|仕訳帳文書  <br/> |0x00000612  <br/> |
|仕訳帳の会議  <br/> |0x00000613  <br/> |
|仕訳帳の会議の取り消し  <br/> |0x00000614  <br/> |
|仕訳帳のリモート セッション  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許可されている操作のプロパティを指定します。
    
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
