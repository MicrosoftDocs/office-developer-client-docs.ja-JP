---
title: PidTagOriginallyIntendedRecipAddrtype 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipAddrtype
api_type:
- COM
ms.assetid: dcfb6bd5-bff5-4a50-aec7-4bdfdabf7631
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a826f1bdf150b42b61a61b2f53870e9f170e0777
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416091"
---
# <a name="pidtagoriginallyintendedrecipaddrtype-canonical-property"></a>PidTagOriginallyIntendedRecipAddrtype 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
自動送信されたメッセージの最初に意図した受信者のアドレスの種類を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x007B  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、最初に意図したメッセージ受信者のアドレス プロパティの 1 つです。 メッセージを転送した自動エージェントによって設定する必要があります。
  
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

