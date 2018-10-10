---
title: '5 章: データを更新し、保存する'
TOCTitle: 'Chapter 5: Updating and Persisting Data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91c747c970988a9ca853f0be66f5c0b485f5c3f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476502"
---
# <a name="chapter-5-updating-and-persisting-data"></a><span data-ttu-id="2623b-102">5 章: データを更新し、保存する</span><span class="sxs-lookup"><span data-stu-id="2623b-102">Chapter 5: Updating and Persisting Data</span></span>


<span data-ttu-id="2623b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2623b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2623b-p101">これまでの章では、ADO を使用してデータ ソース内のデータにアクセスする方法、データ内を移動する方法、およびデータを編集する方法について説明しました。ユーザーがデータを変更できるようにするアプリケーションを構築する場合、これらの変更を保存する方法を理解しておく必要があります。 **Save** メソッドを使用して **Recordset** の変更をファイルに保存することも、 **Update** メソッドまたは **UpdateBatch** メソッドを使用して、変更内容をデータ ソースに返送して保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="2623b-p101">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data. Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes. You can either persist the **Recordset** changes to a file using the **Save** method, or you can send the changes back to the data source for storage using the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="2623b-p102">これまでの章では、 **Recordset** の複数の行で変更を行いました。ADO では、データ行の追加、削除、および変更に関連する 2 つの基本的な概念をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2623b-p102">In the preceding chapters, you changed the data in several rows of the **Recordset**. ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</span></span>

<span data-ttu-id="2623b-109">最初の概念はすぐに変更する**レコード セット**です。代わりに、内部*バッファーのコピー*に加えられました。</span><span class="sxs-lookup"><span data-stu-id="2623b-109">The first notion is that changes aren't immediately made to the **Recordset**; instead, they are made to an internal *copy buffer*.</span></span> <span data-ttu-id="2623b-110">変更したくない場合は、コピー バッファー内の変更は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="2623b-110">If you decide you don't want the changes, the modifications in the copy buffer are discarded.</span></span> <span data-ttu-id="2623b-111">変更を維持することにした場合は、コピー バッファー内の変更が**レコード セット**に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2623b-111">If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.</span></span>

<span data-ttu-id="2623b-112">変更は、行を完全な (つまり、*イミディ エイト*モード) の操作を宣言するか (つまり完全な一連の作業時間を宣言するまでの行のセットに対するすべての変更を収集すると、すぐにデータ ソースに反映かの 2 つ目の概念は、します。、*バッチ*モード)。</span><span class="sxs-lookup"><span data-stu-id="2623b-112">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, *immediate* mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, *batch* mode).</span></span> <span data-ttu-id="2623b-113">**LockType**プロパティは、基になるデータ ソースへの変更があったときを決定します。</span><span class="sxs-lookup"><span data-stu-id="2623b-113">The **LockType** property determines when the changes are made to the underlying data source.</span></span> <span data-ttu-id="2623b-114">**adLockOptimistic**または**adLockPessimistic**は、 **adLockBatchOptimistic**はバッチ モードを指定するときにイミディ エイト モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="2623b-114">**adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode.</span></span> <span data-ttu-id="2623b-115">**LockType**設定が使用可能な**CursorLocation**プロパティに影響します。</span><span class="sxs-lookup"><span data-stu-id="2623b-115">The **CursorLocation** property can affect which **LockType** settings are available.</span></span> <span data-ttu-id="2623b-116">**CursorLocation**プロパティが**adUseClient**に設定されて場合、 **adLockPessimistic**設定はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="2623b-116">For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.</span></span>

<span data-ttu-id="2623b-p105">即時モードでは、 **Update** メソッドを呼び出すたびに、変更がデータ ソースに反映されます。バッチ モードでは、 **Update** を呼び出すか、現在の行の位置が移動されるたびに、変更内容がコピー バッファーに保存されますが、データ ソースに変更を反映するのは **UpdateBatch** メソッドのみです。</span><span class="sxs-lookup"><span data-stu-id="2623b-p105">In immediate mode, each invocation of the **Update** method propagates the changes to the data source. In batch mode, each invocation of **Update** or movement of the current row position saves the changes to the copy buffer, but only the **UpdateBatch** method propagates the changes to the data source.</span></span>
