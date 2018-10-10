---
title: '手順 4: データを受信し、表示する'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2a447b68b8c0eeb18d18050ba8dbbb6f09786ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478905"
---
# <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="95bc1-102">手順 4: データを受信し、表示する</span><span class="sxs-lookup"><span data-stu-id="95bc1-102">Step 4: Receive and Display the Data</span></span>


<span data-ttu-id="95bc1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="95bc1-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="95bc1-104">手順 4: データを受信し、表示する</span><span class="sxs-lookup"><span data-stu-id="95bc1-104">Step 4: Receive and Display the Data</span></span>

<span data-ttu-id="95bc1-p101">この手順では、 [Recordset](datacontrol-object-rds.md) を取得するための XMLResponse.asp ファイルを示す **RDS.DataControl** オブジェクトが埋め込まれた HTML ファイルを作成します。Windows のメモ帳などのテキスト エディターで default.htm を開き、次のコードを追加します。URL の "sqlserver" は、実際に使用するサーバー コンピューターの名前に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="95bc1-p101">In this step you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**. Open default.htm with a text editor, such as Windows Notepad, and add the code below. Replace "sqlserver" in the URL with the name of your server computer.</span></span>

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

<span data-ttu-id="95bc1-108">Default.htm ファイルを閉じ、XMLResponse.asp を保存した同じフォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="95bc1-108">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> <span data-ttu-id="95bc1-109">4.0 またはそれ以降の Internet Explorer を使用すると、URL の https://*sql server*/XMLPersist/default.htm を開き、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="95bc1-109">Using Internet Explorer 4.0 or later, open the URL https://*sqlserver*/XMLPersist/default.htm and observe the results.</span></span> <span data-ttu-id="95bc1-110">データは、バインドされた DHTML テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="95bc1-110">The data is displayed in a bound DHTML table.</span></span> <span data-ttu-id="95bc1-111">これで URL の https://*sql server*/XMLPersist/XMLResponse.asp を開き、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="95bc1-111">Now open the URL https://*sqlserver*/XMLPersist/XMLResponse.asp and observe the results.</span></span> <span data-ttu-id="95bc1-112">XML が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95bc1-112">The XML is displayed.</span></span>

