---
title: RDS オブジェクト モデルの概要
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300876"
---
# <a name="rds-object-model-summary"></a>RDS オブジェクト モデルの概要


**適用先:** Access 2013、Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Object</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">章.スペース</a></p></td>
<td><p>このオブジェクトには、サーバー プロキシを取得するためのメソッドが含まれます。プロキシは、既定のサーバー プログラムの場合と、カスタム サーバー プログラム (ビジネス オブジェクト) の場合があります。サーバー プログラムは、インターネット、イントラネット、またはローカル エリア ネットワークを介して呼び出すこと、またはローカルなダイナミック リンク ライブラリとすることができます。</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">rdsserver.datafactory DataFactory</a></p></td>
<td><p>このオブジェクトは、既定のサーバー プログラムを表します。 RDS データの既定の取得動作および更新動作を実行します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">章.DataControl</a></p></td>
<td><p>このオブジェクトは、<strong>RDS.DataSpace</strong> オブジェクトおよび <strong>RDSServer.DataFactory</strong> オブジェクトを、自動的に呼び出すことができます。 既定の RDS データ取得動作または更新動作を呼び出すには、このオブジェクトを使用します。 また、このオブジェクトは、返された <strong>Recordset</strong> オブジェクトにアクセスするビジュアル コントロールを提供します。</p></td>
</tr>
</tbody>
</table>

