---
title: Recordset プロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 7693f89f07413772ea961a61c86e9c5448c4c449
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300666"
---
# <a name="recordsetbatchsize-property-dao"></a><span data-ttu-id="2117f-102">Recordset プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2117f-102">Recordset.BatchSize property (DAO)</span></span>


<span data-ttu-id="2117f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2117f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2117f-104">構文</span><span class="sxs-lookup"><span data-stu-id="2117f-104">Syntax</span></span>

<span data-ttu-id="2117f-105">*式*。BatchSize</span><span class="sxs-lookup"><span data-stu-id="2117f-105">*expression* .BatchSize</span></span>

<span data-ttu-id="2117f-106">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="2117f-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2117f-107">注釈</span><span class="sxs-lookup"><span data-stu-id="2117f-107">Remarks</span></span>

<span data-ttu-id="2117f-p101">**BatchSize** プロパティを使用すると、一括更新でサーバーにステートメントを送信するときに使用するバッチ サイズを指定できます。このプロパティの値によって、1 つのコマンド バッファーでサーバーに送信されるステートメントの数が決まります。既定では、それぞれのバッチで 15 ステートメントがサーバーに送信されます。このプロパティはいつでも変更できます。データベース サーバーがステートメントのバッチ処理をサポートしていない場合、このプロパティを 1 に設定すると、それぞれのステートメントを個別に送信できます。</span><span class="sxs-lookup"><span data-stu-id="2117f-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="2117f-113">例</span><span class="sxs-lookup"><span data-stu-id="2117f-113">Example</span></span>

<span data-ttu-id="2117f-114">この例では、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定した Recordset オブジェクトに対する一括更新の要素を制御します。</span><span class="sxs-lookup"><span data-stu-id="2117f-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

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

