---
title: シンプルなコマンドを作成し、実行する
TOCTitle: Creating and Executing a Simple Command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91355c8b24fcd6e797a6610524076b8850b16f57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476413"
---
# <a name="creating-and-executing-a-simple-command"></a><span data-ttu-id="61738-102">シンプルなコマンドを作成し、実行する</span><span class="sxs-lookup"><span data-stu-id="61738-102">Creating and Executing a Simple Command</span></span>


<span data-ttu-id="61738-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="61738-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="61738-p101">**Command** オブジェクトの一般的な使用方法ではありませんが、次のコードに、 **Command** オブジェクトを使用してデータ ソースに対するコマンドを実行する基本的な方法を示します。この場合、行を返すコマンドなので、コマンドの実行結果を **Recordset** オブジェクトに返します。</span><span class="sxs-lookup"><span data-stu-id="61738-p101">Though not a typical usage of the **Command** object, the following code shows the basic method of using the **Command** object to execute a command against a data source. In this case, it is a row-returning command, so it returns the results of the command execution into a **Recordset** object.</span></span>

```vb 
 
 'BeginBasicCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = 'ALFKI' " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print "ALFKI" 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndBasicCmd 
```

<span data-ttu-id="61738-106">実行するコマンドは、 **CommandText** プロパティで指定します。</span><span class="sxs-lookup"><span data-stu-id="61738-106">The command to be executed is specified with the **CommandText** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="61738-p102">[!メモ] このセクションのいくつかの例では、ユーティリティ関数 GetNewConnection を呼び出して、データ プロバイダーとの接続を確立します。冗長性を避けるため、ここでは 1 回のみ記述されています。</span><span class="sxs-lookup"><span data-stu-id="61738-p102">Several examples in this section call a utility function, GetNewConnection, to establish a connection with the data provider. To avoid redundancy, it is listed only once, here:</span></span></P>



```vb 
 
'BeginNewConnection 
Private Function GetNewConnection() As ADODB.Connection 
 Dim oCn As New ADODB.Connection 
 Dim sCnStr As String 
 
 sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Integrated Security='SSPI';Database='Northwind';" 
 oCn.Open sCnStr 
 
 If oCn.State = adStateOpen Then 
 Set GetNewConnection = oCn 
 End If 
 
End Function 
'EndNewConnection 
```
