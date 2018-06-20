---
title: PidTagResourceType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5d494577721feba01dd9cb93f344308251a8ed33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803379"
---
# <a name="pidtagresourcetype-canonical-property"></a>PidTagResourceType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
サービス プロバイダーの種類を示す値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RESOURCE_TYPE  <br/> |
|識別子:  <br/> |0x3E03  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、次の値の 1 つだけ持つことができます。
  
MAPI_AB 
  
> アドレス帳
    
MAPI_AB_PROVIDER 
  
> アドレス帳プロバイダー
    
MAPI_HOOK_PROVIDER 
  
> スプーラー フック プロバイダー
    
MAPI_PROFILE_PROVIDER 
  
> プロファイル プロバイダー
    
MAPI_SPOOLER 
  
> スプーラーのメッセージ
    
MAPI_STORE_PROVIDER 
  
> メッセージ ストア プロバイダー
    
MAPI_SUBSYSTEM 
  
> MAPI サブシステムの内部
    
MAPI_TRANSPORT_PROVIDER 
  
> トランスポート プロバイダー
    
## <a name="related-resources"></a>関連リソース

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
