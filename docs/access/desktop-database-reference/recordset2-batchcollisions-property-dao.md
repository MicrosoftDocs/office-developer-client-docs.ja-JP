---
title: Recordset2 の競合プロパティ (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307491"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2 の競合プロパティ (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。BatchCollisions

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

このプロパティには、最後に呼び出したバッチ **[Update](recordset2-update-method-dao.md)** メソッドの実行時に競合が発生した行に対するブックマークの配列が格納されます。 **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** プロパティは、この配列の要素の数を示します。

作業中の **Recordset** オブジェクトの **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを **BatchCollisions** 配列のブックマーク値に設定すると、最後のバッチ モード Update 操作で更新を完了できなかった各レコードに移動できます。

競合が発生したレコードを修正した後、もう一度バッチ モード **Update** メソッドを呼び出すことができます。この時点で DAO は再度一括更新を試み、2 回目の更新に失敗したレコードのセットが、もう一度 **BatchCollisions** プロパティに反映されます。前回の処理で更新に成功したレコードは、 **[RecordStatus](recordset2-recordstatus-property-dao.md)** プロパティが dbRecordUnmodified に設定されているため、2 回目の更新の対象から除外されます。この処理は、競合が発生している限り続行するか、または更新を中止して結果セットを閉じるまで続行できます。

この配列は、バッチ モード **Update** メソッドを実行するたびに再作成されます。

