---
title: MAPI Url の通知に基づくインデックス作成について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 27ad80b9eca8332beeda147a8b2b4204f9f1cd38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799593"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a><span data-ttu-id="e4092-103">MAPI Url の通知に基づくインデックス作成について</span><span class="sxs-lookup"><span data-stu-id="e4092-103">About MAPI URLs for Notification-Based Indexing</span></span>

<span data-ttu-id="e4092-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4092-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4092-105">ストア プロバイダーには、オブジェクトのインデックス作成の準備が整っているインデクサーが通知された、MAPI プロトコル ハンドラー オブジェクトを一意に識別する MAPI URL が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e4092-105">When a store provider notifies an indexer that an object is ready for indexing, it generates a MAPI URL that uniquely identifies the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="e4092-106">MAPI Url、Unicode でエンコードされた、次の形式。</span><span class="sxs-lookup"><span data-stu-id="e4092-106">MAPI URLs are encoded in Unicode, and have the following format:</span></span> 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

<span data-ttu-id="e4092-107">次の表では、一般的な URL の各部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4092-107">The following table describes the various parts of a typical URL.</span></span>

|<span data-ttu-id="e4092-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="e4092-108">Part</span></span> | <span data-ttu-id="e4092-109">説明</span><span class="sxs-lookup"><span data-stu-id="e4092-109">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="e4092-110">*SID*</span><span class="sxs-lookup"><span data-stu-id="e4092-110">*SID*</span></span> |<span data-ttu-id="e4092-111">現在のユーザーのセキュリティ識別子です。</span><span class="sxs-lookup"><span data-stu-id="e4092-111">The current user's security identifier.</span></span>| 
|<span data-ttu-id="e4092-112">*StoreDisplayName*</span><span class="sxs-lookup"><span data-stu-id="e4092-112">*StoreDisplayName*</span></span> |<span data-ttu-id="e4092-113">そのストア上で、ユーザーの表示名を指定する文字列です。</span><span class="sxs-lookup"><span data-stu-id="e4092-113">A string that specifies the display name of the user on that store.</span></span>|
|<span data-ttu-id="e4092-114">*ハッシュ番号*</span><span class="sxs-lookup"><span data-stu-id="e4092-114">*HashNumber*</span></span> |<span data-ttu-id="e4092-115">計算された 16 進数表現では、 **DWORD**は、ストア エントリ ID またはストア マッピングの署名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="e4092-115">A **DWORD** in hexadecimal representation that is calculated based on the store entry ID or the store mapping signature.</span></span> <span data-ttu-id="e4092-116">この値は、レジストリに格納されているが、MAPI プロトコル ハンドラーでストアを識別するのには後で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4092-116">This value is stored in the registry and will be used later to identify the store in the MAPI Protocol Handler.</span></span><br/><br/><span data-ttu-id="e4092-117">この数値は、他のストアとの衝突を最小限に抑える方法で計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4092-117">This number must be calculated in a way that minimizes collisions with other stores.</span></span> <span data-ttu-id="e4092-118">Microsoft Outlook を使用してハッシュを計算するアルゴリズムでは、[番号を保存するハッシュを計算するアルゴリズム](algorithm-to-calculate-the-store-hash-number.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4092-118">For the algorithm that Microsoft Outlook uses to calculate the hash number, see [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).</span></span>|
|<span data-ttu-id="e4092-119">*StoreType*</span><span class="sxs-lookup"><span data-stu-id="e4092-119">*StoreType*</span></span> |<span data-ttu-id="e4092-120">インデックスを作成するオブジェクトが含まれるストアの種類を識別する番号です。</span><span class="sxs-lookup"><span data-stu-id="e4092-120">A number that identifies the type of the store that contains the object to be indexed.</span></span> <span data-ttu-id="e4092-121">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e4092-121">The possible values are as follows:</span></span><br/><span data-ttu-id="e4092-122">-0 - 既定のストアです。</span><span class="sxs-lookup"><span data-stu-id="e4092-122">- 0 - Default store.</span></span><br/><br/><span data-ttu-id="e4092-123">-代理ストアを 1 -、代理人のアイテムがローカルにキャッシュを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4092-123">- 1 - Delegate store, used for delegate items cached locally.</span></span><br/><br/><span data-ttu-id="e4092-124">-2 - パブリック フォルダー、パブリック フォルダーのお気に入りを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4092-124">- 2 - Public folders, used for public folder favorites.</span></span><br/><br/><span data-ttu-id="e4092-125">**注**: ストアは、プッシュの代わりにクロールするが、使用される値が*X*の文字です。</span><span class="sxs-lookup"><span data-stu-id="e4092-125">**NOTE**: If the store is being crawled instead of pushed, the value that is used is the character*X*.</span></span>| 
|<span data-ttu-id="e4092-126">*FolderNameA/.../FolderNameN*</span><span class="sxs-lookup"><span data-stu-id="e4092-126">*FolderNameA/…/FolderNameN*</span></span> |<span data-ttu-id="e4092-127">IPM_SUBTREE のルートからフォルダーまたはメッセージへのパスです。</span><span class="sxs-lookup"><span data-stu-id="e4092-127">The path from the root of the IPM_SUBTREE to the folder or message.</span></span> <span data-ttu-id="e4092-128">たとえば、 **[受信トレイ]** の下で [**ファミリ**] フォルダーにメッセージは、このパラメーターの**受信トレイと家族**を持っています。</span><span class="sxs-lookup"><span data-stu-id="e4092-128">For example, a message in the **Family** folder under **Inbox** has **Inbox/Family** for this parameter.</span></span> |
|<span data-ttu-id="e4092-129">*EntryIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="e4092-129">*EntryIDEncoded*</span></span> |<span data-ttu-id="e4092-130">Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="e4092-130">MAPI entry ID for the item encoded as a Unicode string.</span></span> <span data-ttu-id="e4092-131">特定の特殊文字をエンコードする方法については、次のセクション特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4092-131">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="e4092-132">エントリ ID をエンコードするためのアルゴリズムの詳細については、[アルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4092-132">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="e4092-133">**注**: ランダムのハングル文字または使用可能なフォントに応じて、アルゴリズムに準拠しているボックスに ID が表示されるエントリがこのエンコードされたテキストとして表示するときです。</span><span class="sxs-lookup"><span data-stu-id="e4092-133">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span>  |
|<span data-ttu-id="e4092-134">*AttachIDEncoded*</span><span class="sxs-lookup"><span data-stu-id="e4092-134">*AttachIDEncoded*</span></span> |<span data-ttu-id="e4092-135">Unicode 文字列としてエンコードされた添付ファイルの ID です。</span><span class="sxs-lookup"><span data-stu-id="e4092-135">Attachment ID encoded as a Unicode string.</span></span> <span data-ttu-id="e4092-136">特定の特殊文字をエンコードする方法については、次のセクション特殊文字」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4092-136">See the following section "Special Characters" for information about how certain special characters are encoded.</span></span> <span data-ttu-id="e4092-137">エントリ ID をエンコードするためのアルゴリズムの詳細については、[アルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4092-137">For more information about the algorithm to encode the entry ID, see [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).</span></span><br/><br/><span data-ttu-id="e4092-138">**注**: ランダムのハングル文字または使用可能なフォントに応じて、アルゴリズムに準拠しているボックスに ID が表示されるエントリがこのエンコードされたテキストとして表示するときです。</span><span class="sxs-lookup"><span data-stu-id="e4092-138">**NOTE**: When viewed as text, this encoded entry ID appears as random Hangul characters or boxes in compliance with the algorithm, depending on available fonts.</span></span> |
|<span data-ttu-id="e4092-139">*Filename*</span><span class="sxs-lookup"><span data-stu-id="e4092-139">*FileName*</span></span> |<span data-ttu-id="e4092-140">添付ファイルの名前、メッセージに表示されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="e4092-140">Name of the attachment file, as it appears in the message.</span></span>|
    
## <a name="examples-of-mapi-urls"></a><span data-ttu-id="e4092-141">MAPI Url の例</span><span class="sxs-lookup"><span data-stu-id="e4092-141">Examples of MAPI URLs</span></span>

<span data-ttu-id="e4092-142">MAPI Url の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e4092-142">The following are some examples of MAPI URLs.</span></span>
  
- <span data-ttu-id="e4092-143">フォルダーの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="e4092-143">MAPI URL for a folder:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- <span data-ttu-id="e4092-144">メッセージの MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="e4092-144">MAPI URL for a message:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- <span data-ttu-id="e4092-145">添付ファイルは MAPI URL:</span><span class="sxs-lookup"><span data-stu-id="e4092-145">MAPI URL for an attachment:</span></span> 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a><span data-ttu-id="e4092-146">特殊文字</span><span class="sxs-lookup"><span data-stu-id="e4092-146">Special characters</span></span>

<span data-ttu-id="e4092-147">メッセージまたは添付ファイルに含まれる場合は、特定の文字がエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="e4092-147">Certain characters are encoded if they appear in the message or attachment.</span></span> <span data-ttu-id="e4092-148">MAPI URL をエンコードする文字を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e4092-148">The following shows which characters are encoded in a MAPI URL:</span></span>
  
- <span data-ttu-id="e4092-149">% > %25</span><span class="sxs-lookup"><span data-stu-id="e4092-149">% > %25</span></span>
    
- <span data-ttu-id="e4092-150">/> %2f</span><span class="sxs-lookup"><span data-stu-id="e4092-150">/ > %2F</span></span> 
    
- <span data-ttu-id="e4092-151">\ > %5 C</span><span class="sxs-lookup"><span data-stu-id="e4092-151">\ > %5C</span></span> 
    
- <span data-ttu-id="e4092-152">\*> %2a</span><span class="sxs-lookup"><span data-stu-id="e4092-152">\* > %2A</span></span> 
    
- <span data-ttu-id="e4092-153">?</span><span class="sxs-lookup"><span data-stu-id="e4092-153"></span></span> <span data-ttu-id="e4092-154">> %3f</span><span class="sxs-lookup"><span data-stu-id="e4092-154">> %3F</span></span> 
    
## <a name="blob-associated-with-each-mapi-url"></a><span data-ttu-id="e4092-155">各 MAPI URL に関連付けられた blob</span><span class="sxs-lookup"><span data-stu-id="e4092-155">Blob associated with each MAPI URL</span></span>

<span data-ttu-id="e4092-156">オブジェクトのインデックスを作成する MAPI URL をプッシュするには、ストア プロバイダーは、MAPI プロトコル ハンドラーの特定の情報を格納するバイナリ ラージ オブジェクト (BLOB) をも作成します。</span><span class="sxs-lookup"><span data-stu-id="e4092-156">When pushing a MAPI URL for an object to be indexed, a store provider also creates a binary large object (BLOB) that contains certain information for the MAPI Protocol Handler.</span></span> <span data-ttu-id="e4092-157">ストア プロバイダーは、各 MAPI URL を使用してこの BLOB に関連付けるし、MAPI URL がインデクサーにプッシュするときに送信します。</span><span class="sxs-lookup"><span data-stu-id="e4092-157">The store provider associates this BLOB with each MAPI URL and sends it when pushing the MAPI URL to the indexer.</span></span> <span data-ttu-id="e4092-158">BLOB の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e4092-158">The format of the BLOB is as follows:</span></span> 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

<span data-ttu-id="e4092-159">ストア プロバイダーは、以下の順に BLOB をこれらの値を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4092-159">The store provider must write these values to the BLOB in the order shown.</span></span> <span data-ttu-id="e4092-160">次の表では、BLOB の各フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e4092-160">The following table describes each field of the BLOB.</span></span>

|<span data-ttu-id="e4092-161">パーツ</span><span class="sxs-lookup"><span data-stu-id="e4092-161">Part</span></span> | <span data-ttu-id="e4092-162">説明</span><span class="sxs-lookup"><span data-stu-id="e4092-162">Description</span></span>|
|:----|:-----------|  
|<span data-ttu-id="e4092-163">*dwVersion*</span><span class="sxs-lookup"><span data-stu-id="e4092-163">*dwVersion*</span></span> |<span data-ttu-id="e4092-164">これは、送信されるデータのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="e4092-164">This is the version of the data being sent.</span></span> <span data-ttu-id="e4092-165">現在、この値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="e4092-165">Currently this value is 1.</span></span>|
|<span data-ttu-id="e4092-166">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e4092-166">*dwFlags*</span></span> |<span data-ttu-id="e4092-167">将来の使用のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="e4092-167">Reserved for future use.</span></span> <span data-ttu-id="e4092-168">現在この値は 0 を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4092-168">Currently this value should be 0.</span></span>|
|<span data-ttu-id="e4092-169">*cbProfileName*</span><span class="sxs-lookup"><span data-stu-id="e4092-169">*cbProfileName*</span></span> |<span data-ttu-id="e4092-170">バイトで、プロファイル名のサイズです。</span><span class="sxs-lookup"><span data-stu-id="e4092-170">The size of the profile name, in bytes.</span></span> <span data-ttu-id="e4092-171">この情報は、MAPI プロトコル ハンドラーは、項目のインデックスを作成するときに使用するプロファイルを知っている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="e4092-171">This information is useful for the MAPI Protocol Handler to know which profile to use when indexing the item.</span></span>|
|<span data-ttu-id="e4092-172">*wszProfileName*</span><span class="sxs-lookup"><span data-stu-id="e4092-172">*wszProfileName*</span></span> |<span data-ttu-id="e4092-173">Null で終わる Unicode 文字列プロファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e4092-173">Null-terminated Unicode string that contains the profile name.</span></span>|
|<span data-ttu-id="e4092-174">*cbProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="e4092-174">*cbProviderItemID*</span></span> |<span data-ttu-id="e4092-175">プロバイダー アイテム ID のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="e4092-175">Size of the provider item ID, in bytes.</span></span> <span data-ttu-id="e4092-176">ストア プロバイダーは、この情報を取得する追加のフォルダーを開けないようにするのには、フォルダーのアイテムの ID プロバイダーのみを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4092-176">The store provider should send only the provider item ID for folders, to prevent opening additional folders to get this information.</span></span>|
|<span data-ttu-id="e4092-177">*wszProviderItemID*</span><span class="sxs-lookup"><span data-stu-id="e4092-177">*wszProviderItemID*</span></span> |<span data-ttu-id="e4092-178">Null で終わる Unicode 文字列ストア内の項目を一意に識別するプロバイダー アイテム ID を持つ。</span><span class="sxs-lookup"><span data-stu-id="e4092-178">Null-terminated Unicode string with the provider item ID that uniquely identifies the item in the store.</span></span>|
    
## <a name="see-also"></a><span data-ttu-id="e4092-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4092-179">See also</span></span>

- [<span data-ttu-id="e4092-180">ストアの通知に基づくインデックスの作成について</span><span class="sxs-lookup"><span data-stu-id="e4092-180">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="e4092-181">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="e4092-181">MAPI Constants</span></span>](mapi-constants.md)
