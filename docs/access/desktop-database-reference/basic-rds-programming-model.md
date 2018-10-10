---
title: 基本の RDS プログラミング モデル
TOCTitle: Basic RDS Programming Model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a90423f6bd05ae3d721faf97291ea6d21aa4393
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478122"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="3f31d-102">基本の RDS プログラミング モデル</span><span class="sxs-lookup"><span data-stu-id="3f31d-102">Basic RDS Programming Model</span></span>


<span data-ttu-id="3f31d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f31d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3f31d-p101">RDS は、次のような状況にあるクライアント アプリケーションを対象としています。このクライアント アプリケーションでは、サーバー上で実行するプログラムと、目的の情報を返すために必要なパラメーターを指定します。サーバー上で呼び出されたプログラムは、指定されたデータ ソースにアクセスして情報を取得し、必要に応じてそのデータを処理し、結果の情報は使用しやすい形式でクライアント アプリケーションに返します。RDS は、次に示す一連の操作を実行する手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f31d-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="3f31d-107">サーバーで呼び出されるプログラムを指定し、クライアントから参照する方法を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f31d-107">Specify the program to be invoked on the server, and obtain a way to refer to it from the client.</span></span> <span data-ttu-id="3f31d-108">(この参照とも呼ばれる*プロキシ*です。</span><span class="sxs-lookup"><span data-stu-id="3f31d-108">(This reference is sometimes called a *proxy*.</span></span> <span data-ttu-id="3f31d-109">リモート サーバー プログラムを表します。</span><span class="sxs-lookup"><span data-stu-id="3f31d-109">It represents the remote server program.</span></span> <span data-ttu-id="3f31d-110">クライアント アプリケーションは"call"プロキシ プログラムをローカルであるかが実際にはリモート サーバー プログラムを呼び出します。)</span><span class="sxs-lookup"><span data-stu-id="3f31d-110">The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

  - <span data-ttu-id="3f31d-p103">サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します。サーバー プログラムは、実際に ADO を使用してデータ ソースにアクセスします。ADO は、渡されたパラメーターの 1 つを使用して接続し、もう一方のパラメーターに指定されているコマンドを発行します。</span><span class="sxs-lookup"><span data-stu-id="3f31d-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

  - <span data-ttu-id="3f31d-p104">サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。また、 **Recordset** オブジェクトをサーバー上で処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="3f31d-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

  - <span data-ttu-id="3f31d-117">サーバー プログラムは、結果の **Recordset** オブジェクトをクライアント アプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="3f31d-117">The server program returns the final **Recordset** object to the client application.</span></span>

  - <span data-ttu-id="3f31d-118">クライアントでは、返された **Recordset** オブジェクトを、ビジュアル コントロールで使用しやすい形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="3f31d-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

  - <span data-ttu-id="3f31d-119">その **Recordset** オブジェクトに変更を加えた場合は、サーバー プログラムに変更が送り返され、その変更がデータ ソースに反映されます。</span><span class="sxs-lookup"><span data-stu-id="3f31d-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="3f31d-p105">このプログラミング モデルには、便利な機能があります。データ ソースへのアクセスに複雑なサーバー プログラムを必要としない場合は、必要な接続パラメーターおよびコマンド パラメーターを提供すると、自動的に、既定の簡単なサーバー プログラムを使用して指定データを取得できます。</span><span class="sxs-lookup"><span data-stu-id="3f31d-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="3f31d-p106">複雑な処理が必要な場合は、独自のカスタム サーバー プログラムを指定できます。たとえば、カスタム サーバー プログラムには ADO のすべての機能を自由に組み込むことができるので、複数の異なるデータ ソースに接続し、各データ ソースのデータを複雑な方法で組み合わせて 1 つの単純なデータに加工し、その結果をクライアント アプリケーションに返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="3f31d-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="3f31d-124">さらに、ADO では、必要に応じて、既定のサーバー プログラムの動作をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="3f31d-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>
