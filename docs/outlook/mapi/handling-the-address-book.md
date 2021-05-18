---
title: アドレス帳の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 464549732562a4a02d081dc5a4c5e573e38cbbce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413921"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="13aaa-103">アドレス帳の処理</span><span class="sxs-lookup"><span data-stu-id="13aaa-103">Handling the address book</span></span>
  
<span data-ttu-id="13aaa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13aaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13aaa-105">MAPI �A�h���X�����������ɂ́A�Z������Q�Ƃ��āA�ύX�����] �Ƀ��b�Z�[�W�̎�M�҂��M�҂̃v���p�e�B��ύX����ꎞ�A�h���X] ��쐬���āA1 �ȏ�̋��ʂ̃A�h���X] �_�C�A���O �{�b�N�X���\�����ꂽ���b�Z�[�W�̃��[�U�[�܂��͔z�z���X�g��ǉ�����Ƃ��Ďg�p����G���g���𒊏o����܂߂邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="13aaa-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="13aaa-106">[アドレス帳を開く](opening-the-address-book.md): MAPI を使用してアドレス帳を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="13aaa-107">[[共通アドレス] ダイアログ ボックスの表示](displaying-the-common-address-dialog-box.md): さまざまなアドレス帳コンテナーを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="13aaa-108">[アドレス帳コンテナーを開く](opening-an-address-book-container.md): さまざまなアドレス帳コンテナーを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="13aaa-109">[[アドレス帳のオプションの](setting-address-book-options.md)設定] : アドレス帳を使用するためのオプションを記述するプロパティを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="13aaa-110">[受信者の作成](creating-a-recipient.md): メッセージにアドレス指定し、変更可能なアドレス帳コンテナーにエントリを追加するときに受信者を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="13aaa-111">[配布リストの作成](creating-a-distribution-list.md): 変更可能なコンテナーに配布リストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="13aaa-112">[受信者のコピー](copying-a-recipient.md): あるコンテナーから別のコンテナーまたは同じコンテナーに受信者をコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="13aaa-113">[受信者の削除](deleting-a-recipient.md): 変更可能なコンテナーから 1 つ以上のアドレス帳エントリを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="13aaa-114">[受信者の準備](preparing-a-recipient.md): 短期的なエントリ識別子を長期エントリ識別子に変換し、プロパティを追加、変更、または並べ替えることによって受信者を準備する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="13aaa-115">[配布リストのメンバーへのアクセス](accessing-the-members-of-a-distribution-list.md): 配布リストのメンバーにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="13aaa-116">[受信者プロパティの取得](retrieving-recipient-properties.md): 受信者アドレス帳エントリの 1 つ以上のプロパティにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="13aaa-117">[アドレス帳の検索](searching-the-address-book.md): MAPI 検索機能の 2 つのレベルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="13aaa-118">[[高度な検索] ダイアログ ボックスの使用](using-an-advanced-search-dialog-box.md): アドレス帳コンテナーで高度な検索機能を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="13aaa-119">[受信者名の解決](resolving-a-recipient-name.md): アドレス帳の名前を解決する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="13aaa-120">[[配布リストの展開](expanding-distribution-lists.md)]: 配布リストを展開するように MAPI に求める方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13aaa-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

