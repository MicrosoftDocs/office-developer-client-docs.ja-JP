---
title: Member オブジェクト (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289423"
---
# <a name="member-object-ado-md"></a>Member オブジェクト (ADO MD)


**適用先:** Access 2013、Office 2013

キューブ内のレベルのメンバー、レベルのメンバーの子、またはセルセットの軸に沿ったメンバーの位置を表します。

## <a name="remarks"></a>注釈

**Member** のプロパティは、使用されているコンテキストによって異なります。 **CubeDef** の [Level](level-object-ado-md.md) の [Member](cubedef-object-ado-md.md) には、階層の現在の [Member](children-property-ado-md.md) のすぐ下のレベルの **Members** を返す **Children** プロパティがあります。 **Position** の [Member](position-object-ado-md.md) では、 **Children** コレクションは常に空です。また、 [Type](type-property-ado-md.md) プロパティは、 **Level** の **Members** のみに適用されます。

**Position** の **Member** には、 [Cellset](drilleddown-property-ado-md.md) を表示する際に有用な [DrilledDown](parentsameasprev-property-ado-md.md) プロパティと [ParentSameAsPrev](cellset-object-ado-md.md) プロパティがあります。 **Level** の **Member** でこの 2 つのプロパティにアクセスすると、エラーが発生します。

**Level** の **Member** オブジェクトのコレクションとプロパティを使用すると、次の操作を実行できます。

  - **Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Member](uniquename-property-ado-md.md) を識別します。

  - **Caption** プロパティを使用して、 [Member](caption-property-ado-md.md) を表示する際に使用する文字列を返します。

  - **Description** プロパティを使用して、単位または式の [Member](description-property-ado-md.md) を説明する文字列を返します。

  - **Type** プロパティを使用して、 [Member](type-property-ado-md.md) の種類を特定します。

  - **LevelDepth** プロパティと **LevelName** プロパティを使用して、 [Member](leveldepth-property-ado-md.md) の [Level](levelname-property-ado-md.md) に関する情報を取得します。

  - **Parent** プロパティと [Children](hierarchy-object-ado-md.md) プロパティを使用して、 [Hierarchy](parent-property-ado-md.md) の関連する [Members](children-property-ado-md.md) を取得します。

  - **ChildCount** プロパティを使用して、 [Member](childcount-property-ado-md.md) の子の数をカウントします。

  - 標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Level** オブジェクトに関する追加情報を取得します。

**Axis** に沿って **Position** の [Member](axis-object-ado-md.md) オブジェクトのコレクションとプロパティを使用すると、次の操作を実行できます。

  - **Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Member](uniquename-property-ado-md.md) を識別します。

  - **Caption** プロパティを使用して、 [Member](caption-property-ado-md.md) を表示する際に使用する文字列を返します。

  - **Description** プロパティを使用して、メジャーまたは式の [Member](description-property-ado-md.md) を説明する文字列を返します。

  - **LevelDepth** プロパティと **LevelName** プロパティを使用して、 [Member](leveldepth-property-ado-md.md) の [Level](levelname-property-ado-md.md) に関する情報を取得します。

  - **ChildCount** プロパティを使用して、 [Member](childcount-property-ado-md.md) の子の数をカウントします。

  - [DrilledDown](drilleddown-property-ado-md.md) プロパティを使用して、 **Axis** 上のこの **Member** の直下に少なくとも 1 つの子があるかどうかを特定します。

  - [ParentSameAsPrev](parentsameasprev-property-ado-md.md) プロパティを使用して、この **Member** の親が **Member** の直上の親と同じかどうかを特定します。

  - 標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、**Level** オブジェクトに関する追加情報を取得します。

**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CatalogName</p></td>
<td><p>このキューブが属しているカタログの名前。</p></td>
</tr>
<tr class="even">
<td><p>ChildrenCardinality</p></td>
<td><p>メンバーの子の数。</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>キューブの名前。</p></td>
</tr>
<tr class="even">
<td><p>説明</p></td>
<td><p>メンバーの説明。</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p><a href="dimension-object-ado-md.md">次元</a>の明確な名前。</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>階層の明確な名前。</p></td>
</tr>
<tr class="odd">
<td><p>levelnumber</p></td>
<td><p>階層のルートとレベルの距離。</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>レベルの明確な名前。</p></td>
</tr>
<tr class="odd">
<td><p>メンバーキャプション</p></td>
<td><p>メンバーに関連付けられているラベルまたはキャプション。</p></td>
</tr>
<tr class="even">
<td><p>memberguid</p></td>
<td><p>メンバーの GUID。</p></td>
</tr>
<tr class="odd">
<td><p>MemberName</p></td>
<td><p>メンバーの名前。</p></td>
</tr>
<tr class="even">
<td><p>memberordinal</p></td>
<td><p>メンバーの序数。</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>メンバーの種類。</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>メンバーの明確な名前。</p></td>
</tr>
<tr class="odd">
<td><p>parentcount</p></td>
<td><p>このメンバーが持っている親の数。</p></td>
</tr>
<tr class="even">
<td><p>parentlevel</p></td>
<td><p>メンバーの親のレベル番号。</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>メンバーの親の明確な名前。</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>このキューブが属しているスキーマの名前。</p></td>
</tr>
</tbody>
</table>

