---
title: executeoptionenum (Access デスクトップデータベースリファレンス)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293246"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**適用先:** Access 2013、Office 2013

プロバイダーによるコマンドの実行方法を表します。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0x10</p></td>
<td><p>コマンドを非同期に実行することを示します。 この値は、<a href="commandtypeenum.md">CommandTypeEnum</a> の値 <strong>adCmdTableDirect</strong> と組み合わせて使用できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p><a href="cachesize-property-ado.md">CacheSize</a> プロパティで指定した初期量の残りの行を非同期に取得することを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>取得中にメイン スレッドがブロックしないことを示します。 要求された行がまだ取得されていない場合、現在の行が自動的にファイルの最後に移動します。</p><p>永続的に保存された <strong>Recordset</strong> を持つ <a href="stream-object-ado.md">Stream</a> から <a href="recordset-object-ado.md">Recordset</a> を開いた場合、<strong>adAsyncFetchNonBlocking</strong> は無効になり、操作は同期で実行され、ブロッキングが発生します。 <a href="commandtypeenum.md">adCmdTableDirect</a> オプションを使用して <strong>Recordset</strong> を開いた場合、<strong>adAsynchFetchNonBlocking</strong> は無効になります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>コマンド テキストが、行を返さないコマンドまたはストアド プロシージャ (たとえば、データの挿入のみを行うコマンド) であることを示します。 取得した行があっても削除されるので、コマンドからは返されません。 <strong>adExecuteNoRecords</strong>は、<strong>コマンド</strong>または<strong>Connection</strong>の<strong>Execute</strong>メソッドに、省略可能なパラメーターとしてのみ渡すことができます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>解像度</p></td>
<td><p>コマンドの実行結果がストリームとして返されることを示します。 <strong>adExecuteStream</strong>は、 <strong>Command</strong> <strong>Execute</strong>メソッドにオプションのパラメーターとして渡すことができます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p><strong>CommandText</strong> が、<strong>Record</strong> オブジェクトとして返される単一の行を返すコマンドまたはストアド プロシージャであることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adoptionunspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>コマンドが指定されていないことを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums オプションの asyncexecute</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums のオプション。 asyncfetch</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプション。 asyncfetchnonblocking ブロッキング</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプション。未指定</p></td>
</tr>
</tbody>
</table>

