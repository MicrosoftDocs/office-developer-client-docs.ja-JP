---
title: �㗝�l�A�N�Z�X
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 69945bc03d9183ea18a436186523741ce534b71e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568491"
---
# <a name="delegate-access"></a><span data-ttu-id="12242-103">�㗝�l�A�N�Z�X</span><span class="sxs-lookup"><span data-stu-id="12242-103">Delegate Access</span></span>

  
  
<span data-ttu-id="12242-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12242-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12242-105">代理人アクセスは、別のユーザーとしてメッセージを送信または別のユーザーに対してメッセージが表示するユーザーのことを指します。</span><span class="sxs-lookup"><span data-stu-id="12242-105">Delegate access refers to the user's ability to send a message as another user or receive a message for another user.</span></span> <span data-ttu-id="12242-106">代理人アクセスは、mapi トランスポート プロバイダーは、選択した場合をサポートできるサービス プロバイダーに依存しない機能です。</span><span class="sxs-lookup"><span data-stu-id="12242-106">Delegate access is a service provider-independent feature of MAPI that transport providers can support if they choose.</span></span> <span data-ttu-id="12242-107">ただし、これを行うプロバイダーは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="12242-107">However, no provider is required to do so.</span></span> <span data-ttu-id="12242-108">代理人アクセスは、ユーザーとして、メッセージを送信したり、別のユーザーまたはユーザーが別のユーザーのメッセージ ストアにアクセスする必要があるときの受信メッセージをフィルター処理する必要がある場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="12242-108">Delegate access is valuable when it is necessary for a user to send messages as, or filter incoming messages for, another user or when a user must access another user's message store.</span></span> <span data-ttu-id="12242-109">他のユーザーのストアに接続するための代理ユーザーを許可する前に、メッセージ ストア プロバイダーは代理人ユーザーが適切な権限を持っているを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12242-109">Before allowing a delegate user to connect to another user's store, the message store provider must verify that the delegate user has the proper authority.</span></span> 
  
<span data-ttu-id="12242-110">�㗝�l�A�N�Z�X��T�|�[�g���邽�߂Ɏg�p����v���p�e�B�� 2 �̃O���[�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="12242-110">There are two groups of properties that are used to support delegate access:</span></span>
  
 <span data-ttu-id="12242-111">**PR_SENT_REPRESENTING_ADDRTYPE**([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS**([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-113">**PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-114">**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-115">**PR_SENT_REPRESENTING_SEARCH_KEY**([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-116">**PR_RCVD_REPRESENTING_ADDRTYPE**([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS**([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-118">**PR_RCVD_REPRESENTING_ENTRYID**([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-119">**PR_RCVD_REPRESENTING_NAME**([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="12242-120">**PR_RCVD_REPRESENTING_SEARCH_KEY**([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12242-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span></span> 
  
<span data-ttu-id="12242-121">送信メッセージは、 **PR_SENT_REPRESENTING**プロパティは、送信者として機能する必要があるメッセージングのユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="12242-121">On outgoing messages, the **PR_SENT_REPRESENTING** properties identify the messaging user that should act as the sender.</span></span> <span data-ttu-id="12242-122">クライアントは、オプションとしてこれらのプロパティを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="12242-122">Clients can set these properties as an option.</span></span> <span data-ttu-id="12242-123">時間によっては、 **PR_SENT_REPRESENTING**プロパティは設定されていない場合は、メッセージは代理人のアクセスをサポートするトランスポート プロバイダーに到達、 **PR_SENDER**のプロパティ設定を行うため、プロバイダーの責任です。</span><span class="sxs-lookup"><span data-stu-id="12242-123">If the **PR_SENT_REPRESENTING** properties are not set by the time the message reaches a transport provider that supports delegate access, it is the provider's responsibility to set them along with the **PR_SENDER** properties.</span></span> 
  
<span data-ttu-id="12242-p103">��M���b�Z�[�W�ɂ́A **PR_RCVD_REPRESENTING**�v���p�e�B�́A��M�҂Ƃ��ċ@�\����K�v������܂����[�U�[����肵�܂��B�㗝�l�̃��b�Z�[�W��z�M����ӔC�g�����X�|�[�g �v���o�C�_�[�́A **PR_RCVD_REPRESENTING**�� **PR_RECEIVED_BY**�̗����̃v���p�e�B��ݒ肷��K�v������܂��B�N���C�A���g�́A�㗝�l�̃��b�Z�[�W���M�́A�Ή����� **PR_RCVD_REPRESENTING**�v���p�e�B�� **PR_SENT_REPRESENTING**�v���p�e�B�̒l��R�s�[����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="12242-p103">On incoming messages, the **PR_RCVD_REPRESENTING** properties identify the user that should act as the recipient. Transport providers responsible for delivering delegate messages must set both the **PR_RCVD_REPRESENTING** and **PR_RECEIVED_BY** properties. Clients receiving a delegate message should copy the values of the **PR_SENT_REPRESENTING** properties to the corresponding **PR_RCVD_REPRESENTING** properties.</span></span> 
  
<span data-ttu-id="12242-p104">���Ƃ��΁A�T���[���x�ɒ��ɁAJohn �� Sally �̃��b�Z�[�W����M����Ƃ��܂��B **PR_RCVD_REPRESENTING**�v���p�e�B�́A�㗝�l�̈���Ƃ��� John ����肵�܂��BJohn Sally �̔ގ�M�������b�Z�[�W�ւ̕ԐM�𑗐M���郁�b�Z�[�W�� **PR_SENDER**�v���p�e�B�́A���o�l�Ƃ��� John ����肵�܂��BJohn Sally ��\�����A���邽�߂ɁA **PR_SENT_REPRESENTING**�v���p�e�B�� Sally ����肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="12242-p104">For example, suppose John is receiving Sally's messages while Sally is on vacation. The **PR_RCVD_REPRESENTING** properties identify John as the delegate recipient. When John sends a reply to a message that he has received for Sally, the message's **PR_SENDER** properties identify John as the sender. Because John is representing Sally, the **PR_SENT_REPRESENTING** properties identify Sally.</span></span> 
  
<span data-ttu-id="12242-131">代理人の受信メッセージを処理する必要があります**PR_SENDER**プロパティによって識別されるユーザーとしてではなく、 **PR_SENT_REPRESENTING**プロパティで識別されるメッセージングのユーザーとしてこれらのメッセージ配信通常プロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="12242-131">Transport providers handling incoming delegate messages should usually deliver these messages as the messaging user identified by the **PR_SENT_REPRESENTING** properties rather than as the user identified by the **PR_SENDER** properties.</span></span> <span data-ttu-id="12242-132">この規則の例外は、アクセス権限およびトランスポートの種類に一致する必要がある場合です。</span><span class="sxs-lookup"><span data-stu-id="12242-132">The exception to this rule is when it is necessary to match access privilege and transport types.</span></span> <span data-ttu-id="12242-133">この例では、トランスポート プロバイダーは、送信側の id を選択できます。</span><span class="sxs-lookup"><span data-stu-id="12242-133">In this case, a transport provider can choose a sending identity.</span></span> 
  
<span data-ttu-id="12242-134">**PR_SENT_REPRESENTING**プロパティが、代理人の受信メッセージに使用できる場合は、配信を処理するトランスポート プロバイダーは、これらの値は、 **PR_SENDER**の対応するプロパティの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="12242-134">If the **PR_SENT_REPRESENTING** properties are unavailable for an incoming delegate message, the transport provider handling delivery must set them, using the values of the corresponding **PR_SENDER** properties.</span></span> <span data-ttu-id="12242-135">**PR_SENT_REPRESENTING**プロパティが使用できるトランスポート プロバイダーが [代理人アクセスをサポートしていない場合は、配信の**PR_SENDER**プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="12242-135">If the **PR_SENT_REPRESENTING** properties are available but the transport provider does not support delegate access, it can use the **PR_SENDER** properties for delivery.</span></span> 
  

