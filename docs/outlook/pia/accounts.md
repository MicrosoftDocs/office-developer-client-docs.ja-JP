---
title: アカウント
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb7c56a8a261f36628c3b440c1aeec31c7aec46e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406821"
---
# <a name="accounts"></a><span data-ttu-id="53687-102">アカウント</span><span class="sxs-lookup"><span data-stu-id="53687-102">Accounts</span></span> 

<span data-ttu-id="53687-103">このセクションでは、電子メール アカウントに関連するサンプル タスクを示します。</span><span class="sxs-lookup"><span data-stu-id="53687-103">This section provides sample tasks that involve views.</span></span> <span data-ttu-id="53687-104">電子メール アカウントの例は、Microsoft Exchange Server、Post Office Protocol 3 (POP3)、Internet Message Access Protocol (IMAP)、および Hypertext Transfer Protocol (HTTP) のアカウントです。</span><span class="sxs-lookup"><span data-stu-id="53687-104">This section provides sample tasks that involve e-mail accounts. Examples of e-mail accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts. An account for the current profile is represented by an Account object.</span></span> <span data-ttu-id="53687-105">現在のプロファイルのアカウントは、[Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) オブジェクトによって表されます。</span><span class="sxs-lookup"><span data-stu-id="53687-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="53687-106">トピック</span><span class="sxs-lookup"><span data-stu-id="53687-106">Topic</span></span>|<span data-ttu-id="53687-107">説明</span><span class="sxs-lookup"><span data-stu-id="53687-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="53687-108">アカウント情報を取得する</span><span class="sxs-lookup"><span data-stu-id="53687-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="53687-109">信頼されている Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) オブジェクトを入力引数として受け取り、 **Account** オブジェクトを使用して、現在の Outlook プロファイルで使用できる各アカウントの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="53687-109">Takes as an input argument a trusted Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="53687-110">現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="53687-110">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="53687-111">送信可能な電子メール アイテムと会議出席依頼を作成する方法と、それらを現在のフォルダーに基づく特定のアカウントを使用して送信する方法を示す 2 つのコード例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53687-111">Contains two code examples that show how to create a sendable e-mail item and meeting request, and then to send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="53687-112">フォルダーのアカウントを取得する</span><span class="sxs-lookup"><span data-stu-id="53687-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="53687-113">現在のセッションで特定のフォルダーに関連付けられているアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="53687-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="53687-114">複数のアカウントの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="53687-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="53687-115">現在のプロファイルの各アカウントの情報を取得して表示します。</span><span class="sxs-lookup"><span data-stu-id="53687-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|<span data-ttu-id="53687-116">[Hotmail アカウントを使用してメール アイテムを送信する](how-to-send-a-mail-item-by-using-a-hotmail-account.md)</span><span class="sxs-lookup"><span data-stu-id="53687-116">Uses the [SendUsingAccount](how-to-send-a-mail-item-by-using-a-hotmail-account.md) property to send a mail item by using a Windows Live Hotmail account.</span></span> | <span data-ttu-id="53687-117">[SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) プロパティを使用し、Windows Live Hotmail アカウントを使用して、メール アイテムを送信します。</span><span class="sxs-lookup"><span data-stu-id="53687-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="53687-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="53687-118">See also</span></span>

- [<span data-ttu-id="53687-119">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="53687-119">Exchange Users</span></span>](exchange-users.md)
- [<span data-ttu-id="53687-120">メール</span><span class="sxs-lookup"><span data-stu-id="53687-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="53687-121">受信者</span><span class="sxs-lookup"><span data-stu-id="53687-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="53687-122">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="53687-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
