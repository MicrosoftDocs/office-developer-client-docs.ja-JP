---
title: PidTagRoamingDatatypes 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359557"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>PidTagRoamingDatatypes 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージに存在するストリーム プロパティを示すビットマスクが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|識別子:  <br/> |0x7C06  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |構成  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次の値の 1 つ以上に設定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000002  <br/> |フォルダー関連情報 (FAI) メッセージにディクショナリ ストリームを含め、固定 XML スキーマにシリアル化し **、PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) プロパティに格納する必要があります。 FAI メッセージに Dictionary ストリームが含まれている場合、アプリケーションはディクショナリをエントリがないとして扱う必要があります。  <br/> |
|0x00000004  <br/> |**FAI** メッセージに、任意の XML スキーマを使用する PR_ROAMING_XMLSTREAM ([PidTagRoamingXmlStream)](pidtagroamingxmlstream-canonical-property.md)プロパティに格納されている XML ストリームが含まれている必要があります。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

