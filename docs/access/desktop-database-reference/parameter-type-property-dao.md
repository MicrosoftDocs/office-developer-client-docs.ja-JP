---
title: パラメーター Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288022"
---
# <a name="parametertype-property-dao"></a>パラメーター Type プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 (**Integer**) の値を使用します。

## <a name="syntax"></a>構文

*式*。種類

*式***Parameter**オブジェクトを表す変数を指定します。

## <a name="remarks"></a>注釈

設定値または戻り値は、操作の種類またはデータ型を示す定数です。Microsoft Access ワークスペース内の **[Parameter](parameter-object-dao.md)** オブジェクトでは、このプロパティは値の取得のみ可能です。

次の表は、 **Parameter** オブジェクトで使用可能な設定値および戻り値を示しています。

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
<td><p><strong>dbbigint</strong></p></td>
<td><p>多倍長整数型 (Big Integer)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbbinary</strong></p></td>
<td><p>バイナリ型 (Binary)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbboolean</strong></p></td>
<td><p>ブール型 (Boolean)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbbyte</strong></p></td>
<td><p>バイト型 (Byte)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbChar</strong></p></td>
<td><p>文字型 (Char)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbcurrency</strong></p></td>
<td><p>通貨型 (Currency)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbdate</strong></p></td>
<td><p>日付/時刻型 (Date/Time)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbdecimal</strong></p></td>
<td><p>10 進型 (Decimal)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbdouble</strong></p></td>
<td><p>倍精度浮動小数点型 (Double)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbfloat</strong></p></td>
<td><p>浮動小数点型 (Float)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbguid</strong></p></td>
<td><p>GUID 型 (GUID)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInteger</strong></p></td>
<td><p>整数型 (Integer)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblong</strong></p></td>
<td><p>Long 型 (Long)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLongBinary</strong></p></td>
<td><p>ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbmemo</strong></p></td>
<td><p>メモ型 (Memo)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbnumeric</strong></p></td>
<td><p>数値型 (Numeric)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsingle</strong></p></td>
<td><p>単精度浮動小数点型 (Single)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbtext</strong></p></td>
<td><p>テキスト型 (Text)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbTime</strong></p></td>
<td><p>時刻型 (Time)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbtimestamp</strong></p></td>
<td><p>タイムスタンプ型 (TimeStamp)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbvarbinary</strong></p></td>
<td><p>VarBinary</p></td>
</tr>
</tbody>
</table>


新しい **Field** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。

