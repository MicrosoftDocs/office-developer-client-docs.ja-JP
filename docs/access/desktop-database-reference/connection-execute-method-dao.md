---
title: Connection メソッド (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295913"
---
# <a name="connectionexecute-method-dao"></a>Connection メソッド (DAO)

**適用先:** Access 2013、Office 2013

指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。

## <a name="syntax"></a>構文

*式*。Execute (***クエリ***、***オプション***)

*式***Connection**オブジェクトを表す変数を取得します。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Query</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>SQL ステートメントまたは <strong>QueryDef</strong> オブジェクトの <strong>Name</strong> プロパティの値を示す文字列型 (<strong>String</strong>) の値。</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>[設定] で指定された、クエリのデータ整合性の特性を表す定数 (または定数の組み合わせ)。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

オプションには、次の**[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** 定数を使用できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbdenywrite</strong></p></td>
<td><p>他のユーザーに対して書き込み権限を許可しません (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(既定値) 矛盾した更新を実行します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>一貫性のある更新を実行します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>SQL パススルー クエリを実行します。 このオプションを設定すると、SQL ステートメントが ODBC データベースに渡されて処理されます (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>エラーが発生した場合、更新をロールバックします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>編集中のデータが他のユーザーによって変更されている場合、実行時エラーを生成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>クエリを非同期に実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>SQLPrepare ODBC API 関数を呼び出さずにステートメントを実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。

> [!NOTE]
> [!メモ] 定数 **dbConsistent** と **dbInconsistent** は互いに排他的です。1 つの **OpenRecordset** のインスタンスにおいては、どちらか一方を使用できますが、両方を使用することはできません。 **dbConsistent** と **dbInconsistent** の両方を使用すると、エラーが発生します。

**Execute** メソッドはアクション クエリでのみ有効です。別の種類のクエリで **Execute** を使用すると、エラーが発生します。アクション クエリはレコードを返さないので、 **Execute** は **Recordset** を返しません。 **Recordset** が返されない場合は、ODBCDirect ワークスペースで SQL パススルー クエリを実行してもエラーは返されません。

**Connection** 、 **Database** 、または **QueryDef** のオブジェクトの **RecordsAffected** プロパティを使用して、最後に使用された **Execute** メソッドによって影響を受けたレコードの数を取得できます。たとえば、アクション クエリの実行時に削除、更新、または挿入されたレコードの数が **RecordsAffected** に格納されます。 **Execute** メソッドを使用してクエリを実行すると、 **QueryDef** オブジェクトの **RecordsAffected** プロパティは、影響を受けたレコードの数に設定されます。

Microsoft Access ワークスペースでは、指定した SQL ステートメントの構文が正しく、ユーザーが適切な権限を持っている場合、1 行も変更または削除できなくても、 **Execute** メソッドが失敗することはありません。したがって、 **Execute** メソッドを使って更新または削除のクエリを実行するときは、必ず **dbFailOnError** オプションを指定してください。このオプションを使用すると、影響を受けるレコードの一部がロックされているために更新または削除できない場合、実行時エラーが生成され、既に成功している変更もすべてロールバックされます。

以前のバージョンの Microsoft Jet データベース エンジンでは、暗黙のトランザクション内に自動的に SQL ステートメントが埋め込まれていました。 **dbFailOnError** を指定して実行したステートメントの一部が失敗した場合は、ステートメント全体がロールバックされました。パフォーマンスを向上するために、バージョン 3.5 以降では、この暗黙のトランザクションが取り除かれました。古いバージョンの DAO コードを更新する場合は、 **Execute** ステートメントの前後で明示的なトランザクションを使用することを検討してください。

Microsoft Access ワークスペースでのパフォーマンスを最適にする (特にマルチユーザー環境の場合) には、トランザクション内部に **Execute** メソッドをネストします。現在の **Workspace** オブジェクトの **BeginTrans** メソッドを使用し、次に **Execute** メソッドを使用し、最後に **Workspace** の **CommitTrans** メソッドを使用してトランザクションを完了します。これにより、変更がディスクに保存され、クエリ実行中に適用されていたロックがすべて解除されます。

