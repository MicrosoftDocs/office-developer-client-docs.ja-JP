---
title: DBEngine.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 53df33e3171cde0d861f738a852350ec20bf0dec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477369"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="5a33d-102">DBEngine.LoginTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="5a33d-102">DBEngine.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="5a33d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a33d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5a33d-104">ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="5a33d-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a33d-105">構文</span><span class="sxs-lookup"><span data-stu-id="5a33d-105">Syntax</span></span>

<span data-ttu-id="5a33d-106">*式*です。LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="5a33d-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="5a33d-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="5a33d-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a33d-108">注釈</span><span class="sxs-lookup"><span data-stu-id="5a33d-108">Remarks</span></span>

<span data-ttu-id="5a33d-p101">**LoginTimeout** プロパティの既定の設定は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。</span><span class="sxs-lookup"><span data-stu-id="5a33d-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="5a33d-p102">Microsoft SQL Server などの ODBC データベースへのログオンを試みたときに、ネットワーク エラーが発生したりサーバーが実行中でないことが原因で、接続に失敗したりする場合があります。接続時に既定の 20 秒間待機する代わりに、エラーが発生するまでの時間を指定できます。外部のサーバー データベースに対するクエリの実行など、多くのさまざまなイベントの一部として、サーバーへの暗黙的なログオンが発生します。</span><span class="sxs-lookup"><span data-stu-id="5a33d-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>
