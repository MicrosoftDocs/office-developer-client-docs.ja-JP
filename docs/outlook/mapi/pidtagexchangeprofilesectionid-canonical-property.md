---
title: PidTagExchangeProfileSectionId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 37a318df01101487fe0e8970251201c2515d1e8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802722"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>PidTagExchangeProfileSectionId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
複数の Microsoft Exchange Server アカウントを使用している場合は、アカウントを決定するために動的に生成された GUID が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|識別子:  <br/> |0x3d150102  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |複数の Exchange アカウント  <br/> |
   
## <a name="remarks"></a>備考

Microsoft Outlook 2010 と Microsoft Outlook 2013 は、1 つ 1 つの Exchange アカウントではなく、複数の Exchange アカウントをサポートします。 複数の Exchange アカウントに対応するため、MAPI プロファイルのレイアウトが変更されました。 Microsoft Office Outlook 2007 と以前のバージョンでは、プロファイルには、サーバー名、ユーザー名、およびオフライン フォルダー ファイル (.ost) などの Exchange の設定には専用の固定プロファイル セクションが含まれています。 場所です。 **PbGlobalProfileSectionGuid**プロパティの一意の識別子を使用してこれらの設定が確認されました。 交換の設定に使用されるセクションは、Exchange のグローバル プロファイル セクションと呼ばれます。 Outlook 2007 で Exchange のグローバル プロファイルの詳細については、[グローバル プロファイル セクションを開く方法](http://support.microsoft.com/kb/188482)を参照してください。
  
固定プロファイル セクションの場所は、複数の Exchange アカウントに対応するために十分ではありません。 代わりに、プロファイルに Exchange アカウントごとのセクションが存在し、そのアカウントの設定は、専用です。 交換の設定に使用される新しいセクションは、 **emsmdbUID**の一意の識別子によって識別されます。
  
メッセージにサービス プロファイルの Exchange アカウント、アカウントの作成時に動的に生成される GUID を格納するプロパティが表示されます。 この GUID は、 **PidTagExchangeProfileSectionId**プロパティに格納されます。 メッセージ ストアやアドレス帳コンテナーに属している Exchange アカウントを決定するプロパティを公開します。 メッセージ サービス テーブルにアクセスできるように、各 Exchange サービスは、このプロパティを公開します。 
  
次のインターフェイスのいずれかのクエリを実行した後、 **PidTagExchangeProfileSectionId**で[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すことによってこのプロパティを取得できます。 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)
    
- [これにより: IMAPIContainer](iabcontainerimapicontainer.md)
    
オブジェクトが Exchange に関連しては、呼び出しは**MAPI_E_NOT_FOUND**を返します。
  
アドレス帳を表示するときに、 **PidTagExchangeProfileSectionId**にあるコンテナーを制限できます。 開かれているコンテナーを作成したら、そこから**emsmdbUID**を照会できます。 注目に値します受信者を Exchange アドレス帳から選択した場合、受信者もいる**PidTagExchangeProfileSectionId**プロパティの一覧にします。 
  
> [!NOTE]
> コード サンプルおよび関数のヘッダーでは、全体では、この GUID は**emsmdbUID**と呼ばれます。 
  
Exchange アカウントの 1 つは、従来の Exchange アカウントとしてマークされます。 通常、最初のアカウントをプロファイルに追加されることです。 開くには**pbGlobalProfileSectionGuid**のすべての呼び出しは、従来のアカウントの Exchange のグローバル セクションにリダイレクトされます。 非レガシ Exchange アカウントを使用してデータをやり取りするオブジェクト モデルの呼び出しは、従来の Exchange アカウントを使用しても操作できます。 
  
従来の Exchange サービスには、 **PR_EMSMDB_LEGACY** (0x3D18000B)、 **true**メッセージ サービス テーブルに設定されているプロパティがあります。 
  
従来の**emsmdbUID**は**PidTagExchangeProfileSectionId**としてプロファイルの Outlook のグローバル プロファイル セクションでも記録されます。 複数の Exchange アカウントをサポートするために記述されたコードは、正しい**emsmdbUID**コードとの対話は、パスワードを取得する必要がありますので、従来の**emsmdbUID**を取得する必要はありません。
  
## <a name="see-also"></a>関連項目



[複数の Exchange アカウントを使用します。](using-multiple-exchange-accounts.md)


[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](http://support.microsoft.com/kb/188482)
