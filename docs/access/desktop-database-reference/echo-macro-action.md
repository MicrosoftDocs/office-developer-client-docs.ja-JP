---
title: Echo マクロアクション (Access デスクトップデータベースリファレンス)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293624"
---
# <a name="echo-macro-action"></a>Echo マクロ アクション

**適用先:** Access 2013、Office 2013

**Echo** アクションを使用すると、エコーが有効かどうかを指定できます。たとえば、このアクションを使用して、マクロの実行中にその結果を表示または非表示にすることができます。

## <a name="setting"></a>Setting

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。

**Echo** アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo On/エコーの設定</strong></p></td>
<td><p>[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>エコーの設定</strong>] ボックスで、[ <strong>はい</strong>] (エコーをオンにする) または [ <strong>いいえ</strong>] (エコーをオフにする) をクリックします。既定値は [ <strong>はい</strong>] です。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Status Bar Text/ステータス バー テキスト</strong></p></td>
<td><p>エコーがオフのときにステータス バーに表示されるテキストです。 たとえば、エコーがオフになっている場合は、マクロが&quot;実行中であることをステータスバーに表示できます。&quot;</p></td>
</tr>
</tbody>
</table>


マクロを実行すると、通常、マクロの機能に不要な情報が画面更新に表示されます。 **Echo On/エコーの設定** 引数を [ **いいえ** ] に設定すると、画面を更新せずにマクロが実行されます。 マクロが完了すると、エコーが自動的にオンになり、ウィンドウが再描画されます。 **Echo On/エコーの設定** 引数を [ **いいえ** ] に設定しても、マクロの機能またはその結果には影響しません。

**Echo** アクションでは、エラー メッセージなどの作業ウィンドウ固定 (モーダル) ダイアログ ボックス、またはプロパティ シートなどのポップアップ フォームの表示は抑制されません。エコーがオフの場合でも、ダイアログ ボックスおよびポップアップフォームを使用して、情報を収集または表示することができます。すべてのメッセージまたはダイアログ ボックス (ユーザーが情報を入力する必要があるエラー メッセージ ボックスおよびダイアログ ボックスを除く) が表示されないようにするには、 **SetWarnings** アクションを使用します。

**Echo** アクションは、マクロで複数回実行できます。これにより、マクロの実行中にステータス バーのテキストを変更することができます。

エコーをオフにすると、 **DisplayHourglassPointer** アクションを使用して、マクロ ポインターを砂時計のアイコン (または "待ち状態" に対して設定したマウス ポインターのアイコン) に変更し、マクロが実行中であることを視覚的に示すことができます。

Visual Basic for Applications (VBA) モジュールで **Echo** アクションを実行するには、**DoCmd** オブジェクトの **Echo** メソッドを使用します。

## <a name="examples"></a>例

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>マクロによるコントロールの値の設定

次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、**Echo**、**CloseWindow**、**OpenForm**、**SetValue**、および **GoToControl** の各アクションの使い方を示します。**SetValue** アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、**GoToControl** アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクション</p></th>
<th><p>引数: 設定値</p></th>
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></p></td>
<td><p>画面の更新は停止しますが、マクロは実行されています。</p></td>
</tr>
<tr class="even">
<td><p><strong>CloseWindow</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>formobject 名前</strong>: 製品リストの<strong>保存</strong>:<strong>いいえ</strong></p></td>
<td><p>[製品リスト] フォームを閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: Products<strong>ビュー</strong>: <strong>formdata mode</strong>: <strong>addwindow mode</strong>: <strong>Normal</strong></p></td>
<td><p>[製品] フォームを開きます。</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</p></td>
<td><p>[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name/コントロール名</strong>: CategoryID</p></td>
<td><p>[カテゴリ ID] コントロールに移動します。</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>マクロによるフォームの同期

次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、**Echo**、**MessageBox**、**GoToControl**、**StopMacro**、**OpenForm**、および **MoveAndSizeWindow** の各アクションの使い方を示します。また、**MessageBox**、**GoToControl**、**StopMacro** の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品のレビュー] ボタンに割り当てる必要があります。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>条件</p></th>
<th><p>アクション</p></th>
<th><p>引数: 設定値</p></th>
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></p></td>
<td><p>画面の更新は停止しますが、マクロは実行されています。</p></td>
</tr>
<tr class="even">
<td><p>IsNull([仕入先コード])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。 <strong>Beep</strong>: <strong>yestype</strong>: <strong>none title</strong>: 仕入先の選択</p></td>
<td><p>[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name/コントロール名</strong>: 会社名</p></td>
<td><p>フォーカスを [仕入先名] コントロールに移動します。</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>マクロを停止します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: 製品リスト<strong>ビュー</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![仕入先]!SupplierID<strong>データモード</strong>:<strong>読み取りのみウィンドウモード</strong>:<strong>標準</strong></p></td>
<td><p>[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</p></td>
<td><p>[製品リスト] を [仕入先] フォームの右下に配置します。</p></td>
</tr>
</tbody>
</table>

