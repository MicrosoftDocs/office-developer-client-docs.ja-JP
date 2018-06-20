---
title: POP3 アカウントのメッセージのダウンロードの履歴の解析
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: このトピックでは、ダウンロードまたはそのアカウントの削除されたメッセージを特定するのには、POP3 アカウントのメッセージのダウンロードの履歴を表す POP3 の BLOB の構造について説明します。
ms.openlocfilehash: ffed3178e4e8b45f17fc335575a7febd77d40902
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799549"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a><span data-ttu-id="de539-103">POP3 アカウントのメッセージのダウンロードの履歴の解析</span><span class="sxs-lookup"><span data-stu-id="de539-103">Parsing the message download history for a POP3 account</span></span>

<span data-ttu-id="de539-104">このトピックでは、ダウンロードまたはそのアカウントの削除されたメッセージを特定するのには、POP3 アカウントのメッセージのダウンロードの履歴を表す POP3 の BLOB の構造について説明します。</span><span class="sxs-lookup"><span data-stu-id="de539-104">This topic describes the structure of the POP3 BLOB that represents the message download history of a POP3 account, to identify the messages that have been downloaded or deleted on that account.</span></span>

<span data-ttu-id="de539-105"><a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a></span><span class="sxs-lookup"><span data-stu-id="de539-105"></span></span>

## <a name="why-parse-the-message-download-history"></a><span data-ttu-id="de539-106">メッセージのダウンロードの履歴を解析する理由</span><span class="sxs-lookup"><span data-stu-id="de539-106">Why parse the message download history?</span></span>

<span data-ttu-id="de539-107">Outlook の Post Office プロトコル (POP) プロバイダーを取得し、ローカル デバイス上の新しい電子メール メッセージをダウンロードしてその後に残すかメール サーバー上のこれらの電子メール メッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="de539-107">The Post Office Protocol (POP) provider for Outlook allows users to retrieve and download new email messages on their local device, and subsequently to leave or delete these email messages on the mail server.</span></span> <span data-ttu-id="de539-108">メール クライアントは、ダウンロードする新しいメッセージをチェックし、識別し、その受信トレイの新着メッセージのみをダウンロードできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de539-108">When the mail client checks for new messages to download, it has to be able to identify and download only the new messages for that Inbox.</span></span> <span data-ttu-id="de539-109">メール クライアントは、一意の識別子 (UID)、その受信トレイに配信されたことをメッセージごとのマップを入手するのには (一意な ID を一覧表示) UIDL コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de539-109">The mail client does this by first using the UIDL (Unique ID Listing) command to obtain a map of each message that has ever been delivered to that Inbox to a unique identifier (UID).</span></span> <span data-ttu-id="de539-110">クライアントは、ダウンロードまたはそのクライアントの受信トレイで削除されたメッセージのメッセージのダウンロードの履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="de539-110">The client also gets the message download history for messages that have been downloaded or deleted for the Inbox on that client.</span></span> <span data-ttu-id="de539-111">メッセージ マップの UID とダウンロードの履歴を使用して、クライアントことができますし、メッセージを識別するそれらは存在しない新規となり、履歴からをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de539-111">Using the message UID map and download history, the client can then identify those messages that are absent from the history as new and, hence, should be downloaded.</span></span>
  
<span data-ttu-id="de539-112">受信トレイのメッセージ ダウンロードの履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="de539-112">To get the messages download history for an Inbox:</span></span>
  
- <span data-ttu-id="de539-113">POP3 アカウントのメッセージの履歴を表すバイナリ ラージ オブジェクト (BLOB) が含まれています、 [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティを検索するのには[、POP3 アカウントの履歴をダウンロードするメッセージを検索する](locating-the-message-download-history-for-a-pop3-account.md)に手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de539-113">Follow the steps in [Locating the message download history for a POP3 account](locating-the-message-download-history-for-a-pop3-account.md) to find the [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) property, which contains a binary large object (BLOB) that represents the message history for a POP3 account.</span></span> 
    
- <span data-ttu-id="de539-114">、BLOB の構造を説明し、BLOB をダウンロードまたは POP3 アカウントの受信トレイで削除されたメッセージを識別する例を示していますが、このトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de539-114">Read this topic, which describes the structure of the BLOB, and shows an example BLOB to identify messages that have been downloaded or deleted for the Inbox of the POP3 account.</span></span>

<span data-ttu-id="de539-115"><a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a></span><span class="sxs-lookup"><span data-stu-id="de539-115"></span></span>

## <a name="pop-blob-structure"></a><span data-ttu-id="de539-116">POP の BLOB の構造</span><span class="sxs-lookup"><span data-stu-id="de539-116">POP BLOB structure</span></span>

<span data-ttu-id="de539-117">POP BLOB 構造では、表 1 で説明したようは、**バージョン**および**カウント****カウント**数が null で終わるのでは、リソースのタグの後に、2 つのフィールドで始まります。</span><span class="sxs-lookup"><span data-stu-id="de539-117">The POP BLOB structure, as described in Table 1, begins with two fields, **Version** and **Count**, followed by a **Count** number of resource tags, each of which is null-terminated.</span></span> 
  
<span data-ttu-id="de539-118">**表 1 です。メッセージを表すバイナリ ラージ オブジェクトの構造は、POP3 アカウントの履歴をダウンロードします。**</span><span class="sxs-lookup"><span data-stu-id="de539-118">**Table 1. Structure of the BLOB that represents the message download history of a POP3 account**</span></span>

|<span data-ttu-id="de539-119">**BLOB のフィールド**</span><span class="sxs-lookup"><span data-stu-id="de539-119">**Field in BLOB**</span></span>|<span data-ttu-id="de539-120">**Size**</span><span class="sxs-lookup"><span data-stu-id="de539-120">**Size**</span></span>|<span data-ttu-id="de539-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="de539-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de539-122">**バージョン**</span><span class="sxs-lookup"><span data-stu-id="de539-122">**Version**</span></span> <br/> |<span data-ttu-id="de539-123">2 バイト</span><span class="sxs-lookup"><span data-stu-id="de539-123">2 bytes</span></span>  <br/> |<span data-ttu-id="de539-124">3 (**PBLOB_VERSION_NUM**) をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de539-124">Must be 3 (**PBLOB_VERSION_NUM**).</span></span>  <br/> |
|<span data-ttu-id="de539-125">**Count**</span><span class="sxs-lookup"><span data-stu-id="de539-125">**Count**</span></span> <br/> |<span data-ttu-id="de539-126">2 バイト</span><span class="sxs-lookup"><span data-stu-id="de539-126">2 bytes</span></span>  <br/> |<span data-ttu-id="de539-127">リソースの数は、この BLOB にタグ付けします。</span><span class="sxs-lookup"><span data-stu-id="de539-127">The number of resource tags in this BLOB.</span></span>  <br/> |
|<span data-ttu-id="de539-128">リソース タグ</span><span class="sxs-lookup"><span data-stu-id="de539-128">Resource tag</span></span>  <br/> |<span data-ttu-id="de539-129">可変</span><span class="sxs-lookup"><span data-stu-id="de539-129">Variable</span></span>  <br/> |<span data-ttu-id="de539-130">リソース タグのエンコードが UTF-8 文字列を 0 または null で終わる。</span><span class="sxs-lookup"><span data-stu-id="de539-130">0 or more null-terminated UTF-8 strings that encode the resource tags.</span></span> <span data-ttu-id="de539-131">Null で終わる文字列の数は、**カウント**をと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de539-131">The number of null-terminated strings must match **Count**.</span></span>  <br/> |
   
<span data-ttu-id="de539-132">各リソースのタグは、メッセージ、操作に関するいくつかの日付と時刻のメタデータに適用され、メッセージの UID をエンコードする操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="de539-132">Each resource tag specifies the operation that is applied to a message, some date-time metadata about the operation, and encodes the UID of the message.</span></span> <span data-ttu-id="de539-133">リソース タグ文字列の形式は次のように分割して表 2 の詳細については。</span><span class="sxs-lookup"><span data-stu-id="de539-133">The format of a resource tag string is broken down as follows, and is further explained in Table 2.</span></span> 
  
`Ocyyyymmddhhmmssuuu...`
  
<span data-ttu-id="de539-134">**表 2 になります。リソース タグの構造**</span><span class="sxs-lookup"><span data-stu-id="de539-134">**Table 2. Structure of a resource tag**</span></span>

|<span data-ttu-id="de539-135">**リソース タグ内のフィールド**</span><span class="sxs-lookup"><span data-stu-id="de539-135">**Field in a resource tag**</span></span>|<span data-ttu-id="de539-136">**Size**</span><span class="sxs-lookup"><span data-stu-id="de539-136">**Size**</span></span>|<span data-ttu-id="de539-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="de539-137">**Description**</span></span>|
|:-----|:-----|:-----|
| `O` <br/> |<span data-ttu-id="de539-138">1 文字</span><span class="sxs-lookup"><span data-stu-id="de539-138">1 character</span></span>  <br/> |<span data-ttu-id="de539-139">電子メール メッセージに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="de539-139">The operation performed on the email message.</span></span> <span data-ttu-id="de539-140">値である必要があります「+」、"-"、または"&amp;"、成功の取得、削除、または取得および削除の操作をそれぞれ示します。</span><span class="sxs-lookup"><span data-stu-id="de539-140">The value must be "+", "-", or "&amp;", which indicates a successful get, delete, or get-and-delete operation, respectively.</span></span>  <br/> |
| `c` <br/> |<span data-ttu-id="de539-141">1 文字</span><span class="sxs-lookup"><span data-stu-id="de539-141">1 character</span></span>  <br/> |<span data-ttu-id="de539-142">操作に関連するメッセージの内容の一部です。</span><span class="sxs-lookup"><span data-stu-id="de539-142">The part of the message content involved in the operation.</span></span> <span data-ttu-id="de539-143">値である必要があります""、"h"または"b"は、「なし」内容を指定するには、ヘッダーや本文をそれぞれ。</span><span class="sxs-lookup"><span data-stu-id="de539-143">The value must be " ", "h", or "b", which indicates the content of none, header, or body, respectively.</span></span>  <br/> |
| `yyyy` <br/> |<span data-ttu-id="de539-144">4 文字</span><span class="sxs-lookup"><span data-stu-id="de539-144">4 characters</span></span>  <br/> |<span data-ttu-id="de539-145">操作の 4 桁の年。</span><span class="sxs-lookup"><span data-stu-id="de539-145">The four-digit year of the operation.</span></span>  <br/> |
| `MM` <br/> |<span data-ttu-id="de539-146">2 文字</span><span class="sxs-lookup"><span data-stu-id="de539-146">2 characters</span></span>  <br/> |<span data-ttu-id="de539-147">操作の 2 桁の月です。</span><span class="sxs-lookup"><span data-stu-id="de539-147">The two-digit month of the operation.</span></span>  <br/> |
| `dd` <br/> |<span data-ttu-id="de539-148">2 文字</span><span class="sxs-lookup"><span data-stu-id="de539-148">2 characters</span></span>  <br/> |<span data-ttu-id="de539-149">操作の 2 桁の日です。</span><span class="sxs-lookup"><span data-stu-id="de539-149">The two-digit day of the operation.</span></span>  <br/> |
| `hh` <br/> |<span data-ttu-id="de539-150">2 文字</span><span class="sxs-lookup"><span data-stu-id="de539-150">2 characters</span></span>  <br/> |<span data-ttu-id="de539-151">操作の 2 桁の時間。</span><span class="sxs-lookup"><span data-stu-id="de539-151">The two-digit hour of the operation.</span></span>  <br/> |
| `mm` <br/> |<span data-ttu-id="de539-152">2 文字</span><span class="sxs-lookup"><span data-stu-id="de539-152">2 characters</span></span>  <br/> |<span data-ttu-id="de539-153">操作の 2 桁の分。</span><span class="sxs-lookup"><span data-stu-id="de539-153">The two-digit minute of the operation.</span></span>  <br/> |
| `ss` <br/> |<span data-ttu-id="de539-154">2 文字</span><span class="sxs-lookup"><span data-stu-id="de539-154">2 characters</span></span>  <br/> |<span data-ttu-id="de539-155">2 桁の 2 番目の操作です。</span><span class="sxs-lookup"><span data-stu-id="de539-155">The two-digit second of the operation.</span></span>  <br/> |
| `uuu…` <br/> |<span data-ttu-id="de539-156">可変長</span><span class="sxs-lookup"><span data-stu-id="de539-156">Variable length</span></span>  <br/> |<span data-ttu-id="de539-157">エンコードされたメッセージの UID です。</span><span class="sxs-lookup"><span data-stu-id="de539-157">The encoded UID of a message.</span></span>  <br/> |

<span data-ttu-id="de539-158"><a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="de539-158"></span></span>

## <a name="example"></a><span data-ttu-id="de539-159">例</span><span class="sxs-lookup"><span data-stu-id="de539-159">Example</span></span>

<span data-ttu-id="de539-160">図 1 では、POP アカウントのメッセージのダウンロードの履歴を表すバイナリ ラージ オブジェクトの例を示します。</span><span class="sxs-lookup"><span data-stu-id="de539-160">Figure 1 shows an example of a BLOB that represents the message download history of a POP account.</span></span> 
  
<span data-ttu-id="de539-161">**図 1 です。メッセージの BLOB の構造の例は、POP3 アカウントの履歴をダウンロードします。**</span><span class="sxs-lookup"><span data-stu-id="de539-161">**Figure 1. Example BLOB structure for the message download history of a POP3 account**</span></span>

![POP3 アカウントのメッセージ ダウンロード履歴の BLOB](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
<span data-ttu-id="de539-163">表 1 と表 2 に記載されている構造に基づき、この BLOB は、23 の電子メール メッセージのダウンロードの履歴を表します。</span><span class="sxs-lookup"><span data-stu-id="de539-163">Based on the structure described in Table 1 and Table 2, this BLOB represents the download history of 23 email messages.</span></span>
  
<span data-ttu-id="de539-164">生の UID で各リソースのタグを解析するには、このエンコーディングを UID が続くことに注意してください: UID の文字は、ほとんどの英数字、および各英数字以外の文字が前に、ASCII 文字「$」(0x24)。</span><span class="sxs-lookup"><span data-stu-id="de539-164">To parse the raw UID in each resource tag, be aware that the UID follows this encoding: characters in a UID are mostly alphanumeric characters, and each non-alphanumeric character is preceded by the ASCII character "$" (0x24).</span></span> <span data-ttu-id="de539-165">ASCII 文字 $ 2 d は、英数字以外の文字を使用するように"-"です。</span><span class="sxs-lookup"><span data-stu-id="de539-165">So the ASCII characters $2d represent the non-alphanumeric character "-".</span></span> <span data-ttu-id="de539-166">リソース タグ 1 で生の UID を対応する ASCII 文字に変換する最初の前に実際の UID を生成するには、「$」、英数字以外の文字に変換する例を図 2 に示します。</span><span class="sxs-lookup"><span data-stu-id="de539-166">Figure 2 shows an example of first converting the raw UID in resource tag 1 to the ASCII representation, then converting any non-alphanumeric character preceded by "$" to produce the actual UID:</span></span>
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
<span data-ttu-id="de539-167">**図 2 になります。リソース タグで生の UID を実際のメッセージの UID に変換します。**</span><span class="sxs-lookup"><span data-stu-id="de539-167">**Figure 2. Converting the raw UID in a resource tag to the actual message UID**</span></span>

![BLOB の生の UID から実際のメッセージ UID への変換](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
<span data-ttu-id="de539-169">この BLOB のリソース タグ 1 を解釈する: メッセージの UID を持つ`0BC535DB-EA63-11E1-A75C-00215AD7BB74`13時 11分: 38 で、2012 年 9 月 6 日に正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="de539-169">To interpret resource tag 1 in this BLOB: the message with the UID  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` was successfully retrieved on September 6, 2012, at 13:11:38.</span></span> 
  
<span data-ttu-id="de539-170">22 リソースの残りのタグは、その BLOB を同様に解析できます。</span><span class="sxs-lookup"><span data-stu-id="de539-170">You can similarly parse the remaining 22 resource tags for that BLOB.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de539-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="de539-171">See also</span></span>
<span data-ttu-id="de539-172"><a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a></span><span class="sxs-lookup"><span data-stu-id="de539-172"></span></span>

- [<span data-ttu-id="de539-173">管理メッセージは、POP3 アカウントのダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="de539-173">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)    
- [<span data-ttu-id="de539-174">POP3 アカウントのメッセージのダウンロードの履歴を検索します。</span><span class="sxs-lookup"><span data-stu-id="de539-174">Locating the message download history for a POP3 account</span></span>](locating-the-message-download-history-for-a-pop3-account.md)    
- [<span data-ttu-id="de539-175">POP3 UIDL 履歴の解析</span><span class="sxs-lookup"><span data-stu-id="de539-175">Parsing the POP3 UIDL History</span></span>](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

