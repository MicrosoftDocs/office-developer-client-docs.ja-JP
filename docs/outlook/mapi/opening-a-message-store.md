---
title: メッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 39d6df6db329abf7509f816165341ea0eda8331b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801672"
---
# <a name="opening-a-message-store"></a><span data-ttu-id="49ae1-103">メッセージ ストアを開く</span><span class="sxs-lookup"><span data-stu-id="49ae1-103">Opening a message store</span></span>

<span data-ttu-id="49ae1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49ae1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49ae1-105">プロファイルによっては、クライアントは、通常のセッション中に 1 つまたは複数のメッセージ ストアを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="49ae1-105">Depending on the profile, a client will need to open one or more message stores during a typical session.</span></span> <span data-ttu-id="49ae1-106">ポインターへのアクセスは、メッセージ ストアを開く、 [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)の実装です。</span><span class="sxs-lookup"><span data-stu-id="49ae1-106">Opening a message store means gaining access to a pointer to its [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implementation.</span></span> <span data-ttu-id="49ae1-107">**IMsgStore**インターフェイスは、通知、フォルダーの割り当て、およびフォルダーやメッセージにアクセスするためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-107">The **IMsgStore** interface provides methods for notification, making folder assignments, and accessing folders and messages.</span></span> 
  
<span data-ttu-id="49ae1-108">クライアントは、プロファイルが変更されている場合、ログオン時のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="49ae1-108">Clients open message stores at logon and when a profile is being modified.</span></span> <span data-ttu-id="49ae1-109">クライアントは、アクティブなセッション中に、メッセージ ・ ストアをプロファイルに追加するユーザーを許可している場合にすぐに開くか、次のセッションまでそれらを無視します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-109">If your client allows users to add message stores to the profile during an active session, you can either open them immediately or ignore them until the next session.</span></span> <span data-ttu-id="49ae1-110">メッセージ ストアのテーブル上の通知の登録、新しいメッセージ ストアの可用性に警告表示されます。</span><span class="sxs-lookup"><span data-stu-id="49ae1-110">By registering for notifications on the message store table, you will be alerted to the availability of a new message store.</span></span>
  
<span data-ttu-id="49ae1-111">メッセージ ストアを開くには、エントリ id を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49ae1-111">To open a message store, you must have its entry identifier available.</span></span> <span data-ttu-id="49ae1-112">ほとんどのクライアントはアクセスを開くには、メッセージ ストアのテーブルを使用するメッセージ ・ ストアのエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="49ae1-112">Most clients access the entry identifiers for the message stores they wish to open through the message store table.</span></span> <span data-ttu-id="49ae1-113">ただし、いくつかのメッセージは、クライアントがメッセージ ストアのテーブルをバイパスし、必要なエントリの識別子を作成するようにして、そのエントリ id の形式のドキュメントを格納します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-113">However, some message stores document the format of their entry identifiers, thereby enabling clients to bypass the message store table and construct the necessary entry identifier.</span></span> <span data-ttu-id="49ae1-114">[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)に直接このエントリの識別子を渡すことができ、MAPI 自動的にプロファイル プロバイダーの作成、メッセージ サービスに関連付けることのないです。</span><span class="sxs-lookup"><span data-stu-id="49ae1-114">They can pass this entry identifier directly to [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) and MAPI automatically creates a profile section for the provider without associating it with any message service.</span></span> 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a><span data-ttu-id="49ae1-115">メッセージ ストアのテーブルからエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-115">Retrieve an entry identifier from the message store table</span></span>
  
1. <span data-ttu-id="49ae1-116">メッセージ ストアのテーブルを開くには、 [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-116">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table.</span></span> 
    
2. <span data-ttu-id="49ae1-117">次の列を含む列の小さなセットにテーブルを制限するのには**IMAPITable::SetColumns**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-117">Call **IMAPITable::SetColumns** to limit the table to a small column set that includes the following columns:</span></span> 
    
   - <span data-ttu-id="49ae1-118">**PR_PROVIDER_DISPLAY**または**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="49ae1-118">**PR_PROVIDER_DISPLAY** or **PR_DISPLAY_NAME**</span></span>
   - <span data-ttu-id="49ae1-119">**PR_ENTRYID**プロパティ</span><span class="sxs-lookup"><span data-stu-id="49ae1-119">**PR_ENTRYID** properties</span></span> 
   - <span data-ttu-id="49ae1-120">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="49ae1-120">**PR_MDB_PROVIDER**</span></span>
   - <span data-ttu-id="49ae1-121">**PR_RESOURCE_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="49ae1-121">**PR_RESOURCE_FLAGS**</span></span>
    
3. <span data-ttu-id="49ae1-122">メッセージ ・ ストアを開くことを表す行を除外する制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-122">Build a restriction to filter out the row that represents the message store to be opened.</span></span> <span data-ttu-id="49ae1-123">既定のメッセージ ストアの検索に関する詳細については、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49ae1-123">For more information about looking for the default message store, see [Opening the Default Message Store](opening-the-default-message-store.md).</span></span> <span data-ttu-id="49ae1-124">メッセージ ストアの名前で検索するには、プロパティの制限を次のいずれかを適用します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-124">To look for a message store by name, apply any of the following property restrictions:</span></span>
    
   - <span data-ttu-id="49ae1-125">メッセージ ・ ストアのこのタイプの一般名と**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) に一致します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-125">Match **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) with the general name for this type of message store.</span></span> <span data-ttu-id="49ae1-126">たとえば、「個人用フォルダー」に PR_PROVIDER_DISPLAY を設定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="49ae1-126">For example, PR_PROVIDER_DISPLAY might be set to "Personal Folders".</span></span>
    
   - <span data-ttu-id="49ae1-127">メッセージ ・ ストアのこのタイプの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) とは、特定の**MAPIUID**に一致します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-127">Match **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) with the specific **MAPIUID** for this type of message store.</span></span> 
    
   - <span data-ttu-id="49ae1-128">この特定のメッセージ ストアの名前と**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-128">Match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name for this particular message store.</span></span> <span data-ttu-id="49ae1-129">「マイ メッセージ 2010 の会計年度」に**PR_DISPLAY_NAME**を設定する可能性があります、</span><span class="sxs-lookup"><span data-stu-id="49ae1-129">For example, **PR_DISPLAY_NAME** might be set to "My Messages for Fiscal Year 2010."</span></span> 
    
4. <span data-ttu-id="49ae1-130">メッセージ ストアのテーブルから適切な行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-130">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve the appropriate row from the message store table.</span></span> <span data-ttu-id="49ae1-131">行のエントリの識別子は、 _pprows_パラメーターで指定された行セットの**aRow**メンバーのプロパティ値の配列に含まれます。</span><span class="sxs-lookup"><span data-stu-id="49ae1-131">The entry identifier for the row will be included in the property value array for the **aRow** member of the row set pointed to by the  _pprows_ parameter.</span></span> 
    
5. <span data-ttu-id="49ae1-132">_Pprows_で指定された行セットを解放するために[FreeProws](freeprows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-132">Call [FreeProws](freeprows.md) to free the row set pointed to by  _pprows_.</span></span>
    
6. <span data-ttu-id="49ae1-133">リリース、**リ ス**のメソッドを呼び出してメッセージ ストアのテーブルです。</span><span class="sxs-lookup"><span data-stu-id="49ae1-133">Release the message store table by calling its **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="49ae1-134">メッセージ ・ ストアを開くためのカスタムのエントリ id を作成した場合は、標準的なエントリの識別子に変換する[WrapStoreEntryID](wrapstoreentryid.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-134">If you have created a custom entry identifier for the message store to be opened, call the [WrapStoreEntryID](wrapstoreentryid.md) function to convert it to a standard entry identifier.</span></span> 
  
<span data-ttu-id="49ae1-135">メッセージ ストアのエントリの識別子がある場合は後、を開くには、次の方法のいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-135">After you have a message store's entry identifier, call one of the following methods to open it:</span></span>
  
- [<span data-ttu-id="49ae1-136">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="49ae1-136">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
- [<span data-ttu-id="49ae1-137">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="49ae1-137">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
<span data-ttu-id="49ae1-138">**OpenMsgStore**は、さまざまなメッセージ ・ ストア用の特別なオプションを指定する必要がある場合に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-138">Call **OpenMsgStore** if you need to specify a variety of special options for the message store.</span></span> <span data-ttu-id="49ae1-139">**OpenMsgStore** ] ダイアログ ボックスの表示を抑制するには、一時的、または、アクセス レベルの設定、メッセージングのストアとしては、メッセージ ・ ストアを識別し、エラーを保留にできます。</span><span class="sxs-lookup"><span data-stu-id="49ae1-139">**OpenMsgStore** allows you to suppress the display of dialog boxes, identify the message store as temporary or as a nonmessaging store, set access levels, and to defer errors.</span></span> <span data-ttu-id="49ae1-140">**OpenEntry**では、アクセス レベルを設定し、エラーを遅らせることができます。</span><span class="sxs-lookup"><span data-stu-id="49ae1-140">**OpenEntry** allows you only to set access levels and defer errors.</span></span> 
  
<span data-ttu-id="49ae1-141">MDB_NO_MAIL を設定するフラグを示します MAPI にない送信または受信メッセージのメッセージ ・ ストアを使用すること。</span><span class="sxs-lookup"><span data-stu-id="49ae1-141">Setting the MDB_NO_MAIL flag indicates to MAPI that the message store will not be used for sending or receiving messages.</span></span> <span data-ttu-id="49ae1-142">MAPI には、このメッセージ ・ ストアの存在についての MAPI スプーラー通知しません。</span><span class="sxs-lookup"><span data-stu-id="49ae1-142">MAPI does not inform the MAPI spooler about the existence of this message store.</span></span> <span data-ttu-id="49ae1-143">MDB_TEMPORARY フラグは、永続的な情報を格納する使用することはできませんという意味と、一時的なメッセージ ・ ストアを指定します。</span><span class="sxs-lookup"><span data-stu-id="49ae1-143">The MDB_TEMPORARY flag designates a message store as temporary, implying that it cannot be used to store permanent information.</span></span> <span data-ttu-id="49ae1-144">一時的なメッセージ ・ ストアは、メッセージ ストアの表には表示されません。</span><span class="sxs-lookup"><span data-stu-id="49ae1-144">Temporary message stores do not appear in the message store table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49ae1-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="49ae1-145">See also</span></span>

- [<span data-ttu-id="49ae1-146">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="49ae1-146">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
