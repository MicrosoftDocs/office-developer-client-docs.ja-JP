---
title: PidTagSearchFolderTemplateId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4e752d3264a64ad7b467947c44d01eb7c47ec863
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803503"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>PidTagSearchFolderTemplateId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
検索に使用されているテンプレートの ID が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|識別子:  <br/> |0x6841  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |検索  <br/> |
   
## <a name="remarks"></a>備考

検索フォルダーの条件は、テンプレートによって指定されます。 検索フォルダーを定義するメッセージには、このプロパティは、対応するテンプレートを識別します。 検索条件を定義するには、テンプレートも検索から除外するフォルダーを定義、検索から除外する項目を定義および**PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)) の値を指定します。
  
検索フォルダーのテンプレートの詳細については、 [[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。
    
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
