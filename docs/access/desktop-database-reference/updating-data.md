---
title: データを更新する (Access デスクトップデータベースリファレンス)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313567"
---
# <a name="updating-data"></a>データの更新


**適用先:** Access 2013、Office 2013

更新動作および更新機能は、更新モード (ロックの種類)、カーソルの種類、およびカーソル位置に大きく依存します。

**AddNew** メソッドを呼び出した後、または既存のレコードのフィールドを変更した後に行われた **Recordset** オブジェクトの現在のレコードへの変更内容を保存するには、 **Update** メソッドを使用します。 **Recordset** オブジェクトは、更新をサポートしている必要があります。

**Recordset** オブジェクトがバッチ更新をサポートしている場合、 **UpdateBatch** メソッドを呼び出すまで、1 つ以上のレコードに対する複数の変更をローカルにキャッシュできます。現在のレコードの編集中、または新規レコードの追加中に **UpdateBatch** メソッドを呼び出すと、変更を一括してプロバイダーに送信する前に、 **Update** メソッドが自動的に呼び出され、現在のレコードの保留中の変更がすべて保存されます。

**Update** メソッドまたは **UpdateBatch** メソッドを呼び出した後も、現在のレコードは変わりません。

このセクションでは、以下のトピックについて説明します。

- [イミディエイト モード](immediate-mode.md)
- [トランザクション処理](transaction-processing.md)
- [バッチモード (ADO)](batch-mode.md)

