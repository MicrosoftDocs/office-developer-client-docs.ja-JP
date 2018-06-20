---
title: PidTagMailPermission の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4cc97647c60322783050abbebd18726434632a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802960"
---
# <a name="pidtagmailpermission-canonical-property"></a>PidTagMailPermission の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージングのユーザーがメッセージを送信する許可されている場合 TRUE が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MAIL_PERMISSION  <br/> |
|識別子:  <br/> |0x3A0E  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが設定されていない MAPI により真の価値を持つものとして扱います。 
  
一部のエントリがいない、メールが有効な企業のディレクトリに false を指定するには、このプロパティを設定します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
