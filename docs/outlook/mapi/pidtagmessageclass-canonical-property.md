---
title: PidTagMessageClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d4e478b053bc1aa81643a60899480ac2ad9d4265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802966"
---
# <a name="pidtagmessageclass-canonical-property"></a>PidTagMessageClass の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
IPM などのメッセージの送信者が定義されているクラスを識別する文字列が含まれています。注意してください。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MESSAGE_CLASS、PR_MESSAGE_CLASS_A、PR_MESSAGE_CLASS_W  <br/> |
|識別子:  <br/> |0x001A  <br/> |
|データを入力します。  <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>備考

メッセージ クラスは、メッセージの種類を指定します。 一連のメッセージは、情報メッセージの種類を表す、定義されているプロパティとメッセージを処理する方法を決定します。 
  
これらのプロパティには、期間を含む連結された文字列が含まれています。 各文字列は、サブクラス化のレベルを表します。 たとえば、IPM.メモは、IPM のサブクラスと IPM のスーパークラスです。Note.Private。 
  
これらのプロパティは、32 127 からの ASCII 文字で構成されている必要があり、ピリオド (ASCII 46) で終了する必要があります。 並べ替えおよび比較操作を大文字の文字列として扱う必要があります。 許容される最大長は 255 文字が、MAPI の修飾子を追加する場所を確保するためにお勧めの 128 文字で元の長さを保持すること。 
  
すべてのメッセージは、これらのプロパティを再度入力する必要があります。 通常、新しいメッセージを作成するクライアント アプリケーション設定[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)が正常に戻るとすぐにされます。 クライアントは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出すときに、プロパティが設定されていない場合、メッセージ ・ ストアする必要があります設定は、IPM。 
  
MAPI によって定義された値は次のとおりです。 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM と IPC を想定スーパークラスのみ、およびメッセージの少なくとも 1 つのサブクラス修飾子を保存または送信する前に追加する必要があります。 メッセージ クラスの使用方法の詳細については、[メッセージ クラス](mapi-message-classes.md)を参照してください。 メッセージ クラスの必須およびオプションのプロパティのリストは、[メッセージのプロパティについて](message-properties-overview.md)のサブトピックを参照してください。
  
カスタム メッセージ クラスは、メッセージ クラスだけで使用するための予約済み範囲のプロパティを定義できます。 詳細については、[プロパティ識別子の詳細](mapi-property-identifier-overview.md)を参照してください。 
  
フォルダー、受信メッセージを受信するメッセージ クラスのコントロールが格納されます。 詳細については、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドを参照してください。 
  
フォームおよびフォームのサーバーとメッセージ クラスの使用方法の詳細については、[メッセージ クラスを選択する](choosing-a-message-class.md)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> プロパティとは、ボイス メールと fax メッセージを表示するための許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
