---
title: 名前空間 (Access デスクトップデータベースリファレンス)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288626"
---
# <a name="namespaces"></a>名前空間

**適用先:** Access 2013、Office 2013

ADO での XML の保存形式には、次の 4 つの名前空間が使用されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefix</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>現在の<strong>Recordset</strong>のスキーマを&quot;定義する要素と属性を含む&quot;XML データ名前空間を参照します。</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>データ型定義の仕様を表します。</p></td>
</tr>
<tr class="odd">
<td><p>clr</p></td>
<td><p>ADO の <strong>Recordset</strong> プロパティおよび属性に固有の要素と属性を含む名前空間を表します。</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>現在の行セットのスキーマを表します。</p></td>
</tr>
</tbody>
</table>


仕様に定義されているように、クライアントは独自のタグをこれらの名前空間に追加することはできません。たとえば、クライアントは名前空間を "urn:schemas-microsoft-com:rowset" として定義し、"rs:MyOwnTag" などを書き込むことはできません。名前空間の詳細については、「[XML 名前空間 (英語)](https://www.w3.org/tr/xml-names/)」を参照してください。

> [!NOTE]
> [!メモ] スキーマ タグの ID は "RowsetSchema" であることが必要です。また、現在の行セットのスキーマを表すために使用される名前空間は、"#RowsetSchema" を指す必要があります。

名前空間のプレフィックス (コロンの右側で等号の左側の部分) は任意です。

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

この名前が XML ドキュメント全体で一貫して使用される限り、ユーザーはこれを任意の名前に定義できます。ADO は常に "s"、"rs"、"dt"、および "z" を書き込みますが、これらのプレフィックス名は、読み込むコンポーネント内にはハードコーディングされません。



