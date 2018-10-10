---
title: Recordset.BatchSize プロパティ (DAO)
TOCTitle: BatchSize Property
ms:assetid: f03dc505-682f-4b60-62f2-1bd088d873c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836544(v=office.15)
ms:contentKeyID: 48548599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d67c87be0a3ffb7bc9d7b349746e397bb19a9c63
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478878"
---
# <a name="recordsetbatchsize-property-dao"></a><span data-ttu-id="68fa9-102">Recordset.BatchSize プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="68fa9-102">Recordset.BatchSize Property (DAO)</span></span>


<span data-ttu-id="68fa9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="68fa9-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="68fa9-104">構文</span><span class="sxs-lookup"><span data-stu-id="68fa9-104">Syntax</span></span>

<span data-ttu-id="68fa9-105">*式*です。BatchSize</span><span class="sxs-lookup"><span data-stu-id="68fa9-105">*expression* .BatchSize</span></span>

<span data-ttu-id="68fa9-106">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="68fa9-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="68fa9-107">注釈</span><span class="sxs-lookup"><span data-stu-id="68fa9-107">Remarks</span></span>

<span data-ttu-id="68fa9-p101">**BatchSize** プロパティは、バッチ更新でステートメントをサーバーに送信するときに使用されるバッチ サイズを決定します。このプロパティの値は、1 つのコマンド バッファーでサーバーに送信されるステートメントの数を決定します。既定では、各バッチで 15 個のステートメントがサーバーに送信されます。このプロパティはいつでも変更できます。データベース サーバーがステートメントのバッチ処理をサポートしていない場合、このプロパティを 1 に設定すると、各ステートメントが個別に送信されます。</span><span class="sxs-lookup"><span data-stu-id="68fa9-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="68fa9-113">例</span><span class="sxs-lookup"><span data-stu-id="68fa9-113">Example</span></span>

<span data-ttu-id="68fa9-114">次の使用例は、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定した Recordset オブジェクトの任意のバッチ更新の環境を制御します。</span><span class="sxs-lookup"><span data-stu-id="68fa9-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```
