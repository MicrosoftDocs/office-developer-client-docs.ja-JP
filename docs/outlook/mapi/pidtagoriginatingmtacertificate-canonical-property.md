---
title: PidTagOriginatingMtaCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f78609537b85a89617e7b2fa8f30a4ba952805b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414810"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>PidTagOriginatingMtaCertificate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを発信したメッセージ転送エージェント (MTA) の識別子を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|識別子:  <br/> |0x0E25  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを設定すると、[送信されたアイテム] フォルダー内の送信メッセージで使用できます。
  
このプロパティは、メッセージごとの X.400 レポート属性に対応します。
  
## <a name="related-resources"></a>関連リソース

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

