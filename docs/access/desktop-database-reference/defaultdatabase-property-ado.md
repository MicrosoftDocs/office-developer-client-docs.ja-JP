---
title: DefaultDatabase プロパティ (ADO)
TOCTitle: DefaultDatabase Property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 136e6bc0d68aac987a331ce20b8fca36a72afa73
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478215"
---
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="f8080-102">DefaultDatabase プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8080-102">DefaultDatabase Property (ADO)</span></span>


<span data-ttu-id="f8080-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8080-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8080-104">[Connection](connection-object-ado.md) オブジェクトの既定のデータベースを示します。</span><span class="sxs-lookup"><span data-stu-id="f8080-104">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f8080-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="f8080-105">Settings and Return Values</span></span>

<span data-ttu-id="f8080-106">プロバイダーで使用可能なデータベースの名前に評価される文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="f8080-106">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8080-107">解説</span><span class="sxs-lookup"><span data-stu-id="f8080-107">Remarks</span></span>

<span data-ttu-id="f8080-108">**DefaultDatabase** プロパティは、特定の **Connection** オブジェクトの既定のデータベースの名前を設定または取得するために使います。</span><span class="sxs-lookup"><span data-stu-id="f8080-108">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="f8080-p101">既定のデータベースがある場合、そのデータベースのオブジェクトにアクセスする SQL 文の構文が不適切な場合があります。 **DefaultDatabase** プロパティで指定されたデータベース以外のデータベースのオブジェクトにアクセスするには、オブジェクト名を目的のデータベース名で修飾する必要があります。接続時に、プロバイダーは **DefaultDatabase** プロパティに既定のデータベース情報を書き込みます。プロバイダーの中には 1 つの接続に 1 つのデータベースしか許可しないものがあり、その場合は **DefaultDatabase** プロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="f8080-p101">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database. To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name. Upon connection, the provider will write default database information to the **DefaultDatabase** property. Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="f8080-113">データ ソースとプロバイダーによっては、この機能をサポートせず、エラーまたは空の文字列を返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="f8080-113">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="f8080-114">**リモート データ サービスの使用法**このプロパティはクライアント側の**接続**オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8080-114">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>
