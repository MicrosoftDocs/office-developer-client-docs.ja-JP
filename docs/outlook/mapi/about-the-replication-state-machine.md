---
title: レプリケーション状態マシンについて
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9ea18f8e5c7eb758780727829fb1e18d2a19ec92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799611"
---
# <a name="about-the-replication-state-machine"></a><span data-ttu-id="82df8-103">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="82df8-103">About the Replication State Machine</span></span>

  
  
<span data-ttu-id="82df8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82df8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82df8-105">このトピックには、Microsoft Outlook 2013 および Microsoft Outlook 2010 のデータ ・ レプリケーションのステート マシンの概要が含まれています。</span><span class="sxs-lookup"><span data-stu-id="82df8-105">This topic contains an overview of the state machine for Microsoft Outlook 2013 and Microsoft Outlook 2010 data replication.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82df8-106">やサポートされているに使用するためにこのトピックの説明に従って、レプリケーション API を完全に実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82df8-106">The Replication API must be fully implemented according to the instructions in this topic in order to be useful or supported.</span></span> <span data-ttu-id="82df8-107">レプリケーション API は、サーバーとの間に 2013 の Outlook または Outlook 2010 の変更をレプリケートするには、排他的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="82df8-107">The Replication API is available exclusively to replicate Outlook 2013 or Outlook 2010 changes to and from a server.</span></span> 
  
## <a name="iostx-and-the-state-machine"></a><span data-ttu-id="82df8-108">IOSTX とステート マシン</span><span class="sxs-lookup"><span data-stu-id="82df8-108">IOSTX and the State Machine</span></span>

<span data-ttu-id="82df8-109">クライアントは、Outlook 2013 または Outlook 2010 のフォルダーとローカル ストアとサーバ間で項目を同期する順序で**[IOSTX::SyncBeg](iostx-syncbeg.md)**、 **[IOSTX::SyncEnd](iostx-syncend.md)**、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**、および**[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-109">A client calls **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**, and **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** in a sequence to synchronize Outlook 2013 or Outlook 2010 folders and items between a local store and a server.</span></span> <span data-ttu-id="82df8-110">呼び出しの実際の手順が異なります (例、2013 の Outlook または Outlook 2010 のフォルダーの階層、Outlook 2013 または Outlook 2010 のフォルダー、メール アイテム、予定表アイテム、およびなど) を複製する必要のあるデータと同期 (かどうかの方向ローカル ストアから、サーバーにアップロードまたはローカル ストアに、サーバーからダウンロード) します。</span><span class="sxs-lookup"><span data-stu-id="82df8-110">The actual sequence of calls depends on the data that needs to be replicated (for example, a hierarchy of Outlook 2013 or Outlook 2010 folders, an Outlook 2013 or Outlook 2010 folder, mail items, calendar items, and so on) and the direction of synchronization (whether uploading from the local store to the server, or downloading from the server to the local store).</span></span> <span data-ttu-id="82df8-111">以下は、典型的な呼び出しシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="82df8-111">Here is a typical sequence of calls:</span></span> 
  
1. <span data-ttu-id="82df8-112">クライアントでは、状態の識別子および対応するデータ構造体のアドレスへのポインターを指定する、レプリケーションを開始するのには**IOSTX::SyncBeg**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-112">The client calls **IOSTX::SyncBeg** to begin replication, specifying a state identifier and a pointer to an address of a corresponding data structure.</span></span> 
    
2. <span data-ttu-id="82df8-113">2013 の outlook または Outlook 2010 のデータ構造体、クライアントに必要な情報を持つデータ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="82df8-113">Outlook 2013 or Outlook 2010 allocates the data structure and initializes the data structure with the necessary information for the client.</span></span> 
    
3. <span data-ttu-id="82df8-114">クライアントは、ローカル ストアをレプリケーションに関する必要な情報を伝えるためにデータ構造を更新する、レプリケーションを行います。</span><span class="sxs-lookup"><span data-stu-id="82df8-114">The client performs the replication, updating the data structure to convey to the local store any necessary information about the replication.</span></span>
    
4. <span data-ttu-id="82df8-115">レプリケーションを実行すると、クライアントは、ローカル ストアの特定のレプリケーションの完了を通知するには、 **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** と**IOSTX::SyncEnd**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-115">After performing the replication, the client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** and **IOSTX::SyncEnd** to notify the local store of the completion of the specific replication.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="82df8-116">クライアントは、常にクライアントが特定の状態を開始するレプリケーションを終了するのには**IOSTX::SyncEnd**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-116">The client always calls **IOSTX::SyncEnd** to end a replication that the client has begun for a certain state.</span></span> <span data-ttu-id="82df8-117">によって、全体のデータを同期する必要のあるクライアントは、クライアントが、 **IOSTX::SyncBeg**および**IOSTX::SyncEnd**の呼び出しのペアを 2 回以上呼び出すことがあります。</span><span class="sxs-lookup"><span data-stu-id="82df8-117">Depending on the overall data that the client needs to synchronize, the client may call the pair of calls **IOSTX::SyncBeg** and **IOSTX::SyncEnd** more than once.</span></span> 
  
## <a name="state-table"></a><span data-ttu-id="82df8-118">状態テーブル</span><span class="sxs-lookup"><span data-stu-id="82df8-118">State Table</span></span>

> [!NOTE]
> <span data-ttu-id="82df8-119">レプリケーション状態機械の状態の対応する識別子とデータ構造体に有効なすべての状態を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="82df8-119">The following table lists all the valid states in the replication state machine, along with the corresponding state identifiers and data structures.</span></span> <span data-ttu-id="82df8-120">**データのレプリケート**] 列で [アイテム] という用語には、メール、予定表、連絡先、メモ、ジャーナル、および作業項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="82df8-120">In the **Data Replicated** column, the term "items" includes mail, calendar, contact, note, journal, and task items.</span></span> <span data-ttu-id="82df8-121">ローカル ストアからの変更をレプリケートするサーバーに、ときに、上のプレフィックス (たとえば、 **LR_SYNC_UPLOAD_HIERARCHY** 、 **[UPHIER](uphier.md)** ) で状態識別子の [アップロード] を指定してデータ構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="82df8-121">When replicating changes from the local store to the server, use state identifiers specifying "UPLOAD" and data structures with the "UP" prefix (for example, **LR_SYNC_UPLOAD_HIERARCHY** and **[UPHIER](uphier.md)** ).</span></span> <span data-ttu-id="82df8-122">ローカル ストアに、サーバーから変更をレプリケートする、ときに、"DN"のプレフィックス (たとえば、 **LR_SYNC_DOWNLOAD_HIERARCHY** 、 **[DNHIER](dnhier.md)** ) で状態識別子をダウンロードする] を指定してデータ構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="82df8-122">When replicating changes from the server to the local store, use state identifiers specifying "DOWNLOAD" and data structures with the "DN" prefix (for example, **LR_SYNC_DOWNLOAD_HIERARCHY** and **[DNHIER](dnhier.md)** ).</span></span> 
  
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82df8-123">**State**</span><span class="sxs-lookup"><span data-stu-id="82df8-123">**State**</span></span> <br/> |<span data-ttu-id="82df8-124">**レプリケートされたデータ**</span><span class="sxs-lookup"><span data-stu-id="82df8-124">**Data Replicated**</span></span> <br/> |<span data-ttu-id="82df8-125">**状態識別子**</span><span class="sxs-lookup"><span data-stu-id="82df8-125">**State Identifier**</span></span> <br/> |<span data-ttu-id="82df8-126">**データ構造体**</span><span class="sxs-lookup"><span data-stu-id="82df8-126">**Data Structure**</span></span> <br/> |
|[<span data-ttu-id="82df8-127">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="82df8-127">Idle state</span></span>](idle-state.md) <br/> | <span data-ttu-id="82df8-128">*None*</span><span class="sxs-lookup"><span data-stu-id="82df8-128">*None*</span></span>  <br/> |<span data-ttu-id="82df8-129">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="82df8-129">**LR_SYNC_IDLE**</span></span> <br/> | <span data-ttu-id="82df8-130">*None*</span><span class="sxs-lookup"><span data-stu-id="82df8-130">*None*</span></span>  <br/> |
|[<span data-ttu-id="82df8-131">状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="82df8-131">Synchronize state</span></span>](synchronize-state.md) <br/> |<span data-ttu-id="82df8-132">フォルダーまたはアイテム</span><span class="sxs-lookup"><span data-stu-id="82df8-132">Folders or items</span></span>  <br/> |<span data-ttu-id="82df8-133">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="82df8-133">**LR_SYNC**</span></span> <br/> |<span data-ttu-id="82df8-134">**[同期](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-134">**[SYNC](sync.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-135">階層の状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-135">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |<span data-ttu-id="82df8-136">フォルダー</span><span class="sxs-lookup"><span data-stu-id="82df8-136">Folders</span></span>  <br/> |<span data-ttu-id="82df8-137">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="82df8-137">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |<span data-ttu-id="82df8-138">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-138">**[UPHIER](uphier.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-139">アップロード フォルダーの状態</span><span class="sxs-lookup"><span data-stu-id="82df8-139">Upload folder state</span></span>](upload-folder-state.md) <br/> |<span data-ttu-id="82df8-140">Folder</span><span class="sxs-lookup"><span data-stu-id="82df8-140">Folder</span></span>  <br/> |<span data-ttu-id="82df8-141">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="82df8-141">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |<span data-ttu-id="82df8-142">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-142">**[UPFLD](upfld.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-143">内容の状態を同期します。</span><span class="sxs-lookup"><span data-stu-id="82df8-143">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |<span data-ttu-id="82df8-144">アイテム</span><span class="sxs-lookup"><span data-stu-id="82df8-144">Items</span></span>  <br/> |<span data-ttu-id="82df8-145">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="82df8-145">**LR_SYNC_CONTENTS**</span></span> <br/> |<span data-ttu-id="82df8-146">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-146">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-147">テーブルの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-147">Upload table state</span></span>](upload-table-state.md) <br/> |<span data-ttu-id="82df8-148">アイテム</span><span class="sxs-lookup"><span data-stu-id="82df8-148">Items</span></span>  <br/> |<span data-ttu-id="82df8-149">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="82df8-149">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |<span data-ttu-id="82df8-150">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-150">**[UPTBL](uptbl.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-151">メッセージの状態をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-151">Upload message state</span></span>](upload-message-state.md) <br/> |<span data-ttu-id="82df8-152">Item</span><span class="sxs-lookup"><span data-stu-id="82df8-152">Item</span></span>  <br/> |<span data-ttu-id="82df8-153">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="82df8-153">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |<span data-ttu-id="82df8-154">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-154">**[UPMSG](upmsg.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-155">読み取りステータスをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-155">Upload read status state</span></span>](upload-read-status-state.md) <br/> |<span data-ttu-id="82df8-156">アイテム</span><span class="sxs-lookup"><span data-stu-id="82df8-156">Items</span></span>  <br/> |<span data-ttu-id="82df8-157">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="82df8-157">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |<span data-ttu-id="82df8-158">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-158">**[UPREAD](upread.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-159">削除ステータスをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-159">Upload delete status state</span></span>](upload-delete-status-state.md) <br/> |<span data-ttu-id="82df8-160">アイテム</span><span class="sxs-lookup"><span data-stu-id="82df8-160">Items</span></span>  <br/> |<span data-ttu-id="82df8-161">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="82df8-161">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |<span data-ttu-id="82df8-162">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-162">**[UPDEL](updel.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-163">階層の状態をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-163">Download hierarchy state</span></span>](download-hierarchy-state.md) <br/> |<span data-ttu-id="82df8-164">フォルダー</span><span class="sxs-lookup"><span data-stu-id="82df8-164">Folders</span></span>  <br/> |<span data-ttu-id="82df8-165">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="82df8-165">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |<span data-ttu-id="82df8-166">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-166">**[DNHIER](dnhier.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-167">テーブルの状態をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-167">Download table state</span></span>](download-table-state.md) <br/> |<span data-ttu-id="82df8-168">アイテム</span><span class="sxs-lookup"><span data-stu-id="82df8-168">Items</span></span>  <br/> |<span data-ttu-id="82df8-169">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="82df8-169">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |<span data-ttu-id="82df8-170">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-170">**[DNTBL](dntbl.md)**</span></span> <br/> |
|[<span data-ttu-id="82df8-171">メッセージ ヘッダーの状態をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-171">Download message header state</span></span>](download-message-header-state.md) <br/> |<span data-ttu-id="82df8-172">メッセージのヘッダー</span><span class="sxs-lookup"><span data-stu-id="82df8-172">Message header</span></span>  <br/> |<span data-ttu-id="82df8-173">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="82df8-173">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |<span data-ttu-id="82df8-174">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="82df8-174">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
   
## <a name="state-transition-diagram"></a><span data-ttu-id="82df8-175">状態遷移図</span><span class="sxs-lookup"><span data-stu-id="82df8-175">State Transition Diagram</span></span>

<span data-ttu-id="82df8-176">次の図では、アップロードするか、フォルダーまたはフォルダー (メール、予定表、連絡先、メモ、タスク、または仕訳帳の項目) の内容の完全な同期 (アップロード後にダウンロード) を実行するときに発生する状態の遷移を示します。</span><span class="sxs-lookup"><span data-stu-id="82df8-176">The following diagram shows the state transitions that occur when uploading or performing a full synchronization (downloading followed by uploading) of folders or contents of folders (mail, calendar, contact, note, task, or journal items).</span></span> 
  
<span data-ttu-id="82df8-177">挿入アートをここでは不足しているに @@@NEED。</span><span class="sxs-lookup"><span data-stu-id="82df8-177">@@@@@NEED TO INSERT ART HERE THAT IS MISSING@@@@@@</span></span>
  
## <a name="example-uploading-a-folder-hierarchy"></a><span data-ttu-id="82df8-178">アップロードするフォルダー階層の例。</span><span class="sxs-lookup"><span data-stu-id="82df8-178">Example: Uploading a Folder Hierarchy</span></span>

 <span data-ttu-id="82df8-179">フォルダーの階層構造をアップロードすると、次の一連の手順が実行されます。</span><span class="sxs-lookup"><span data-stu-id="82df8-179">When uploading a hierarchy of folders, the following sequence of steps takes place:</span></span> 
  
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82df8-180">**手順**</span><span class="sxs-lookup"><span data-stu-id="82df8-180">**Step**</span></span> <br/> |<span data-ttu-id="82df8-181">**アクション**</span><span class="sxs-lookup"><span data-stu-id="82df8-181">**Action**</span></span> <br/> |<span data-ttu-id="82df8-182">**State**</span><span class="sxs-lookup"><span data-stu-id="82df8-182">**State**</span></span> <br/> |<span data-ttu-id="82df8-183">**関連するデータ構造体**</span><span class="sxs-lookup"><span data-stu-id="82df8-183">**Related Data Structure**</span></span> <br/> |
|<span data-ttu-id="82df8-184">1。</span><span class="sxs-lookup"><span data-stu-id="82df8-184">1.</span></span>  <br/> |<span data-ttu-id="82df8-185">クライアントは、 **IOSTX::SyncBeg**と階層構造のアップロードを開始します。</span><span class="sxs-lookup"><span data-stu-id="82df8-185">The client initiates the hierarchy upload with **IOSTX::SyncBeg**.</span></span>  <br/> |<span data-ttu-id="82df8-186">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="82df8-186">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |<span data-ttu-id="82df8-187">**UPHIER**</span><span class="sxs-lookup"><span data-stu-id="82df8-187">**UPHIER**</span></span> <br/> |
|<span data-ttu-id="82df8-188">2。</span><span class="sxs-lookup"><span data-stu-id="82df8-188">2.</span></span>  <br/> |<span data-ttu-id="82df8-189">2013 の outlook または Outlook 2010 は、クライアントの情報が**UPHIER**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="82df8-189">Outlook 2013 or Outlook 2010 populates **UPHIER** with information for the client.</span></span> <span data-ttu-id="82df8-190">[Out] パラメーターの初期化が含まれます: *iEnt*は、0、およびアップロードする必要がある階層内のフォルダーの数には、*セント*に設定されています。</span><span class="sxs-lookup"><span data-stu-id="82df8-190">This includes initializing the [out] parameters:  *iEnt*  is set to 0, and  *cEnt*  to the number of folders in the hierarchy that needs uploading.</span></span>  <br/> |<span data-ttu-id="82df8-191">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="82df8-191">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |<span data-ttu-id="82df8-192">**UPHIER**</span><span class="sxs-lookup"><span data-stu-id="82df8-192">**UPHIER**</span></span> <br/> |
|<span data-ttu-id="82df8-193">3。</span><span class="sxs-lookup"><span data-stu-id="82df8-193">3.</span></span>  <br/> |<span data-ttu-id="82df8-194">クライアントには、実際の階層構造のアップロードが行われます。</span><span class="sxs-lookup"><span data-stu-id="82df8-194">The client does the actual hierarchy upload.</span></span> <span data-ttu-id="82df8-195">たとえば、*セント*が、10 個のフォルダーのそれぞれについて、10 の場合、クライアントは**IOSTX::SyncBeg**、適切な状態の識別子およびフォルダーをアップロードするデータ構造体を指定するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-195">As an example, if  *cEnt*  is 10, for each of the 10 folders, the client calls **IOSTX::SyncBeg**, specifying the appropriate state identifier and data structure for uploading a folder.</span></span>  <br/> |<span data-ttu-id="82df8-196">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="82df8-196">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |<span data-ttu-id="82df8-197">**UPFLD**</span><span class="sxs-lookup"><span data-stu-id="82df8-197">**UPFLD**</span></span> <br/> |
|<span data-ttu-id="82df8-198">4。</span><span class="sxs-lookup"><span data-stu-id="82df8-198">4.</span></span>  <br/> |<span data-ttu-id="82df8-199">2013 の outlook または Outlook 2010 は、フォルダーのアップロード、フォルダー オブジェクトへのポインターの理由と、フォルダーのエントリ ID を含む、[out] パラメーターを初期化することによって**UPFLD**を設定します。</span><span class="sxs-lookup"><span data-stu-id="82df8-199">Outlook 2013 or Outlook 2010 populates **UPFLD** by initializing its [out] parameters, including the reason for the folder upload, the pointer to the folder object, and the entry ID for the folder.</span></span>  <br/> |<span data-ttu-id="82df8-200">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="82df8-200">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |<span data-ttu-id="82df8-201">**UPFLD**</span><span class="sxs-lookup"><span data-stu-id="82df8-201">**UPFLD**</span></span> <br/> |
|<span data-ttu-id="82df8-202">5。</span><span class="sxs-lookup"><span data-stu-id="82df8-202">5.</span></span>  <br/> |<span data-ttu-id="82df8-203">クライアントは、指定したフォルダーをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="82df8-203">The client uploads the specified folder.</span></span>  <br/> |<span data-ttu-id="82df8-204">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="82df8-204">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |<span data-ttu-id="82df8-205">**UPFLD**</span><span class="sxs-lookup"><span data-stu-id="82df8-205">**UPFLD**</span></span> <br/> |
|<span data-ttu-id="82df8-206">6。</span><span class="sxs-lookup"><span data-stu-id="82df8-206">6.</span></span>  <br/> |<span data-ttu-id="82df8-207">クライアントは、ローカル ストアのフォルダーのアップロードの完了を通知: 成功すると、クライアントの設定、[in] パラメーター *ulFlags*を**UPF_OK**、および、 **IOSTX::SetSyncResult (S_OK)** の呼び出しと**UPFLD**と**IOSTX::SyncEnd**.</span><span class="sxs-lookup"><span data-stu-id="82df8-207">The client notifies the local store of the completion of the folder upload: Upon success, the client sets the [in] parameter  *ulFlags*  in **UPFLD** with **UPF_OK**, and then calls **IOSTX::SetSyncResult (S_OK)** and **IOSTX::SyncEnd**.</span></span> <span data-ttu-id="82df8-208">障害時に、クライアントの場合は、 **UPF_OK**フラグを使って*ulFlags*に未設定。</span><span class="sxs-lookup"><span data-stu-id="82df8-208">Upon failure, the client would not set  *ulFlags*  with the **UPF_OK** flag.</span></span> <span data-ttu-id="82df8-209">**IOSTX::SetSyncResult**、 **HRESULT**の値、および**IOSTX::SyncEnd**を渡して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-209">It calls **IOSTX::SetSyncResult**, passing in the **HRESULT** value, and **IOSTX::SyncEnd**.</span></span>  <br/> |<span data-ttu-id="82df8-210">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="82df8-210">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |<span data-ttu-id="82df8-211">**UPFLD**</span><span class="sxs-lookup"><span data-stu-id="82df8-211">**UPFLD**</span></span> <br/> |
|<span data-ttu-id="82df8-212">7。</span><span class="sxs-lookup"><span data-stu-id="82df8-212">7.</span></span>  <br/> |<span data-ttu-id="82df8-213">**UPF_OK**を設定すると、Outlook 2013 または Outlook 2010 は、フォルダーをアップロードするための内部要求がクリアされます。</span><span class="sxs-lookup"><span data-stu-id="82df8-213">If **UPF_OK** is set, Outlook 2013 or Outlook 2010 will clear the internal request for uploading the folder.</span></span> <span data-ttu-id="82df8-214">*UlFlags*の状態に関係なくをクリーンアップします、内部のブックキーピング情報です。</span><span class="sxs-lookup"><span data-stu-id="82df8-214">Then regardless of the state of  *ulFlags*  , it will clean up any internal bookkeeping information.</span></span> <span data-ttu-id="82df8-215">残っている状態のフォルダーをアップロードするのには階層構造で (*iEnt* 、*セント*よりも小さく)、クライアントと Outlook 2013 または Outlook 2010 は、手順 3 ~ 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="82df8-215">While there are still folders in the hierarchy to upload (*iEnt*  is still less than  *cEnt*), the client and Outlook 2013 or Outlook 2010 repeat steps 3 through 7.</span></span>  <br/> |<span data-ttu-id="82df8-216">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="82df8-216">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |<span data-ttu-id="82df8-217">**UPFLD**</span><span class="sxs-lookup"><span data-stu-id="82df8-217">**UPFLD**</span></span> <br/> |
|<span data-ttu-id="82df8-218">8。</span><span class="sxs-lookup"><span data-stu-id="82df8-218">8.</span></span>  <br/> |<span data-ttu-id="82df8-219">クライアントは、ローカル ストアの階層構造のアップロードの完了を通知: 成功すると、クライアントの設定、[in] **IOSTX::SetSyncResult (S_OK)** と**IOSTX::SyncEnd**で**UPH_OK**、およびその後の呼び出しでは、 **UPHIER**フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="82df8-219">The client notifies the local store of the completion of the hierarchy upload: Upon success, the client sets the [in] flag in **UPHIER** with **UPH_OK**, and then calls **IOSTX::SetSyncResult (S_OK)** and **IOSTX::SyncEnd**.</span></span> <span data-ttu-id="82df8-220">障害時に、クライアント設定はありません**UPH_OK**のフラグ。</span><span class="sxs-lookup"><span data-stu-id="82df8-220">Upon failure, the client would not set the **UPH_OK** flag.</span></span> <span data-ttu-id="82df8-221">**IOSTX::SetSyncResult**、 **HRESULT**の値、および**IOSTX::SyncEnd**を渡して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="82df8-221">It calls **IOSTX::SetSyncResult**, passing in the **HRESULT** value, and **IOSTX::SyncEnd**.</span></span>  <br/> |<span data-ttu-id="82df8-222">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="82df8-222">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |<span data-ttu-id="82df8-223">**UPHIER**</span><span class="sxs-lookup"><span data-stu-id="82df8-223">**UPHIER**</span></span> <br/> |
|<span data-ttu-id="82df8-224">9。</span><span class="sxs-lookup"><span data-stu-id="82df8-224">9.</span></span>  <br/> |<span data-ttu-id="82df8-225">**UPH_OK**が設定されている場合は、Outlook 2013 または Outlook 2010 と階層をアップロードするための内部要求がクリアされます。</span><span class="sxs-lookup"><span data-stu-id="82df8-225">If **UPH_OK** is set, Outlook 2013 or Outlook 2010 will clear the internal request for uploading the hierarchy.</span></span> <span data-ttu-id="82df8-226">*UlFlags*の状態に関係なくをクリーンアップします、内部のブックキーピング情報です。</span><span class="sxs-lookup"><span data-stu-id="82df8-226">Then regardless of the state of  *ulFlags*  , it will clean up any internal bookkeeping information.</span></span>  <br/> |<span data-ttu-id="82df8-227">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="82df8-227">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |<span data-ttu-id="82df8-228">**UPHIER**</span><span class="sxs-lookup"><span data-stu-id="82df8-228">**UPHIER**</span></span> <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82df8-229">関連項目</span><span class="sxs-lookup"><span data-stu-id="82df8-229">See also</span></span>



[<span data-ttu-id="82df8-230">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="82df8-230">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="82df8-231">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="82df8-231">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="82df8-232">同期状態</span><span class="sxs-lookup"><span data-stu-id="82df8-232">SYNCSTATE</span></span>](syncstate.md)
