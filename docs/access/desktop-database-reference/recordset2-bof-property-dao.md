---
title: Recordset2 プロパティ (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5ffe9c679da3f11666799caa070f51f384729cc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307463"
---
# <a name="recordset2bof-property-dao"></a>Recordset2 プロパティ (DAO)


**適用先:** Access 2013、Office 2013

カレントレコードの位置が**Recordset**オブジェクトの最初のレコードより前にあるかどうかを示す値を返します。 値の取得のみ可能なブール型 (**Boolean**) の値です。

## <a name="syntax"></a>構文

*式*。bof プロパティ

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**BOF** プロパティおよび **EOF** プロパティを使用すると、**Recordset** オブジェクトにレコードが格納されているかどうかの確認、またはレコード間を移動したときに **Recordset** オブジェクトの範囲を超えたかどうかの確認ができます。

カレント レコードを参照するポインターの位置により、 **BOF** および **EOF** の戻り値が決まります。

**BOF** プロパティと **EOF** プロパティのいずれかが **True** になっている場合は、カレント レコードが存在しません。

レコードが 1 つも格納されていない **Recordset** オブジェクトを開くと、 **BOF** プロパティおよび **EOF** プロパティが **True** に設定され、 **Recordset** オブジェクトの **RecordCount** は 0 に設定されます。1 つ以上のレコードが格納されている **Recordset** オブジェクトを開くと、先頭のレコードがカレント レコードになり、 **BOF** プロパティと **EOF** プロパティが **False** に設定されます。 **MovePrevious** メソッドまたは **MoveNext** メソッドを使用して、それぞれ **Recordset** オブジェクトの先頭または末尾を越えた位置に移動するまで、これらのプロパティは **False** のまま変わりません。レコードセットの先頭または末尾を越えた位置に移動すると、カレント レコードがなくなり、レコードが存在しない状態になります。

**Recordset** オブジェクトに残っている最後の 1 つのレコードを削除した場合は、カレント レコードの位置を変更しようとするまでは **BOF** プロパティと **EOF** プロパティが **False** のまま変わらないこともあります。

レコードを含む **Recordset** オブジェクトで **MoveLast** メソッドを使用すると、最後のレコードがカレント レコードになり、その後 **MoveNext** メソッドを使用すると、カレント レコードが無効になり、 **EOF** プロパティが **True** に設定されます。一方、レコードを含む **Recordset** オブジェクトで **MoveFirst** メソッドを使用すると、最初のレコードがカレント レコードになり、その後 **MovePrevious** メソッドを使用すると、カレント レコードがなく、 **BOF** プロパティが **True** に設定されます。

通常、 **Recordset** オブジェクトのすべてのレコードを操作する場合は、 **EOF** プロパティが **True** に設定されるまで **MoveNext** メソッドを使用してレコード内をループするコードを記述します。

**EOF** プロパティが **True** に設定されている場合に **MoveNext** メソッドを使用するか、または **BOF** プロパティが **True** に設定されている場合に **MovePrevious** メソッドを使用すると、エラーが発生します。

次の表は、 **BOF** プロパティおよび **EOF** プロパティのさまざまな組み合わせで使用できる Move メソッドの種類を示します。

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst<br />
MoveLast</p></th>
<th><p>MovePrevious<br />
移動&lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext<br />
移動&gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = True、</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>可</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>可</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False、</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
</tr>
<tr class="odd">
<td><p>両方とも <strong>True</strong></p></td>
<td><p>エラー</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>エラー</p></td>
</tr>
<tr class="even">
<td><p>両方とも <strong>False</strong></p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>可</p></td>
<td><p>可</p></td>
</tr>
</tbody>
</table>


Move メソッドが使用可となっていても、そのメソッドがレコードを正常に配置できるとは限りません。指定された Move メソッドを実行しようとすることが許可されていて、エラーが発生しないことを意味しているだけです。 **BOF** プロパティおよび **EOF** プロパティの状態は、試みた Move メソッドの結果によって変わる可能性があります。

**OpenRecordset** メソッドは、 **MoveFirst** メソッドを内部的に呼び出します。したがって、空のレコードのセットに対して **OpenRecordset** メソッドを使用すると、 **BOF** プロパティおよび **EOF** プロパティが **True** に設定されます (失敗した **MoveFirst** メソッドの動作については、次の表を参照)。

Move メソッドを使用してレコードが正常に配置される場合は常に、 **BOF** プロパティと **EOF** プロパティの両方が **False** に設定されます。

Microsoft Access ワークスペースでは、空のレコードセットにレコードを追加すると、 **BOF** プロパティが **False** になりますが、 **EOF** プロパティは **True** のまま変わらず、カレント レコードの位置がレコードセットの末尾にあることを示します。

いずれかの **Delete** メソッドを使用して、レコードセットに 1 つのみ残っているレコードを削除しても、 **BOF** プロパティおよび **EOF** プロパティの設定は変更されません。

次の表は、Move メソッドでレコードが配置されなかった場合に、 **BOF** プロパティおよび **EOF** プロパティがどのように設定されるかを示しています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>、 <strong>MoveLast</strong></p></td>
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>変化なし</p></td>
<td><p>変化なし</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>変化なし</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>、 <strong>Move</strong> &gt; 0</p></td>
<td><p>変化なし</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

