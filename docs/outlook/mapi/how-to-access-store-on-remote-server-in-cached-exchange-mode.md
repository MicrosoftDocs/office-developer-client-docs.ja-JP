---
title: Outlook が Exchange キャッシュ モードではリモート サーバー上のストアにアクセスします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 8f1afd31f017b73fa5270d8fbf4c2a1c8fa08880
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800233"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="c7e93-103">Outlook が Exchange キャッシュ モードではリモート サーバー上のストアにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c7e93-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="c7e93-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7e93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7e93-105">このトピックには、 **MAPI_NO_CACHE**フラグを使用して Microsoft Office Outlook が Exchange キャッシュ モードではときに、フォルダーまたはリモート サーバー上のメッセージ ストアにメッセージを開く方法を示している C++ でのコード サンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7e93-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="c7e93-106">Exchange キャッシュ モードでは、Outlook ユーザーのメールボックスをリモートの Exchange サーバー上のリモート ・ コピーへのオンライン接続を維持するときに、ユーザーのメールボックスのローカル コピーを使用するように Outlook を許可します。</span><span class="sxs-lookup"><span data-stu-id="c7e93-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="c7e93-107">Outlook が既定では、Exchange キャッシュ モードで実行されている場合、同じセッションにログオンしている MAPI ソリューションでは、キャッシュされたメッセージ ストアに接続されています。</span><span class="sxs-lookup"><span data-stu-id="c7e93-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="c7e93-108">アクセスされているすべてのデータと加えられた変更は、メールボックスのローカル コピーに対して行われます。</span><span class="sxs-lookup"><span data-stu-id="c7e93-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="c7e93-109">クライアントまたはサービス プロバイダーは、ローカル メッセージ ストアへの接続をオーバーライドし、 **[IMsgStore::OpenEntry](imsgstore-openentry.md)** を呼び出すときは、 *ulFlags*パラメーターで**MAPI_NO_CACHE**のビットを設定することにより、メッセージまたはリモート ストア上のフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="c7e93-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="c7e93-110">次のコード サンプルは、リモート メッセージ ストアのルート フォルダーを開く、 *ulFlags*パラメーターの設定**MAPI_NO_CACHE**フラグを使用して**IMsgStore::OpenEntry**を呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c7e93-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="c7e93-111">リモート サーバー上で**MDB_ONLINE**フラグを使用してメッセージ ・ ストアを開いた場合、 **MAPI_NO_CACHE**フラグを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c7e93-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7e93-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7e93-112">See also</span></span>

- [<span data-ttu-id="c7e93-113">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="c7e93-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="c7e93-114">ストアがリモート サーバーと Outlook の Exchange キャッシュ モードでは、開いています。</span><span class="sxs-lookup"><span data-stu-id="c7e93-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="c7e93-115">OST 内のメッセージを Exchange キャッシュ モードで同期を呼び出すことがなく管理します。</span><span class="sxs-lookup"><span data-stu-id="c7e93-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)
