---
title: トランザクション処理
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13f25df31bea1eb742b4a7e7c958ccdbfb7274a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314008"
---
# <a name="transaction-processing"></a>トランザクション処理

**適用先:** Access 2013、Office 2013

ADO では、トランザクションを制御するために、 **BeginTrans** 、 **CommitTrans** 、および **RollbackTrans** の各メソッドを提供しています。 **Connection** オブジェクトでこれらのメソッドを使用すると、ソース データに対する一連の変更を 1 つの単位として、保存または取り消しを行うことができます。たとえば、口座間で振り込みをするには、ある口座からその金額を引き出し、同じ金額を別の口座に入金します。いずれかの更新が失敗すると口座の残高が合わなくなります。開いている 1 つのトランザクション内でこうした変更を行う場合、すべての変更が完了するか、すべての変更が取り消されるかのいずれかになります。

> [!NOTE]
> すべてのプロバイダーがトランザクションをサポートしているわけではありません。プロバイダー定義のプロパティ "**Transaction DDL**" が、**Connection** オブジェクトの [Properties](properties-collection-ado.md) コレクションに含まれることを確認してください。このプロパティは、プロバイダーがトランザクションをサポートすることを示します。プロバイダーがトランザクションをサポートしない場合、いずれかのトランザクション メソッドを呼び出すと、エラーが発生します。

**BeginTrans** メソッドを呼び出すと、 **CommitTrans** または **RollbackTrans** を呼び出してトランザクションを終了するまで、変更が直ちにコミットされなくなります。

**CommitTrans** メソッドを呼び出すと、その接続で開いているトランザクション内で行われた変更が保存され、トランザクションが終了します。 **RollbackTrans** メソッドを呼び出すと、開いているトランザクション内で行われた変更がすべて元に戻され、トランザクションが終了します。開いているトランザクションがないときにこれらのメソッドを呼び出すと、エラーが発生します。

**CommitTrans** メソッドまたは [RollbackTrans](attributes-property-ado.md) メソッドを呼び出すと、 **Connection** オブジェクトの **Attributes** プロパティの値に応じて、新規トランザクションが自動的に開始される場合があります。 **Attributes** プロパティが **adXactCommitRetaining** に設定されている場合、 **CommitTrans** メソッドが呼び出された後に、新規トランザクションが自動的に開始されます。 **Attributes** プロパティが **adXactAbortRetaining** に設定されている場合、 **RollbackTrans** メソッドが呼び出された後に、新規トランザクションが自動的に開始されます。

## <a name="transaction-isolation-level"></a>トランザクション分離レベル

**Connection** オブジェクトでトランザクションの分離レベルを設定するには、 **IsolationLevel** プロパティを使用します。 この設定は、次に [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを呼び出すまで有効になりません。 要求した分離レベルを使用できない場合、プロバイダーはその次に高い分離レベルを返すことがあります。 有効な値の詳細については、「ADO プログラマリファレンス」の**IsolationLevel**プロパティを参照してください。

## <a name="nested-transactions"></a>ネストされたトランザクション

ネストされているトランザクションをサポートしているプロバイダーの場合、開いているトランザクションで **BeginTrans** メソッドを呼び出すと、新規のネストされているトランザクションが開始されます。戻り値は、ネストのレベルを示します。"1" はトップレベルのトランザクション (他のトランザクション内にネストされていないトランザクション) を開いたことを示し、"2" は 2 番目のレベルのトランザクション (トップレベルのトランザクション内にネストされているトランザクション) を開いたことを示し、以降も同様です。 **CommitTrans** または **RollbackTrans** を呼び出すと、最後に開いたトランザクションのみに影響します。上位レベルのトランザクションを解決するには、まず現在のトランザクションを閉じるか、またはロールバックする必要があります。

