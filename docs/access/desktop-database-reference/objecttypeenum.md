---
title: objecttypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288533"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**適用先:** Access 2013、Office 2013

権限または所有権を設定するデータベース オブジェクトの種類を示します。

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
<td><p><strong>adpermobjcolumn</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>オブジェクトは列です。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpermobjdatabase</strong></p></td>
<td><p>1/3</p></td>
<td><p>オブジェクトはデータベースです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adpermobjprocedure</strong></p></td>
<td><p>2/4</p></td>
<td><p>オブジェクトはプロシージャです。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpermobjproviderspecific</strong></p></td>
<td><p>-1</p></td>
<td><p>オブジェクトの種類は、プロバイダー によって定義されます。<em>ObjectType</em> パラメーターが <strong>adPermObjProviderSpecific</strong> で、<em>ObjectTypeId</em> が指定されていない場合、エラーが発生します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adpermobjtable</strong></p></td>
<td><p>1-d</p></td>
<td><p>オブジェクトはテーブルです。</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjView</strong></p></td>
<td><p>5</p></td>
<td><p>オブジェクトはビューです。</p></td>
</tr>
</tbody>
</table>

