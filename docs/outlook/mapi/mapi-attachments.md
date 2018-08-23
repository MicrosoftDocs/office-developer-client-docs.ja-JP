---
title: MAPI �̓Y�t�t�@�C��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c6538f8fef7d8ccb87b6e6d9d2b9c68779ca8582
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801334"
---
# <a name="mapi-attachments"></a><span data-ttu-id="aac58-103">MAPI �̓Y�t�t�@�C��</span><span class="sxs-lookup"><span data-stu-id="aac58-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="aac58-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aac58-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aac58-105">いくつかのメッセージ ストア プロバイダーは、ファイル、OLE オブジェクト、メッセージ、またはバイナリ データの形式で追加情報をメッセージに関連付けるクライアントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="aac58-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="aac58-106">この追加情報は、メッセージの添付ファイルと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="aac58-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="aac58-107">添付ファイルが作成、管理し、自分のメッセージのみを使用してアクセス、ためメッセージの下位オブジェクトと見なされます。</span><span class="sxs-lookup"><span data-stu-id="aac58-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="aac58-108">エントリ識別子にアクセスするのではなく、添付ファイルの数と、添付ファイルで連続した番号の正常があります。</span><span class="sxs-lookup"><span data-stu-id="aac58-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="aac58-109">この番号は、メッセージ内ではなくとも、メッセージ ・ ストア内の添付ファイルを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="aac58-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="aac58-110">2 種類のメッセージは、添付ファイルの数が同じ別の添付ファイルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="aac58-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="aac58-111">添付ファイル番号は、メッセージが開かれていて、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティに格納されている限りにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="aac58-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="aac58-p102">���ׂẴ��b�Z�[�W�̓Y�t�t�@�C���ɂ��Ă̊T�v���ɃA�N�Z�X����ɂ́A�N���C�A���g�́A���̓Y�t�t�@�C���̃e�[�u����擾���܂��B�Y�t�t�@�C���̃e�[�u���ɂ́A�Y�t�t�@�C����Y�t�t�@�C���̐��A���R�[�h �L�[�Ȃǂɒ��ڃA�N�Z�X �N���C�A���g��g�p���Ă����񂪊܂܂�܂��B�N���C�A���g�ł̓Y�t�t�@�C���̃e�[�u����擾�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="aac58-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="aac58-p103">**IMessage::GetAttachmentTable** �𔭐M���܂��B�ڍׂɂ��ẮA [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="aac58-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="aac58-p104">**IMAPIProp::OpenProperty** �𔭐M���܂��B�ڍׂɂ��ẮA [IMAPIProp::OpenProperty](imapiprop-openproperty.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="aac58-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="aac58-119">メッセージ ストア プロバイダーは、これらの方法の両方をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aac58-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="aac58-120">**OpenProperty**のアプローチでは、呼び出し元が、プロパティ タグとして、インターフェイス識別子と**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) として IID_IMAPITable を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aac58-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="aac58-121">**PR_MESSAGE_ATTACHMENTS**は、メッセージの添付ファイル テーブルを表すテーブル オブジェクトのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="aac58-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="aac58-122">メッセージ ストア プロバイダーは、メッセージごとに**PR_MESSAGE_ATTACHMENTS**を設定し、 **IMAPIProp::GetPropList**メソッドから返されるプロパティ タグの配列に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aac58-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="aac58-123">詳細については、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aac58-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="aac58-124">**PR_MESSAGE_ATTACHMENTS**��g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="aac58-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="aac58-125">**IMAPIProp::OpenProperty** ��A�Y�t�t�@�C���܂��͎�M�҂̃e�[�u���ɃA�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="aac58-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="aac58-p106">**IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA�Y�t�t�@�C����܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B�ڍׂɂ��ẮA [IMAPIProp::CopyTo](imapiprop-copyto.md)��[IMAPIProp::CopyProps](imapiprop-copyprops.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="aac58-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="aac58-128">�q�̐����� [�Y�t�t�@�C���ɓK�p���邩��������ʐ������܂��B</span><span class="sxs-lookup"><span data-stu-id="aac58-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="aac58-129">�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="aac58-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

