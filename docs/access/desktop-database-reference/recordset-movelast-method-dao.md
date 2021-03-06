---
title: Recordset メソッド (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284533"
---
# <a name="recordsetmovelast-method-dao"></a>Recordset メソッド (DAO)

**適用先:** Access 2013、Office 2013

指定された **Recordset** オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式*。MoveLast (***オプション***)

*式***Recordset**オブジェクトを表す変数を取得します。

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
<td><p><em>Options</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p><strong>MoveLast</strong> への呼び出しを非同期で実行する場合に <strong>dbRunAsync</strong> に設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。

**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合は、 **BOF** プロパティは **True** で、カレント レコードはありません。

**MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。

recordset がテーブルタイプの**recordset**を参照している場合 (Microsoft Access ワークスペースのみ)、移動は現在のインデックスに従います。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

> [!NOTE]
> [!メモ] **MoveLast** メソッドを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset** の末尾までデータを格納して、 **Recordset** に含まれるカレント レコード数を示すことができます。 ただし、このような目的で **MoveLast** を使用すると、アプリケーションのパフォーマンスが低下する場合があります。 **MoveLast** を使用してレコード数を取得するのは、新しく開かれた **Recordset** の正確なレコード数をどうしても取得する必要がある場合だけにしてください。 
> 
> **MoveLast** で **dbRunAsync** 定数を使用すると、メソッドの呼び出しが非同期で実行されます。 **Recordset** の末尾までデータが格納されたことを確認するには **StillExecuting** プロパティを使用し、**MoveLast** メソッドに対する非同期呼び出しの実行を終了するには **Cancel** メソッドを使用します。

**MoveFirst**、**MoveLast**、および **MovePrevious** の各メソッドは、前方スクロール タイプの **Recordset** オブジェクトでは使用できません。

**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、**Move** メソッドを使用します。

