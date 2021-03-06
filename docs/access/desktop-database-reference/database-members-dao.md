---
title: Database メンバー (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2254aeff94aeb2b8b078fc4f4cd4d3ef807e597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294926"
---
# <a name="database-members-dao"></a>Database メンバー (DAO)


**適用先:** Access 2013、Office 2013

Database オブジェクトは、開いているデータベースを表します。

## <a name="methods"></a>メソッド

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
<td><p><strong><a href="database-close-method-dao.md">閉じる</a></strong></p></td>
<td><p>開いている <strong>Database</strong> を閉じます。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。 .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>新しい <strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></p></td>
<td><p>新しい<strong><a href="relation-object-dao.md">Relation</a></strong>オブジェクトを作成します (Microsoft access ワークスペースのみ)。 .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></p></td>
<td><p>新しい<strong><a href="tabledef-object-dao.md">TableDef</a></strong>オブジェクトを作成します (Microsoft access ワークスペースのみ)。 .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></p></td>
<td><p>データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></p></td>
<td><p>既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></p></td>
<td><p>部分レプリカ内の変更をフル レプリカと同期させ、部分レプリカ内のすべてのレコードを消去し、現在のレプリカ フィルターに基づいて部分レプリカのデータを再設定します (Microsoft Office Access データベース エンジンのデータベースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></p></td>
<td><p>2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>プロパティ

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
<td><p><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>開いているデータベースのソースについての情報を提供する値を設定または取得します。 値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-connection-property-dao.md">Connection</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>データベースに対応する <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを返します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-containers-property-dao.md">Containers</a></strong></p></td>
<td><p>指定したデータベースのすべての <strong>Container</strong> オブジェクトを表す <strong>Containers</strong> コレクションを返します。 読み取り専用です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></p></td>
<td><p>レプリカ セットでデザイン マスターを一意に識別する 16 バイトの値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を返します。 読み取り専用 <strong>文字列</strong> です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>指定したデータベースのすべての <strong>QueryDef</strong> オブジェクトを含む <strong>QueryDefs</strong> コレクションを返します。 読み取り専用です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>最後に呼び出した <strong><a href="connection-execute-method-dao.md">Execute</a></strong> メソッドの処理対象となったレコードの数を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>指定したデータベースの開いているレコードセットをすべて含む <strong>Recordsets</strong> コレクションを返します。 読み取り専用です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-relations-property-dao.md">Relations</a></strong></p></td>
<td><p>指定したデータベースの、すべての保存された <strong>Relation</strong> オブジェクトを含む <strong>Relations</strong> コレクションを返します。 読み取り専用です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></p></td>
<td><p>データベース レプリカを一意に識別する 16 バイトの値を取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></p></td>
<td><p>指定したデータベースに保存されたすべての <strong>TableDef</strong> オブジェクトを含む <strong>TableDefs</strong> コレクションを返します。 値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-transactions-property-dao.md">トランザクション</a></strong></p></td>
<td><p>オブジェクトがトランザクションをサポートしているかどうかを示す値を返します。 読み取り専用の <strong>Boolean</strong> です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-version-property-dao.md">バージョン</a></strong></p></td>
<td><p>Microsoft Access ワークスペースで、データベースを作成した Microsoft Jet または Microsoft Office Access のデータベース エンジンのバージョンを取得します。値の取得のみ可能です。文字列型 (<strong>String</strong>) の値を使用します。</p></td>
</tr>
</tbody>
</table>

