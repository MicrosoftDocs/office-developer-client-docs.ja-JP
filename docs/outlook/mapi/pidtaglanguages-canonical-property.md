---
title: PidTagLanguages 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLanguages
api_type:
- HeaderDef
ms.assetid: 16d4e92d-d48e-4e06-9886-2d21f3d10640
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f3d8693644020dd77877db219b000f8f8c804376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417841"
---
# <a name="pidtaglanguages-canonical-property"></a>PidTagLanguages 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージに組み込まれる言語の ASCII リストを含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LANGUAGES、PR_LANGUAGES_A、PR_LANGUAGES_W  <br/> |
|識別子:  <br/> |0x002F  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、コンマで区切られた 2 文字の国/地域コードのシーケンスが含まれています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

