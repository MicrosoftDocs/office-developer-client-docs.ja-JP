---
title: PidTagIpmNoteEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1d46110585fb5075041942560b3a8bd5d0b125a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802908"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a>PidTagIpmNoteEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
Outlook のメモ フォルダーの**エントリ Id**が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_IPM_NOTE_ENTRYID  <br/> |
|識別子:  <br/> |0x36D3  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージ ・ ストアのルート フォルダーと同様に、[受信トレイ] フォルダーに格納されます。 特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。 
  
1. 最初に、受信トレイ フォルダー内のプロパティを探します。 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。 
    
2. 場合 * * IMsgStore::GetReceiveFolder * * 成功するは、受信トレイと[IMsgStore::OpenEntry](imsgstore-openentry.md)の**エントリ Id**への参照を使用して、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得します。 
    
3. **IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと[IMAPIProp::GetProps](imapiprop-getprops.md)に返される参照を使用します。 
    
4. 1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。 そのためには、 **IMsgStore::OpenEntry**、 **lpEntryID**のメッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得するのには NULL を指定するを使用します。 
    
5. ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。
    
[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。
    
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
