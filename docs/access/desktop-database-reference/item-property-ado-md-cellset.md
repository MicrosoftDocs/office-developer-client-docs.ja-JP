---
title: Item プロパティ (ADO MD Cellset)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99f381ad2f38dc7d2c467ed1e40e4084032006d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290868"
---
# <a name="item-property-ado-md-cellset"></a>Item プロパティ (ADO MD Cellset)

**適用先:** Access 2013、Office 2013

座標を使用して、セルセットからセルを取得します。

## <a name="syntax"></a>構文

*セルのセル* = ** セットを設定します。アイテム (*位置*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Positions* |セルを一意に指定する値の**バリアント型 (Variant** ) の配列です。 *Positions* は次のいずれかです。<br/><br/>-位置番号の配列<br/>-メンバ名の配列<br/>-序数の位置 |

## <a name="remarks"></a>注釈

**Item** プロパティを使用して、[Cellset](cellset-object-ado-md.md) オブジェクト内の [Cell](cell-object-ado-md.md) オブジェクトを返します。**Item** プロパティによって、引数 *Positions* に対応するセルが見つからない場合は、エラーが発生します。

**Item** プロパティは **Cellset** オブジェクトの既定プロパティです。 次のいずれの構文形式でも同じ結果が得られます。

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

引数 *Positions* には、返すセルを指定します。セルは、位置を表す序数または各軸に沿った位置によって指定できます。各軸に沿った位置によってセルを指定する場合は、位置の数値またはメンバーの名前を指定できます。

位置を表す序数は、**Cellset** 内のセルを一意に識別する数です。概念的には、**Cellset** 内のセルは **Cellset** が *p* 次元の配列であるかのように番号が付けられます。ここで、*p* は軸の数です。セルは行優先でアドレス指定されます。

**Item** にメンバー名を文字列として渡す場合、メンバーの軸の数値識別子は昇順で記載する必要があります。軸内では、次元のネストの昇順で記載する必要があります。つまり、最も外側の次元のメンバーを最初に記載し、その後に内側の次元のメンバーを記載します。各次元は個別の文字列で表し、メンバーの文字列の一覧はコンマで区切る必要があります。


> [!NOTE]
> [!メモ] データ プロバイダーによっては、メンバー名によるセルの取得がサポートされていない場合があります。詳細については、各自のプロバイダーのドキュメントを参照してください。


