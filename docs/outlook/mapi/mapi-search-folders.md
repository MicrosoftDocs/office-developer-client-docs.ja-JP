---
title: MAPI �����t�H���_�[
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400902"
---
# <a name="mapi-search-folders"></a><span data-ttu-id="96d99-103">MAPI �����t�H���_�[</span><span class="sxs-lookup"><span data-stu-id="96d99-103">MAPI Search Folders</span></span>

  
  
<span data-ttu-id="96d99-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96d99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96d99-p101">�������ʂ̃t�H���[�[�ł́A���ۂ̃��b�Z�[�W�ł͂Ȃ��A��ʓI�ȃt�H���](imapifolder-createfolder.md)�[��̃��b�Z�[�W�ւ̃����N��ێ����܂��B�N���C�A���g�ł́A  _ulFolderType_�p�����[�^�[�Ƃ��� FOLDER_SEARCH [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)���\�b�h��g�p���Č������ʂ̃t�H���[�[��쐬���܂��B�N���C�A���g�̃Z�b�g�A�b�v�ƌ��������K�p���āA�������ʂ̃t�H���](imapicontainer-setsearchcriteria.md)�[����͂���: ���[�������̓���������郁�b�Z�[�W��t�B���^�[�������܂��B���������[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)���\�b�h��g�p���ăZ�b�g�A�b�v���܂��B�N���C�A���g�ł́A���������K�p���āA [SetSearchCriteria](srestriction.md)�ɓn����\�� 1 �܂��͕�����**SRestriction**�\����쐬���܂��B **SetSearchCriteria**������h���C��������t�H���_�[�̈ꗗ����уZ�b�g��w�肷��t���O�̌�������s������@�𐧌䂵�܂��B</span><span class="sxs-lookup"><span data-stu-id="96d99-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria — rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span></span> 
  
 <span data-ttu-id="96d99-111">**SetSearchCriteria**は、指定した制限に一致するメッセージを識別します。</span><span class="sxs-lookup"><span data-stu-id="96d99-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span></span> <span data-ttu-id="96d99-112">選択したメッセージ (条件を満たすもの) は、検索結果フォルダー内のリンクとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="96d99-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span></span> <span data-ttu-id="96d99-113">クライアントは、検索結果フォルダーの内容にアクセスするのには[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出して、テーブルで選択したメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96d99-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span></span> <span data-ttu-id="96d99-114">検索結果フォルダーの内容のテーブルには、汎用フォルダーの内容のテーブルと同じ列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="96d99-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span></span> <span data-ttu-id="96d99-115">ただし、 **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) のプロパティは、検索結果フォルダーの場合は、リンクされているメッセージが格納されているフォルダーのエントリ id を指定します。</span><span class="sxs-lookup"><span data-stu-id="96d99-115">However, for search-results folders, the **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property specifies the entry identifier of the folder where the linked message resides.</span></span> <span data-ttu-id="96d99-116">検索結果フォルダーは、親フォルダーとは見なされません。</span><span class="sxs-lookup"><span data-stu-id="96d99-116">Search-results folders are not considered parent folders.</span></span>
  
<span data-ttu-id="96d99-117">�t�H���_�[�̌������ʂł́A���̐�������������܂��B</span><span class="sxs-lookup"><span data-stu-id="96d99-117">Search-results folders have the following limits:</span></span>
  
- <span data-ttu-id="96d99-118">**SetSearchCriteria**を呼び出すことによっては、検索結果フォルダーの内容を変更できることを唯一の方法です。</span><span class="sxs-lookup"><span data-stu-id="96d99-118">The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**.</span></span> <span data-ttu-id="96d99-119">**SetSearchCriteria**の実装の詳細については、サポート技術情報 279095 を参照してください[260322: どのようにする検索フォルダーの SetSearchCriteria メソッドを使用して](https://go.microsoft.com/fwlink/?LinkId=123603)。</span><span class="sxs-lookup"><span data-stu-id="96d99-119">For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](https://go.microsoft.com/fwlink/?LinkId=123603).</span></span>
    
- <span data-ttu-id="96d99-120">���b�Z�[�W��ړ��܂��͌������ʂ̃t�H���_�[�ɃR�s�[���邱�Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="96d99-120">Messages cannot be moved or copied into search-results folders.</span></span>
    
- <span data-ttu-id="96d99-121">検索結果フォルダーのサブフォルダーを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="96d99-121">Search-results folders cannot contain subfolders.</span></span> 
    
- <span data-ttu-id="96d99-122">�N���C�A���g�ł́A�����̌�����������ʂ̃t�H���_�[��s�����Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="96d99-122">Clients cannot make a search-results folder the subject of a search.</span></span>
    
<span data-ttu-id="96d99-123">ただし、検索結果フォルダーのプロパティを変更して、メッセージを削除することです。</span><span class="sxs-lookup"><span data-stu-id="96d99-123">It is possible, however, to modify the properties of a search-results folder and use it to delete a message.</span></span> <span data-ttu-id="96d99-124">検索結果のフォルダーからメッセージが削除されると、実際には実際のフォルダーから削除されます。</span><span class="sxs-lookup"><span data-stu-id="96d99-124">When a message is deleted from a search-results folder, it is actually deleted from the real folder.</span></span> <span data-ttu-id="96d99-125">ただし、検索結果フォルダー自体を削除するのには影響しません; 中のメッセージ一般的なフォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="96d99-125">However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96d99-126">�֘A����</span><span class="sxs-lookup"><span data-stu-id="96d99-126">See also</span></span>



<span data-ttu-id="96d99-127">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="96d99-127">[MAPI Folders](mapi-folders.md)</span></span>

