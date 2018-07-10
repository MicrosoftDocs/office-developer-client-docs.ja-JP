---
title: 受信者リストを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799878"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="f076f-103">受信者リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="f076f-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="f076f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f076f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f076f-105">受信者一覧は、各メッセージの受信者のプロパティの値の構造体の配列を含む[ADRLIST](adrlist.md)構造体など、メッセージの送信先。</span><span class="sxs-lookup"><span data-stu-id="f076f-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="f076f-106">受信者には、人間のユーザー、コンピューター、またはフォルダーを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="f076f-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="f076f-107">すべてのメッセージを送信するには、名前解決プロセスを使用された 1 つ以上の受信者が必要とする、受信者のプロパティの値の配列で、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティが含まれていることを確認するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="f076f-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="f076f-108">受信者のプロパティは、アドレス帳のプロパティとメッセージのプロパティの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="f076f-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="f076f-109">受信者のプロパティは、特定の受信者のすべてのメッセージにするか、現在のメッセージにのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="f076f-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="f076f-110">両方のメッセージ ・ ストアと、トランスポート プロバイダーは、受信者のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f076f-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="f076f-111">各受信者は、メッセージを送信する準備ができました時点でそのプロパティ値の配列にプロパティのコア セットが必要です。</span><span class="sxs-lookup"><span data-stu-id="f076f-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="f076f-112">受信者のプロパティのセットは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f076f-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="f076f-113">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f076f-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f076f-114">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f076f-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f076f-115">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f076f-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f076f-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="f076f-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="f076f-117">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f076f-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f076f-118">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f076f-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="f076f-119">受信者のアクセス、メッセージを送信して他のユーザーと比較するには、これらのプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f076f-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="f076f-120">すべてのプロパティはすぐに使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f076f-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="f076f-121">できる受信者を追加する最初のエントリの識別子を知らなくてもこのプロパティを割り当てるには、名前解決の処理に依存すること。</span><span class="sxs-lookup"><span data-stu-id="f076f-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="f076f-122">メッセージを送信する前に、いくつかの時点ですべての受信者リストに受信者が解決するかどうかを確認するのには[IAddrBook::ResolveName](iaddrbook-resolvename.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f076f-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="f076f-123">詳細については、[受信者名を解決する](resolving-a-recipient-name.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f076f-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="f076f-124">ユーザーまたは配布リストのエントリをアドレス帳コンテナー内のメッセージと、一時アドレスから、受信者の一覧を作成できます。</span><span class="sxs-lookup"><span data-stu-id="f076f-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="f076f-125">一時アドレスは、1 つのメッセージをアドレス指定のみに使用する一時的なエントリ、または個人用アドレス帳に追加するエントリとして作成される受信者です。</span><span class="sxs-lookup"><span data-stu-id="f076f-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="f076f-126">一時エントリ id とアドレスの形式は、MAPI によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="f076f-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="f076f-127">これらの形式の詳細については、 [1 回限りのアドレス](one-off-addresses.md)と[1 回限りのエントリ Id](one-off-entry-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f076f-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="f076f-128">ユーザーは、受信者のリストを作成するを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f076f-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="f076f-129">でアドレス帳のエントリです。</span><span class="sxs-lookup"><span data-stu-id="f076f-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="f076f-130">で 1 回限りのエントリです。</span><span class="sxs-lookup"><span data-stu-id="f076f-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="f076f-131">アドレス帳の受信者と一時アドレスの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="f076f-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="f076f-132">**共通のアドレス] ダイアログ ボックスを使用して受信者のリストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="f076f-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="f076f-133">[ADRPARM](adrparm.md)構造体と、 [ADRLIST](adrlist.md)構造体へのポインターを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f076f-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="f076f-134">**ADRPARM**構造体のメモリを 0 し、 **ADRLIST**のポインターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="f076f-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="f076f-135">[アドレス] ダイアログ ボックスを表示し、 **ADRPARM**構造体を作成する[IAddrBook::Address](iaddrbook-address.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f076f-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="f076f-136">[IMessage::ModifyRecipients](imessage-modifyrecipients.md)、 **ADRLIST**ポインターを渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f076f-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="f076f-137">この構造体は、各ユーザーが選択されている受信者のプロパティに含まれます。</span><span class="sxs-lookup"><span data-stu-id="f076f-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="f076f-138">**受信者の一覧をプログラムで作成するには**</span><span class="sxs-lookup"><span data-stu-id="f076f-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="f076f-139">リストに含まれる受信者ごとの 1 つの[ADRENTRY](adrentry.md)構造体を含む**ADRLIST**構造体を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f076f-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="f076f-140">各**ADRENTRY**構造体の必要なプロパティ、および**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) を保持するのに十分な大きさを確認します。</span><span class="sxs-lookup"><span data-stu-id="f076f-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="f076f-141">各受信者について、 **ADRLIST**構造体の**aEntries**メンバーのプロパティ値の配列を設定します。</span><span class="sxs-lookup"><span data-stu-id="f076f-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="f076f-142">MODRECIP_ADD フラグを設定して[IMessage::ModifyRecipients](imessage-modifyrecipients.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f076f-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    
