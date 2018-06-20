---
title: MAPI �A�h���X��
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b328a65f400e424fb2cd177e710fb8bcffa392c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801305"
---
# <a name="mapi-address-book"></a><span data-ttu-id="34c79-103">MAPI �A�h���X��</span><span class="sxs-lookup"><span data-stu-id="34c79-103">MAPI Address Book</span></span>

  
  
<span data-ttu-id="34c79-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34c79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34c79-105">統合アドレス帳は、すべてのプロファイルで、アドレス帳プロバイダーからのアドレス指定情報の統合のコレクションにアクセスできるようにするのには MAPI を実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="34c79-105">The integrated address book is an object that MAPI implements to provide access to an integrated collection of addressing information from all of the address book providers in the profile.</span></span> <span data-ttu-id="34c79-106">アドレス帳では、クライアント アプリケーションとサービス ・ プロバイダーはありませんメッセージング システムの一意のアドレス体系を区別します。</span><span class="sxs-lookup"><span data-stu-id="34c79-106">With the address book, client applications and service providers do not have to differentiate between the unique addressing schemes of messaging systems.</span></span> <span data-ttu-id="34c79-107">代わりに、それらを調べることのすべての受信者のアドレスですべてのメッセージング システムでは、メッセージング システムのアドレス帳プロバイダーがインストールされていれば。</span><span class="sxs-lookup"><span data-stu-id="34c79-107">Instead, they can look up the addresses of any recipients in any messaging system, as long as the address book provider for the messaging system is installed.</span></span>
  
<span data-ttu-id="34c79-108">アドレス帳は、ユーザーの介入なし、またはコモン ダイアログ ボックスを使用して対話的にプログラムでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="34c79-108">The address book can be accessed programmatically, without user intervention, or interactively through the use of common dialog boxes.</span></span> <span data-ttu-id="34c79-109">MAPI には、特定の受信者、ユーザーが一意のアドレスと新しいを作成するためのテンプレートのフォームのセットにマップすることはできませんが、受信者を作成するときに、警告に関する詳細情報、アドレス帳のエントリの要約リストを表示するダイアログ ボックスが含まれています。受信者です。</span><span class="sxs-lookup"><span data-stu-id="34c79-109">MAPI includes dialog boxes to display a summary list of the entries in the address book, detailed information about a particular recipient, a warning when a user creates a recipient that cannot be mapped to a unique address, and a set of template forms for creating new recipients.</span></span>
  
<span data-ttu-id="34c79-p103">MAPI �A�h���X���́A�K�w�\���ɂȂ��Ă��邱�ƂɃ��b�Z�[�W �X�g�A�\����Ɠ����ł��B�A�h���X���́A3 ��ނ̃A�h���X���v���o�C�_�[�ɂ���Ď����I�u�W�F�N�g�ւ̃A�N�Z�X��񋟂��܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-p103">The MAPI address book is similar in structure to a message store in that it is organized hierarchically. The address book provides access to three types of objects implemented by an address book provider:</span></span>
  
- <span data-ttu-id="34c79-112">�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="34c79-112">An address book container object.</span></span>
    
- <span data-ttu-id="34c79-113">�z�z���X�g �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="34c79-113">A distribution list object.</span></span>
    
- <span data-ttu-id="34c79-114">���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="34c79-114">A messaging user object.</span></span>
    
<span data-ttu-id="34c79-115">�A�h���X���v���o�C�_�[�ɂ���Ċ��蓖�Ă��Ă���A��ӂ̃G���g�����ʎq����ꂼ��̃I�u�W�F�N�g�̎�ނɃA�N�Z�X���܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-115">Each of these types of objects is accessed through its unique entry identifier that is assigned by its address book provider.</span></span> 
  
<span data-ttu-id="34c79-p104">���܂��܂Ȏ�ނ̃I�u�W�F�N�g��i�[���邱�ƂŁA�A�h���X���̃R���e�i�[�̓t�H���_�[�Ɏ��Ă��܂��B���̑��̃A�h���X���̃R���e�i�[�Ƃ��ă��b�Z�[�W���O ���[�U�[����єz�z���X�g�̃I�u�W�F�N�g��A�h���X���R���e�i�[��ێ��ł��܂��B�A�h���X���̃I�u�W�F�N�g��ۑ�����A�h���X���̃R���e�i�[��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-p104">Address book containers are similar to folders in that they hold objects of different types. An address book container can hold other address book containers as well as messaging user and distribution list objects. Address book containers are used to organize and store address book objects.</span></span>
  
<span data-ttu-id="34c79-119">アドレス帳の統合された外観を得るには、アドレス帳プロバイダーは、0、1、または、最上位のコンテナーにそれらを結合し、単一の最上位のコンテナーの下の結果を表示する MAPI の詳細を公開します。</span><span class="sxs-lookup"><span data-stu-id="34c79-119">To achieve the address book's integrated appearance, address book providers expose zero, one, or more of their top-level containers to MAPI which merges them and displays the results under a single top-level container.</span></span> <span data-ttu-id="34c79-120">アドレス帳プロバイダーは、セッションと別のセットを別のセッションのメッセージの 1 つの種類のコンテナーの 1 つのセットを公開するために選択できます。</span><span class="sxs-lookup"><span data-stu-id="34c79-120">Address book providers can choose to expose one set of containers for one type of messaging session and a different set for another session.</span></span> <span data-ttu-id="34c79-121">アドレス帳プロバイダーが最上位のコンテナーを持たず、受信者を作成するために使用するテンプレートの一覧のみを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="34c79-121">It is also possible for address book providers to have no top-level containers and expose only a list of templates that can be used to create recipients.</span></span>
  
<span data-ttu-id="34c79-p106">���b�Z�[�W�̃��[�U�[�Ɣz�z���X�g��̃I�u�W�F�N�g�́A���b�Z�[�W�̎�M�҂���������Ă��܂��B���b�Z�[�W�̃��[�U�[���X �̎�M�҂ł��B�z�z���X�g�́A��M�҂̃O���[�v�ł��B�e���b�Z�[�W�̃��[�U�[�́A����̃��b�Z�[�W���O �V�X�e���́A����̎�ނ̈�ӂ̃A�h���X������Ă��܂��B�z�z���X�g�́A��M�҂̖��O�t���̃R���N�V�����ł��B�z�z���X�g�ɂ́A���b�Z�[�W�̃��[�U�[ �I�u�W�F�N�g�Ƃ��̑��̔z�z���X�g��܂߂邱�Ƃ��ł��܂��B�N���C�A���g �A�v���P�[�V�����̃��[�U�[�́A�z�z���X�g�Ƀ��b�Z�[�W�𑗐M] ���b�Z�[�W�͊e���X�g�̃��b�Z�[�W�̃��[�U�[�̃����o�[�ɑ��M����邳��܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-p106">Message recipients are implemented with messaging user and distribution list objects. Messaging users are individual recipients; distribution lists are group recipients. Each messaging user has a unique address of a particular type handled by a particular messaging system. A distribution list is a named collection of recipients. Distribution lists can contain messaging user objects and other distribution lists. When a user of a client application sends a message to a distribution list, the message is being sent to each of the list's messaging user members.</span></span> 
  
<span data-ttu-id="34c79-p107">���b�Z�[�W�̃��[�U�[�Ɣz�z���X�g�̃x�[�X �A�h���X �v���p�e�B�ƌĂ΂�� 5 �̃v���p�e�B�̐ݒ肪����܂��B�����͕K�v�ȃv���p�e�B�ł���A���̂悤�ɊȒP�ɐ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-p107">Messaging users and distribution lists have a set of five properties that are known as the base address properties. These are required properties and are briefly described as follows.</span></span>
  
|<span data-ttu-id="34c79-130">**��{ address �v���p�e�B**</span><span class="sxs-lookup"><span data-stu-id="34c79-130">**Base address property**</span></span>|<span data-ttu-id="34c79-131">**���**</span><span class="sxs-lookup"><span data-stu-id="34c79-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34c79-132">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34c79-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34c79-p108">��M�҂̃A�h���X����͂��܂��B�e�A�h���X�̎�ނł́A����̌\`���Ɉˑ����āA����̃��b�Z�[�W���O �V�X�e�����g���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-p108">Type of address for the recipient. Each address type follows a particular format and is used with a particular messaging system.</span></span>  <br/> |
|<span data-ttu-id="34c79-135">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34c79-135">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34c79-136">��M�҂̖��O��\���\�Ȃł��B</span><span class="sxs-lookup"><span data-stu-id="34c79-136">Displayable name for the recipient.</span></span>  <br/> |
|<span data-ttu-id="34c79-137">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34c79-137">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34c79-138">��M�҂̃A�h���X�ł��B</span><span class="sxs-lookup"><span data-stu-id="34c79-138">Address of the recipient.</span></span>  <br/> |
|<span data-ttu-id="34c79-139">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34c79-139">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34c79-140">�G���g�����ʎq����M�҂ɃA�N�Z�X���邽�߂Ɏg�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-140">Entry identifier used to access the recipient.</span></span>  <br/> |
|<span data-ttu-id="34c79-141">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34c79-141">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34c79-142">�o�C�i�������L�[����M�҂���ʂ��邽�߂Ɏg�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-142">Binary comparable key used to identify the recipient.</span></span>  <br/> |
   
<span data-ttu-id="34c79-p109">MAPI �ł́A�����̃O���[�v�̃x�[�X �A�h���X�̃v���p�e�B�̃o���G�[�V�����̃v���p�e�B���\`���܂��B�����̑��̃O���[�v�́A���b�Z�[�W�̃��[�U�[�Ƃ��܂��܂ȏ󋵂ł̔z�z���X�g�ɂ��Đ�����܂��B���Ƃ��΁A�v���p�e�B�� 1 �̃O���[�v�ɂ́A���b�Z�[�W�⑼�̃O���[�v�̑㗝�l�̎�M�҂̑㗝�l�̑��M�҂��ɂ��Đ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="34c79-p109">MAPI defines many groups of properties that are variations of the base address properties. These other groups describe messaging users and distribution lists in different situations. For example, one group of properties describes the delegate sender of a message and another group the delegate recipient.</span></span>
  

