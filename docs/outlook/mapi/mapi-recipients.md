---
title: MAPI ��M��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f83f3f51c8b11aececa31fa277fb799ce1ada512
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801442"
---
# <a name="mapi-recipients"></a><span data-ttu-id="907d0-103">MAPI ��M��</span><span class="sxs-lookup"><span data-stu-id="907d0-103">MAPI Recipients</span></span>

  
  
<span data-ttu-id="907d0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="907d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="907d0-p101">���ׂẴ��b�Z�[�W�𑗐M����̂ɂ́A1 �܂��͕����̈���A�܂��͈�A�̃��b�Z�[�W�̔z�M���\���v���p�e�B�����܂��B��M�҂����b�Z�[�W�̃R���e�L�X�g�ł̂ݎg�p���邽�� MAPI �̌ʂ̃I�u�W�F�N�g�̑���Ƀ��b�Z�[�W�̃I�u�W�F�N�g�ƌ��Ȃ���܂��B�N���C�A���g�ƃv���o�C�_�[ **IMessage** �C���^�[�t�F�C�X��g�p���Ď�M�҂�g�p���܂��B�ڍׂɂ��ẮA [IMessage: IMAPIProp](imessageimapiprop.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="907d0-p101">Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage : IMAPIProp](imessageimapiprop.md).</span></span>
  
<span data-ttu-id="907d0-p102">�N���C�A���g�ł́A���̎�M�҂̃e�[�u������A���b�Z�[�W�̎�M�҂��A�N�Z�X���܂��B���ׂẴ��b�Z�[�W�ɂ́A��M�҂��M�҂̂��ꂼ��ɂ��Ă̊T�v����܂ރe�[�u��������܂��B�e�[�u���Ɋ܂܂�Ă����́A���b�Z�[�W�̏�Ԃɂ���ĈقȂ�܂��B���b�Z�[�W�́A[�\�����A���̎�M�҂́A�\��� 3 ��݂̂�����܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-p102">Clients access a message's recipients through its recipient table. Every message has a recipient table that contains summary information about each of its recipients. The columns included in the table depend on the state of the message. When a message is under composition, its recipients might have only three columns in the table:</span></span>
  
- <span data-ttu-id="907d0-113">表示名、または**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="907d0-113">Display name, or **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="907d0-114">受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="907d0-114">Recipient type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="907d0-115">行識別子、または**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="907d0-115">Row identifier, or **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="907d0-116">メッセージには、名前解決の処理が行われましたが、各受信者もがエントリの識別子、または**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列です。</span><span class="sxs-lookup"><span data-stu-id="907d0-116">After the message has undergone the name resolution process, each recipient will also have an entry identifier, or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column.</span></span> <span data-ttu-id="907d0-117">メッセージが送信されると、受信者テーブルの行が 2 つ以上の列を追加します。</span><span class="sxs-lookup"><span data-stu-id="907d0-117">And when the message has been submitted, the rows in the recipient table will add two more columns:</span></span>
  
- <span data-ttu-id="907d0-118">アドレスの種類、または**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="907d0-118">Address type, or **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="907d0-119">トランスポートの役割または**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="907d0-119">Transport responsibility, or **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="907d0-120">クライアントは、その**IMessage::GetRecipientTable**メソッドまたは**IMAPIProp::OpenProperty**メソッドを呼び出すことによって、メッセージの受信者テーブルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="907d0-120">Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="907d0-121">詳細については、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)および[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="907d0-121">For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="907d0-122">メッセージ ストア プロバイダーは、これらの方法の両方をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="907d0-122">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="907d0-123">**OpenProperty**のアプローチでは、クライアントがインターフェイス識別子とプロパティ タグと**PR_MESSAGE_RECIPIENTS**として IID_IMAPITable を指定することが必要です。</span><span class="sxs-lookup"><span data-stu-id="907d0-123">The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag.</span></span> <span data-ttu-id="907d0-124">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) は、メッセージの受信者テーブルを表すテーブル オブジェクトのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="907d0-124">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) is a table object property that represents a message's recipient table.</span></span> <span data-ttu-id="907d0-125">メッセージ ストア プロバイダーは、メッセージごとに**PR_MESSAGE_RECIPIENTS**を設定し、 **IMAPIProp::GetPropList**メソッドから返されるプロパティ タグの配列に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="907d0-125">Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="907d0-126">詳細については、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="907d0-126">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
<span data-ttu-id="907d0-127">��M�҂̃e�[�u���𑀍삷����@�̏ڍׂɂ��ẮA [��M�҂̃e�[�u��](recipient-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="907d0-127">For more information about how to work with a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="907d0-128">��M�҂̃e�[�u���ɃA�N�Z�X���邽�߂Ɏg�p����Ă���A�ɉ����� **PR_MESSAGE_RECIPIENTS**��g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-128">In addition to being used to access a recipient table, **PR_MESSAGE_RECIPIENTS** can be used:</span></span> 
  
- <span data-ttu-id="907d0-p105">**IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA��M�҂�܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B���̑��̏���Q�Ƃ��Ă��������A [IMAPIProp::CopyTo](imapiprop-copyto.md)�����[IMAPIProp::CopyProps](imapiprop-copyprops.md)���܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-p105">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include recipients when copying. For more information see, [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="907d0-131">�q�̐�������M�҂ɓK�p���邩��������ʐ������܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-131">In a subobject restriction to indicate that the child restiction should apply to recipients.</span></span>
    
<span data-ttu-id="907d0-132">MAPI アドレス帳からエントリをコピーするか、新しいエントリを作成することによって、クライアントはメッセージに受信者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="907d0-132">Clients can add recipients to a message by copying entries from the MAPI address book or by creating new entries.</span></span> <span data-ttu-id="907d0-133">一時アドレスと呼ばれる、これらの新しいエントリでは、一時的に存在することがまたは変更可能なコンテナー内で永続的に保存されます。</span><span class="sxs-lookup"><span data-stu-id="907d0-133">These new entries, called one-offs, can exist temporarily or be saved permanently in a modifiable container.</span></span> <span data-ttu-id="907d0-134">受信者をアドレス帳から取得されますがある、エントリの id がアドレス帳プロバイダーに関連付けられている、1 回限りの受信者は MAPI によってフォーマットされているエントリの識別子をあります。</span><span class="sxs-lookup"><span data-stu-id="907d0-134">Whereas recipients that are taken from the address book have entry identifiers associated with their address book provider, one-off recipients have entry identifiers that are formatted by MAPI.</span></span> <span data-ttu-id="907d0-135">トランスポート プロバイダーとさまざまな種類のアドレスを持つクライアント関連の 1 回限りのエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="907d0-135">Transport providers and clients associate one-off entry identifiers with various types of addresses.</span></span> 
  
<span data-ttu-id="907d0-136">�g�����X�|�[�g �v���o�C�_�[�ʘb **IMAPISupport::CreateOneOff** ���M�̃A�h���X�� 1 �����̃G���g�����ʎq��쐬���郁�b�Z�[�W�̏ꍇ�B</span><span class="sxs-lookup"><span data-stu-id="907d0-136">Transport providers call **IMAPISupport::CreateOneOff** to create a one-off entry identifier for an address on an outgoing message when:</span></span> 
  
- <span data-ttu-id="907d0-137">�A�h���X�������Ă���Q�[�g�E�F�C���܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-137">The address belongs to a gateway.</span></span>
    
- <span data-ttu-id="907d0-138">���݂̃v���t�@�C���ŃA�h���X���v���o�C�_�[�ɂ���ẮA�A�h���X��������邱�Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="907d0-138">The address cannot be handled by an address book provider in the current profile.</span></span>
    
<span data-ttu-id="907d0-139">�ڍׂɂ��ẮA [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="907d0-139">For more information, see [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).</span></span>
  
<span data-ttu-id="907d0-140">�N���C�A���g����M�Z���ꎞ�G���g�����ʎq��쐬����̂ɂ́A **IAddrBook::CreateOneOff** ��Ăяo�����b�Z�[�W�̏ꍇ�B</span><span class="sxs-lookup"><span data-stu-id="907d0-140">Clients call **IAddrBook::CreateOneOff** to create a one-off entry identifier for an address on an incoming message when:</span></span> 
  
- <span data-ttu-id="907d0-141">�A�h���X�́A1 �����̃A�h���X�Ƃ��Đݒ肳��܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-141">The address is formatted as a one-off address.</span></span>
    
- <span data-ttu-id="907d0-142">�A�h���X�́A�C���^�[�l�b�g �A�h���X�Ƃ��Đݒ肳��܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-142">The address is formatted as an Internet address.</span></span>
    
<span data-ttu-id="907d0-143">�ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="907d0-143">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span>
  
<span data-ttu-id="907d0-144">�ڍׂɂ��ẮA1 �����̃G���g�����ʎq�ƃA�h���X�A [1 �����̃G���g�����ʎq](one-off-entry-identifiers.md)��[1 �����̃A�h���X](one-off-addresses.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="907d0-144">For more information about one-off entry identifiers and addresses, see [One-Off Entry Identifiers](one-off-entry-identifiers.md) and [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="907d0-p107">��M�҂̃v���p�e�B�́A�A�h���X���̃v���p�e�B�ƈ���̈���ɌŗL�̃v���p�e�B�̑g�ݍ��킹�ł��B���ׂĂ̎�M�҂ɂ́A�A�h���X���v���o�C�_�[�ɂ���Ċ��蓖�Ă��Ă���A�x�[�X �A�h���X �v���p�e�B������܂��B�G���g���́A���M���b�Z�[�W�̎�M�҂Ƃ��Ďg�p�����̃x�[�X �A�h���X �v���p�e�B�́A���ׂẴ��b�Z�[�W�̎�M�҂̃v���p�e�B��ێ����� **ADRLIST** �\���ɃR�s�[����܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-p107">The properties of a recipient are a combination of address book properties and properties specific to recipients. All recipients have the base address properties, assigned by address book providers. When an entry is used as a recipient for an outgoing message, the base address properties are copied to the **ADRLIST** structure that holds the properties for all of a message's recipients.</span></span> 
  
<span data-ttu-id="907d0-p108">��M�җp�ɐݒ肳��Ă��� 2 �̃v���p�e�B�́A **PR_RECIPIENT_TYPE** **PR_RESPONSIBILITY**�ł��B **PR_RECIPIENT_TYPE**�́A��M�҂��v���C�}���Acarbon copy �̗��A�u���C���h �J�[�{�� �R�s�[�A�܂��͍đ��M�����M�҂��ǂ���������܂��B�ŏ��� 3 �̎�ނ́A�ŏ��ɑ��M����郁�b�Z�[�W�̎�M�҂Ɋ��蓖�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="907d0-p108">Two properties that are set specifically for recipients are **PR_RECIPIENT_TYPE** and **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** indicates whether a recipient is a primary, carbon copy, blind carbon copy, or a resend recipient. The first three types are assigned to recipients on messages that are being sent for the first time.</span></span> 
  
<span data-ttu-id="907d0-p109">��M�҂Ƀ��b�Z�[�W���\������Ȃ��ꍇ�́A�����đ��M���悤�Ƃ��܂������A��M�҂��R�s�[����܂�����̎�ސݒ肪 MAPI_P1 ��đ��M���鈶���w�肵�܂��B�ꕔ�̎�M�҂ɂ́A���b�Z�[�W���\�������A�����̏ꍇ�A���� **PR_RECIPIENT_TYPE**�v���p�e�B�́A���b�Z�[�W��đ������Ƃ� MAPI_SUBMITTED �t���O�̓�e�ƃ}�[�N����܂��B�N���C�A���g�̓v���C�}���̎�M�҂�������邽�߂ɕK�v�Ȃ܂��́A **PR_RECIPIENT_TYPE**�����M�҂� MAPI_TO �ɐݒ肵�܂��B���̑��̂��ׂĂ̎�ނ̓I�v�V�����ł��B</span><span class="sxs-lookup"><span data-stu-id="907d0-p109">If a recipient does not receive the message and an attempt is made to resend it, the recipient is copied and its type is set to MAPI_P1 to indicate that it is a resend recipient. If only some of the recipients receive a message, their **PR_RECIPIENT_TYPE** properties are marked with the addition of the MAPI_SUBMITTED flag when the message is resent. Clients are required to handle primary recipients, or recipients with their **PR_RECIPIENT_TYPE** set to MAPI_TO. All other types are optional.</span></span> 
  
 <span data-ttu-id="907d0-155">**れない**は、トランスポート プロバイダーに受信者への送信を処理するように動作しているかどうかを示すために設定されています。</span><span class="sxs-lookup"><span data-stu-id="907d0-155">**PR_RESPONSIBILITY** is set to indicate to the transport provider whether or not it should handle sending to the recipient.</span></span> <span data-ttu-id="907d0-156">送信メッセージが送信されると、すべての受信者**れない**を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="907d0-156">When an outgoing message is first sent, all of the recipients set **PR_RESPONSIBILITY** to FALSE.</span></span> <span data-ttu-id="907d0-157">トランスポート プロバイダーは、1 つまたは複数の受信者に送信するための責任を主張とその**れない**プロパティが TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="907d0-157">As a transport provider claims responsibility for sending to one or more of the recipients, their **PR_RESPONSIBILITY** properties are set to TRUE.</span></span> 
  

