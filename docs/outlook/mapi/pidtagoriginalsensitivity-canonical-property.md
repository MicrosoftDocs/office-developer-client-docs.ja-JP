---
title: PidTagOriginalSensitivity の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803099"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>PidTagOriginalSensitivity の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
最初のバージョンのメッセージの送信者によって割り当てられた感度の値が含まれていますは、メッセージを転送または返信する前にします。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|識別子:  <br/> |0x002E  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) は、メッセージが最初に送信されると、クライアント アプリケーションは同じ値にこのプロパティを設定する必要があります。 後で変更することはありませんする必要があります。
  
このプロパティは、コピーしたエントリの感度を保護するためにトランスポート プロバイダーが使用します。 前方参照または**SENSITIVITY_PRIVATE**としてマークされた元のメッセージに対する返信に元のメッセージ テキストの変更をブロックすることなどのことができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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
