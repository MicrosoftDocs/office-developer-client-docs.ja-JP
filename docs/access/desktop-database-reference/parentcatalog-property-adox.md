---
title: ParentCatalog プロパティ (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707459"
---
# <a name="parentcatalog-property-adox"></a>ParentCatalog プロパティ (ADOX)


**適用されます**Access 2013、Office 2013。

プロバイダー固有のプロパティへのアクセスを提供する、テーブルまたは列の親カタログを指定します。

## <a name="settings-and-return-values"></a>設定値および戻り値

[Catalog](catalog-object-adox.md) オブジェクトを設定および取得します。 **ParentCatalog** を開かれた **Catalog** に設定すると、テーブルまたは列を **Catalog** コレクションに追加する前に、プロバイダー固有のプロパティにアクセスできます。

## <a name="remarks"></a>解説

データ プロバイダーの中には、作成時 (テーブルまたは列が **Catalog** コレクションに追加されるとき) のみプロバイダー固有のプロパティ値を設定できるものがあります。 **Catalog** にオブジェクトを追加する前に、これらのプロパティにアクセスするには、あらかじめ **ParentCatalog** プロパティで **Catalog** を指定しておきます。

テーブルまたは列を **ParentCatalog** 以外の **Catalog** に追加すると、エラーが発生します。

