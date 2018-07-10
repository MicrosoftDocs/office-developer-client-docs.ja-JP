---
title: スレッド セーフなオブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8c8c89f3626d54f04896ad54de5d7e480dd9b568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800968"
---
# <a name="implementing-thread-safe-objects"></a><span data-ttu-id="e4763-103">スレッド セーフなオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="e4763-103">Implementing Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="e4763-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4763-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4763-105">直接インターフェイス メソッドの呼び出しから返されるオブジェクトの場合は、スレッド セーフのプロバイダーの責任は。</span><span class="sxs-lookup"><span data-stu-id="e4763-105">With objects that are returned from interface method calls directly, it is the provider's responsibility to ensure thread-safety.</span></span> <span data-ttu-id="e4763-106">コールバック オブジェクトとは、クライアント アプリケーションの責任です。</span><span class="sxs-lookup"><span data-stu-id="e4763-106">With callback objects, it is the client application's responsibility.</span></span>
  
<span data-ttu-id="e4763-107">クライアントは、MAPI ユーティリティ[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すことにより、スレッド セーフである通知コールバックを実装できます。</span><span class="sxs-lookup"><span data-stu-id="e4763-107">A client can implement a thread-safe notification callback by calling the MAPI utility [HrThisThreadAdviseSink](hrthisthreadadvisesink.md).</span></span> <span data-ttu-id="e4763-108">**HrThisThreadAdviseSink**は、スレッド セーフのアドバイズ シンクをスレッド セーフである 1 つに変換します。</span><span class="sxs-lookup"><span data-stu-id="e4763-108">**HrThisThreadAdviseSink** transforms a non-thread-safe advise sink into a thread-safe one.</span></span> <span data-ttu-id="e4763-109">進捗状況のコールバックには、このようなユーティリティはありません。</span><span class="sxs-lookup"><span data-stu-id="e4763-109">For progress callbacks, there is no such utility.</span></span> <span data-ttu-id="e4763-110">クライアントは、MAPI 処理中のスレッド セーフであるオブジェクトを使用するか、手動で作成できます。</span><span class="sxs-lookup"><span data-stu-id="e4763-110">A client can choose to use the MAPI thread-safe progress object or create one manually.</span></span> 
  
<span data-ttu-id="e4763-111">スレッド セーフなオブジェクトは、できない可能性がありますもスレッドに対応していません。</span><span class="sxs-lookup"><span data-stu-id="e4763-111">A thread-safe object might or might not also be thread-aware.</span></span> <span data-ttu-id="e4763-112">スレッドに対応していないオブジェクトは、それを使用するすべてのスレッドを別のコンテキストを保持します。</span><span class="sxs-lookup"><span data-stu-id="e4763-112">A thread-aware object maintains a separate context for every thread that is using it.</span></span> <span data-ttu-id="e4763-113">サービス プロバイダーは、スレッド対応のサポートはいくつかの状況で役に立ちますが、スレッド セーフのオブジェクトでスレッド認識をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e4763-113">Service providers are not required to support thread-awareness in their thread-safe objects, although supporting thread-awareness can be useful in some situations.</span></span> <span data-ttu-id="e4763-114">2 つの MAPI テーブルは、常に定義して、独自のコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="e4763-114">Two MAPI tables always provide their own context by definition.</span></span> <span data-ttu-id="e4763-115">1 つのテーブルを異なるスレッドで使用しないし、一意のコンテキストを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4763-115">One table used on different threads does not and should not provide unique context.</span></span>
  
<span data-ttu-id="e4763-116">**生じます**に使用した同じスレッドで通知を受け取る間、クライアントことができます**アドバイス**の呼び出しに使用されたのと同じスレッド上または MAPI によって所有されている別のスレッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e4763-116">A client can choose between receiving notifications on the same thread that was used for the **MAPIInitialize** call, on the same thread that was used for the **Advise** call, or on a separate thread owned by MAPI.</span></span> <span data-ttu-id="e4763-117">**生じます**を呼び出すために使用されたのと同じスレッド上に通知が到達することを確認するには、クライアントは[生じます](mapiinitialize.md)を呼び出すし、 **ulFlags** 、 [MAPIINIT_0](mapiinit_0.md)構造体のメンバーに 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="e4763-117">To ensure that notifications arrive on the same thread that was used to call **MAPIInitialize**, a client calls [MAPIInitialize](mapiinitialize.md) and passes zero in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="e4763-118">通知は、メイン メッセージ ループの中に配信されます。</span><span class="sxs-lookup"><span data-stu-id="e4763-118">Notifications are then delivered during the main message loop.</span></span> 
  
<span data-ttu-id="e4763-119">MAPI が所有するスレッドに通知を受信するには、クライアントは、 **ulFlags** 、 **MAPIINIT_0**構造体のメンバー MAPI_MULTITHREAD_NOTIFICATIONS に設定して**生じます**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e4763-119">To receive notifications on the MAPI-owned thread, a client calls **MAPIInitialize** with the **ulFlags** member of the **MAPIINIT_0** structure set to MAPI_MULTITHREAD_NOTIFICATIONS.</span></span> <span data-ttu-id="e4763-120">**アドバイス**の呼び出しが行われるクライアントがラップされたバージョンではなく、シンク オブジェクトに通知します。</span><span class="sxs-lookup"><span data-stu-id="e4763-120">The **Advise** call is made with the client's advise sink object rather than a wrapped version.</span></span> 
  
<span data-ttu-id="e4763-121">**アドバイズ**を呼び出すために使用されたのと同じスレッド上に通知が到達することを確認するには、クライアントが[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すし、パスが新しく作成されたラップが**アドバイズ**シンクではなく元のアドバイズ シンクをアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="e4763-121">To ensure that notifications arrive on the same thread that was used to call **Advise**, a client calls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) and passes the newly created wrapped advise sink to **Advise** rather than the original advise sink.</span></span> <span data-ttu-id="e4763-122">**生じます**は、いずれかのフラグの値を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e4763-122">**MAPIInitialize** can be called with either flag value.</span></span> 
  
