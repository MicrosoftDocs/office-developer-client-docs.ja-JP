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
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417834"
---
# <a name="mapi-attachments"></a><span data-ttu-id="4c440-103">MAPI �̓Y�t�t�@�C��</span><span class="sxs-lookup"><span data-stu-id="4c440-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="4c440-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c440-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c440-105">一部のメッセージ ストア プロバイダーでは、クライアントが追加された情報をファイル、OLE オブジェクト、メッセージ、またはバイナリ データの形式でメッセージに関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="4c440-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="4c440-106">この追加された情報は、メッセージの添付ファイルと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="4c440-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="4c440-107">添付ファイルはメッセージを通じてのみ作成、管理、およびアクセスされるので、メッセージ サブオブジェクトと見なされます。</span><span class="sxs-lookup"><span data-stu-id="4c440-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="4c440-108">添付ファイルは、アクセス用のエントリ識別子を持つのではなく、添付ファイル番号と呼ばれる連続した番号を持つ。</span><span class="sxs-lookup"><span data-stu-id="4c440-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="4c440-109">この番号は、メッセージ内の添付ファイルを一意に識別しますが、必ずしもメッセージ ストア内ではありません。</span><span class="sxs-lookup"><span data-stu-id="4c440-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="4c440-110">2 つの異なるメッセージには、同じ添付ファイル番号を持つ異なる添付ファイルを含めできます。</span><span class="sxs-lookup"><span data-stu-id="4c440-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="4c440-111">添付ファイル番号は、メッセージが開いている限り有効で、PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="4c440-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="4c440-p102">���ׂẴ��b�Z�[�W�̓Y�t�t�@�C���ɂ��Ă̊T�v���ɃA�N�Z�X����ɂ́A�N���C�A���g�́A���̓Y�t�t�@�C���̃e�[�u����擾���܂��B�Y�t�t�@�C���̃e�[�u���ɂ́A�Y�t�t�@�C����Y�t�t�@�C���̐��A���R�[�h �L�[�Ȃǂɒ��ڃA�N�Z�X �N���C�A���g��g�p���Ă����񂪊܂܂�܂��B�N���C�A���g�ł̓Y�t�t�@�C���̃e�[�u����擾�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="4c440-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="4c440-p103">**IMessage::GetAttachmentTable** �𔭐M���܂��B�ڍׂɂ��ẮA [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4c440-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="4c440-p104">**IMAPIProp::OpenProperty** �𔭐M���܂��B�ڍׂɂ��ẮA [IMAPIProp::OpenProperty](imapiprop-openproperty.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4c440-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="4c440-119">Message store providers are expected to support both of these approaches.</span><span class="sxs-lookup"><span data-stu-id="4c440-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="4c440-120">**OpenProperty** アプローチでは、呼び出し元が IID_IMAPITable をインターフェイス識別子として **、PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) をプロパティ タグとして指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c440-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="4c440-121">**PR_MESSAGE_ATTACHMENTS** は、メッセージの添付ファイル テーブルを表すテーブル オブジェクト プロパティです。</span><span class="sxs-lookup"><span data-stu-id="4c440-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="4c440-122">メッセージ ストア プロバイダーは、各メッセージPR_MESSAGE_ATTACHMENTSを設定し **、IMAPIProp::GetPropList** メソッドから返されるプロパティ タグの配列に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c440-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="4c440-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span><span class="sxs-lookup"><span data-stu-id="4c440-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="4c440-124">**PR_MESSAGE_ATTACHMENTS**��g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="4c440-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="4c440-125">**IMAPIProp::OpenProperty** ��A�Y�t�t�@�C���܂��͎�M�҂̃e�[�u���ɃA�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="4c440-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="4c440-p106">**IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA�Y�t�t�@�C����܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B�ڍׂɂ��ẮA [IMAPIProp::CopyTo](imapiprop-copyto.md)��[IMAPIProp::CopyProps](imapiprop-copyprops.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4c440-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="4c440-128">�q�̐����� [�Y�t�t�@�C���ɓK�p���邩��������ʐ������܂��B</span><span class="sxs-lookup"><span data-stu-id="4c440-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="4c440-129">�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4c440-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

