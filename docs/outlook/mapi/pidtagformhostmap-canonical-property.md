---
title: PidTagFormHostMap 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433767"
---
# <a name="pidtagformhostmap-canonical-property"></a>PidTagFormHostMap 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
使用可能なフォームのホスト マップが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FORM_HOST_MAP  <br/> |
|識別子:  <br/> |0x3306  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

**IMAPIFormProp** インターフェイスで基になる構造を変更 **する場合、クライアント** アプリケーションは PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと共にこのプロパティを更新する必要があります。 
  
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

