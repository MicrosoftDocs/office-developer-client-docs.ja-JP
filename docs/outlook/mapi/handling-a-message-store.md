---
title: メッセージ ストアの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f915a17b8271f7ec4173f507504bf165a6084085
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800188"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="0d972-103">メッセージ ストアの処理</span><span class="sxs-lookup"><span data-stu-id="0d972-103">Handling a message store</span></span>
  
<span data-ttu-id="0d972-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d972-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d972-105">メッセージ ストアの処理は、任意のクライアントの一連のタスクの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="0d972-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="0d972-106">開く、コピー、移動、追加、およびフォルダーと、さまざまなテーブルを表示する、プロパティの設定、およびアクセス レベルを制御するメッセージを削除して、これらのタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d972-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="0d972-107">[メッセージ ストアを開く](opening-a-message-store.md): セッション中に 1 つまたは複数のメッセージ ストアを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="0d972-108">[既定のメッセージ ストアを開く](opening-the-default-message-store.md): 既定のメッセージ ストアを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="0d972-109">[検証しメッセージ ストアを初期化](validating-and-initializing-a-message-store.md): 初期化し、メッセージ ストアを検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="0d972-110">[メッセージ ストアを検索](searching-a-message-store.md): 検索条件に一致するメッセージを探して、1 つまたは複数のフォルダーを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="0d972-111">[受信フォルダーを選択する](selecting-a-receive-folder.md): 受信フォルダーを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="0d972-112">[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md): フォルダーを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="0d972-113">[フォルダーの内容のテーブルを表示する](displaying-a-folder-contents-table.md): そのメッセージのすべてについての概要情報が含まれているフォルダーの内容テーブルを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="0d972-114">[受信トレイ フォルダーを通過する](traversing-the-inbox-folder.md): 受信トレイ内のすべてのメッセージを順番にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="0d972-115">[コピーまたは移動するメッセージまたはフォルダー](copying-or-moving-a-message-or-a-folder.md): コピーまたは 1 つまたは複数のメッセージを移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="0d972-116">[メッセージを開く](opening-a-message.md): メッセージを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="0d972-117">[メッセージのアイコンを検索する](finding-the-icon-for-a-message.md): メッセージに関連付けられているアイコンを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="0d972-118">[ビュー記述子を開く](opening-a-view-descriptor.md): ビュー記述子を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="0d972-119">[メッセージを削除する](deleting-a-message.md): メッセージを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="0d972-120">[受信トレイにメッセージを保存](saving-a-message-in-the-inbox.md): 受信トレイにメッセージを格納する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="0d972-121">[検索を送信またはメッセージの保存](finding-sent-or-saved-messages.md): 保存または送信されたすべての送信メッセージを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="0d972-122">[会話の追跡](tracking-conversations.md): 会話を追跡する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d972-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    
