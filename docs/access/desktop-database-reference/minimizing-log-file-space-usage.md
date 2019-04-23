---
title: ログ ファイルの使用領域の最小化
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288877"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="312d3-102">ログ ファイルの使用領域の最小化</span><span class="sxs-lookup"><span data-stu-id="312d3-102">Minimizing log file space usage</span></span>

<span data-ttu-id="312d3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="312d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="312d3-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span><span class="sxs-lookup"><span data-stu-id="312d3-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="312d3-106">**Microsoft SQL Server 6.5 でチェックポイント時のログの切り捨てを有効にするには**</span><span class="sxs-lookup"><span data-stu-id="312d3-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="312d3-107">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="312d3-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="312d3-108">この機能を有効にするデータベースの名前をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="312d3-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="312d3-109">From the **Database** tab, select **Truncate**.</span><span class="sxs-lookup"><span data-stu-id="312d3-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="312d3-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span><span class="sxs-lookup"><span data-stu-id="312d3-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="312d3-111">**Microsoft SQL Server 7.0 でチェックポイント時のログの切り捨てを有効にするには**</span><span class="sxs-lookup"><span data-stu-id="312d3-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="312d3-112">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベースのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="312d3-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="312d3-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span><span class="sxs-lookup"><span data-stu-id="312d3-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="312d3-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span><span class="sxs-lookup"><span data-stu-id="312d3-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="312d3-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span><span class="sxs-lookup"><span data-stu-id="312d3-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

