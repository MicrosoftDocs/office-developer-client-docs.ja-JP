---
title: OnError マクロ アクション
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288456"
---
# <a name="onerror-macro-action"></a>OnError マクロ アクション

**適用先:** Access 2013、Office 2013

**OnError** アクションを使用すると、マクロでエラーが発生したときに行われる処理を指定できます。

## <a name="setting"></a>Setting

**OnError** アクションの引数は次のとおりです。


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
<td><p>Go to </p></td>
<td><p>エラーが発生した場合の一般的な動作を指定します。ドロップダウン ボックスの矢印をクリックし、次の設定値のいずれかをクリックします。</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>設定</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Next/次のレコード</strong></p></td>
<td><p>Microsoft Office Access 2007 では、エラーの詳細が <strong>MacroError</strong> オブジェクトに記録されますが、マクロの実行は停止されません。マクロは次のアクションを続行します。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Macro Name/マクロ名</strong></p></td>
<td><p>実行中のマクロが停止され、 <strong>Macro Name/マクロ名</strong> 引数で指定されているマクロが実行されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Fail/失敗</strong></p></td>
<td><p>実行中のマクロが停止され、エラー メッセージが表示されます。</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>マクロ名</p></td>
<td><p>引数 Go が [マクロ名] に設定されている場合は、エラー処理に使用するマクロの名前を入力します。 The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object. In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action. Go to 引数を [<strong>次へ</strong>] または [<strong>失敗</strong>] に設定した場合、この引数は空白にしておく必要があります。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- **OnError** アクションは、通常はマクロの先頭に配置されますが、先頭以降に配置することもできます。このアクションによって設定されるルールは、アクションを実行するたびに適用されます。

- 引数 Go to 引数を**Fail**に設定すると、マクロに " **OnError/エラー**時" アクションがない場合と同じように動作します。 つまり、エラーが発生した場合は、マクロの実行が停止され、標準的なエラー メッセージが表示されます。 [ **失敗** ] 設定値の主な用途は、マクロ内でそれ以前に設定したエラー処理を無効にすることです。

## <a name="example"></a>例

次のマクロは、"OnError/**エラー**時" アクションの使用方法を示します。 この例では、" **OnError** /エラー時" アクションは、エラーが発生したときに ErrorHandler という名前のカスタムエラー処理マクロを実行するように指定します。 エラーが発生すると、CatchErrors submacro が呼び出されます。 エラー番号が2102の場合は、特定のメッセージが表示され、マクロの実行が停止します。 それ以外の場合は、エラーを説明するメッセージが表示され、マクロが一時停止して、追加のトラブルシューティングを実行できるようになります。 ErrorHandler マクロは、 **MacroError**オブジェクトを参照するメッセージボックスを表示して、エラーに関する情報を表示します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
