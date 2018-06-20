---
title: PidTagProfileServerVersion の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803193"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>PidTagProfileServerVersion の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
Microsoft Outlook プロファイル内のアカウントが接続されている、Microsoft Exchange Server のバージョンに関する情報を指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|識別子:  <br/> |0x661B  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>備考

プロファイルが Exchange Server に接続する 1 つまたは複数のアカウントを指定できますが、同一の Exchange Server に接続する必要があります。
  
Microsoft Office Outlook 2007 より前のバージョンの Outlook は、アクティブなプロファイルが接続されている Exchange Server のバージョンに関する情報を格納するには、このプロパティを作成できます。 ただし、バージョン情報の形式は、Exchange Server のバージョンごとに異なります。 たとえば、 **PR_PROFILE_SERVER_VERSION** 10 進値 6944 メジャーのみを表すために Outlook ストアは、Microsoft Exchange Server 2003 の**6.5.6944.3**のバージョン id の番号を構築します。 Exchange 2007 接続の場合は、メジャー バージョン番号を格納する Outlook とメジャー ビルド番号のプロパティでこれらの数値の場合は、連結された 16 進数表現。 **8.0.685.24**の Exchange 2007 のバージョン識別子は、10 進数でメジャー バージョン番号 8 とメジャー ビルド番号 685 を持ちます。 0x8 と 0x2AD を取得する両方の数値を 16 進数に変換します。 これら 2 つの数値を連結するには、Outlook 格納値 0x82AD **PR_PROFILE_SERVER_VERSION**で 16 進数表現でします。 
  
Outlook 2007 の読み取りまたはこのプロパティへの書き込みはないです。 **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** をサポートします。 
  
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
