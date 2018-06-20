---
title: PidTagProfileServerFullVersion の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803196"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>PidTagProfileServerFullVersion の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
プロファイル内のアカウントが接続されている Microsoft Exchange Server の完全なバージョンとビルドの情報を指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|識別子:  <br/> |0x663B  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>備考

プロファイルが Exchange Server に接続する 1 つまたは複数のアカウントを指定できますが、同一の Exchange Server に接続する必要があります。
  
Microsoft Office Outlook 2007 より前のバージョンの Outlook では、このプロパティをサポートしていません。 これらのバージョンの Outlook プロファイルで**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** の存在を確認してください。 
  
一般に、アクティブなメールボックスが、Exchange Server に接続している場合は、Outlook 2007 は、アクティブなプロファイルの**PR_PROFILE_SERVER_FULL_VERSION**プロパティで完全な Exchange Server のバージョン情報を格納します。 Outlook では、メジャーおよびマイナー バージョン番号とメジャーとマイナーのビルド番号を含む**EXCHANGE_STORE_VERSION_NUM**構造体に情報を格納します。 たとえば、 **8.0.685.24**を Exchange Server のバージョンの識別子を保存するには、メジャー バージョン番号は、8 とマイナー バージョン番号は、0、メジャー ビルド番号は、685 とマイナー ビルド番号は、24 です。
  
**PR_PROFILE_SERVER_VERSION**または**PR_PROFILE_SERVER_FULL_VERSION**のいずれかのみでは、プロファイル内に存在する可能性がありますが、どちらか常に、プロファイル内に存在する保証はありません。 Outlook は、Exchange Server に正常に接続されるまでに、これらのプロパティに書き込めません。 
  
Outlook オブジェクト モデルでは、アクティブなメールボックスがホストされている Exchange Server のバージョンを検索するのには、 **ExchangeMailboxServerVersion**オブジェクトのプロパティの**名前空間**を使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
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
