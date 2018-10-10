---
title: '手順 3: サーバーからレコードセットを取得する (RDS チュートリアル)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8509c7869613a92acf0d61e4fb1ebc5be411c0a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478350"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a><span data-ttu-id="eddc5-102">手順 3: サーバーからレコードセットを取得する (RDS チュートリアル)</span><span class="sxs-lookup"><span data-stu-id="eddc5-102">Step 3: Server Obtains a Recordset (RDS Tutorial)</span></span>


<span data-ttu-id="eddc5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="eddc5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eddc5-p101">サーバー プログラムは、目的の行のデータ ソースのクエリを実行するために、接続文字列とコマンド テキストを使用します。通常、この **Recordset** の取得には ADO が使用されますが、マイクロソフトのその他のデータ アクセス インターフェイス (OLE DB など) を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="eddc5-p101">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="eddc5-106">カスタマー サーバー プログラムは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="eddc5-106">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```
