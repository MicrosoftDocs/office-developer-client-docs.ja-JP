---
title: SetField マクロ アクション
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314617"
---
# <a name="setfield-macro-action"></a>SetField マクロ アクション

**適用先:** Access 2013、Office 2013

The **SetField** action can be used to assign a value to a field.

> [!NOTE]
> "**SetField**/フィールドの設定" アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>Setting

"SetField/フィールドの設定" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>名前</strong></p></td>
<td><p>フィールドを識別する文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong>値</strong></p></td>
<td><p>フィールドに割り当てる値を指定する式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.

