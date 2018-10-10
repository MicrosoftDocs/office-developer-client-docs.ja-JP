---
title: トランザクション処理
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a598b2842638b0c58e72ef2b802c8214f5c72b8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477445"
---
# <a name="transaction-processing"></a><span data-ttu-id="9ea13-102">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="9ea13-102">Transaction Processing</span></span>


<span data-ttu-id="9ea13-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ea13-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9ea13-p101">ADO では、トランザクションを制御するために、 **BeginTrans** 、 **CommitTrans** 、および **RollbackTrans** の各メソッドを提供しています。 **Connection** オブジェクトでこれらのメソッドを使用すると、ソース データに対する一連の変更を 1 つの単位として、保存または取り消しを行うことができます。たとえば、口座間で振り込みをするには、ある口座からその金額を引き出し、同じ金額を別の口座に入金します。いずれかの更新が失敗すると口座の残高が合わなくなります。開いている 1 つのトランザクション内でこうした変更を行う場合、すべての変更が完了するか、すべての変更が取り消されるかのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="9ea13-p101">ADO provides the following methods for controlling transactions: **BeginTrans**, **CommitTrans**, and **RollbackTrans**. Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9ea13-p102">すべてのプロバイダーがトランザクションをサポートしているわけではありません。プロバイダー定義のプロパティ "<STRONG>Transaction DDL</STRONG>" が、<STRONG>Connection</STRONG> オブジェクトの <A href="properties-collection-ado.md">Properties</A> コレクションに含まれることを確認してください。このプロパティは、プロバイダーがトランザクションをサポートすることを示します。プロバイダーがトランザクションをサポートしない場合、いずれかのトランザクション メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9ea13-p102">Not all providers support transactions. Verify that the provider-defined property "<STRONG>Transaction DDL</STRONG>" appears in the <STRONG>Connection</STRONG> object's <A href="properties-collection-ado.md">Properties</A> collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span></P>



<span data-ttu-id="9ea13-112">**BeginTrans** メソッドを呼び出すと、 **CommitTrans** または **RollbackTrans** を呼び出してトランザクションを終了するまで、変更が直ちにコミットされなくなります。</span><span class="sxs-lookup"><span data-stu-id="9ea13-112">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="9ea13-p103">**CommitTrans** メソッドを呼び出すと、その接続で開いているトランザクション内で行われた変更が保存され、トランザクションが終了します。 **RollbackTrans** メソッドを呼び出すと、開いているトランザクション内で行われた変更がすべて元に戻され、トランザクションが終了します。開いているトランザクションがないときにこれらのメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9ea13-p103">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="9ea13-p104">**CommitTrans** メソッドまたは [RollbackTrans](attributes-property-ado.md) メソッドを呼び出すと、 **Connection** オブジェクトの **Attributes** プロパティの値に応じて、新規トランザクションが自動的に開始される場合があります。 **Attributes** プロパティが **adXactCommitRetaining** に設定されている場合、 **CommitTrans** メソッドが呼び出された後に、新規トランザクションが自動的に開始されます。 **Attributes** プロパティが **adXactAbortRetaining** に設定されている場合、 **RollbackTrans** メソッドが呼び出された後に、新規トランザクションが自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="9ea13-p104">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** method may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

## <a name="transaction-isolation-level"></a><span data-ttu-id="9ea13-119">トランザクション分離レベル</span><span class="sxs-lookup"><span data-stu-id="9ea13-119">Transaction Isolation Level</span></span>

<span data-ttu-id="9ea13-p105">**Connection** オブジェクトでトランザクションの分離レベルを設定するには、 **IsolationLevel** プロパティを使用します。この設定は、次に [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを呼び出すまで有効になりません。要求した分離レベルを使用できない場合、プロバイダーはその次に高い分離レベルを返すことがあります。有効な値の詳細については、「ADO プログラマ リファレンス」の **IsolationLevel** プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ea13-p105">Use the **IsolationLevel** property to set the isolation level of a transaction on a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation. Refer to the **IsolationLevel** property in the ADO Programmer's Reference for more details on valid values.</span></span>

## <a name="nested-transactions"></a><span data-ttu-id="9ea13-124">ネストされているトランザクション</span><span class="sxs-lookup"><span data-stu-id="9ea13-124">Nested Transactions</span></span>

<span data-ttu-id="9ea13-p106">ネストされているトランザクションをサポートしているプロバイダーの場合、開いているトランザクションで **BeginTrans** メソッドを呼び出すと、新規のネストされているトランザクションが開始されます。戻り値は、ネストのレベルを示します。"1" はトップレベルのトランザクション (他のトランザクション内にネストされていないトランザクション) を開いたことを示し、"2" は 2 番目のレベルのトランザクション (トップレベルのトランザクション内にネストされているトランザクション) を開いたことを示し、以降も同様です。 **CommitTrans** または **RollbackTrans** を呼び出すと、最後に開いたトランザクションのみに影響します。上位レベルのトランザクションを解決するには、まず現在のトランザクションを閉じるか、またはロールバックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea13-p106">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>
