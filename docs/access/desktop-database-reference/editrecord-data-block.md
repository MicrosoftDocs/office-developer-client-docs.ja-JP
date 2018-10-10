---
title: EditRecord データ ブロック
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07763e32e0f8687816dc39298f91733ca814d275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476241"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="d0865-102">EditRecord データ ブロック</span><span class="sxs-lookup"><span data-stu-id="d0865-102">EditRecord Data Block</span></span>

<span data-ttu-id="d0865-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0865-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d0865-104">**EditRecord** データ ブロックを使用して、既存のレコード内の値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d0865-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="d0865-105">[!メモ] **EditRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0865-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="d0865-106">設定</span><span class="sxs-lookup"><span data-stu-id="d0865-106">Setting</span></span>

<span data-ttu-id="d0865-107">**EditRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d0865-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0865-108">引数</span><span class="sxs-lookup"><span data-stu-id="d0865-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="d0865-109">説明</span><span class="sxs-lookup"><span data-stu-id="d0865-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0865-110"><strong>エイリアス</strong></span><span class="sxs-lookup"><span data-stu-id="d0865-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="d0865-111">編集するレコードを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="d0865-111">A string that identifies the record to edit.</span></span> <span data-ttu-id="d0865-112"><em>別名</em>引数を指定しない場合、現在のレコードを編集します。</span><span class="sxs-lookup"><span data-stu-id="d0865-112">If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="d0865-113">備考</span><span class="sxs-lookup"><span data-stu-id="d0865-113">Remarks</span></span>

<span data-ttu-id="d0865-114">**EditRecord**ステートメントの後に、レコードに対する変更は、コミットされていない前に実行するコマンドのブロックを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="d0865-114">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted.</span></span> <span data-ttu-id="d0865-115">**EditRecord**データ ブロックに次の操作を利用できます。</span><span class="sxs-lookup"><span data-stu-id="d0865-115">The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0865-116"><a href="cancelrecordchange-macro-action.md">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="d0865-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0865-117"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="d0865-117"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0865-118"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="d0865-118"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0865-119"><a href="if-then-else-macro-block.md">もし。。。そうしたら。。。マクロ ステートメントはその他</a></span><span class="sxs-lookup"><span data-stu-id="d0865-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0865-120"><a href="setfield-macro-action.md">"SetField/フィールドの設定" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="d0865-120"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0865-121"><a href="setlocalvar-macro-action.md">"SetLocalVar/ローカル変数の設定" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="d0865-121"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d0865-122">" **SetField** /フィールドの設定" アクションを使用して、編集するレコードの新しいフィールド値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0865-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="d0865-123">場合、**を使用することができます.そうしたら。。。他**の条件に基づいて、ステートメントを使用して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="d0865-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="d0865-p103">レコードの編集を取り消すには、" **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **EditRecord** データ ブロックが終了します。</span><span class="sxs-lookup"><span data-stu-id="d0865-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="d0865-p104">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="d0865-p104">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="d0865-128">CreateRecord データ ブロックは、**[後に挿入](after-insert-macro-event.md)**、**[更新した後](after-update-macro-event.md)**、および**[更新後](after-update-macro-event.md)** のデータ マクロのイベントでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0865-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>
