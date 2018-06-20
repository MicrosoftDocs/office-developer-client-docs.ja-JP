---
title: PidTagOwnStoreEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b9ea8af971f9a731aecab0ee6f4b8ea67b651643
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803152"
---
# <a name="pidtagownstoreentryid-canonical-property"></a>PidTagOwnStoreEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
トランスポートの密結合のメッセージ ストアのエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|識別子:  <br/> |0x3E06  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージ ストアのプロパティ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、いずれかが存在する場合に、密結合のストアのエントリの識別子を指定します。 たとえば、トランスポート プロバイダーは、個人用のフォルダーは MAPI スプーラーがストアに、トランスポート プロバイダーを接続できるようにするエントリの識別子を格納を指定できます。
  
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
