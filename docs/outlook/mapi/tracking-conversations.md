---
title: ��b��Ǘ����܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 58157d597d3bb1042d6bc16ff954495a507c8333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804129"
---
# <a name="tracking-conversations"></a><span data-ttu-id="527f4-103">��b��Ǘ����܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="527f4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="527f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="527f4-p101">��b����́A���b�Z�[�W�ɑ΂���ԐM����W���Ă��܂��B�N���C�A���g�́A��b�̊Ǘ��ɖ𗧂� 2 �̃v���p�e�B��ݒ肷��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="527f4-107">**PR_CONVERSATION_TOPIC**([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="527f4-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="527f4-108">**PR_CONVERSATION_TOPIC**は、正規化されたプレフィックス文字列のない件名、メッセージの件名です。</span><span class="sxs-lookup"><span data-stu-id="527f4-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="527f4-109">メッセージの**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティの値にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="527f4-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="527f4-110">**PR_CONVERSATION_INDEX**([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="527f4-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="527f4-p103">**PR_CONVERSATION_INDEX**�ł́A����̃X���b�h��ŁA���b�Z�[�W�̈ʒu������܂��B�V�������b�Z�[�W�A�]�����ꂽ���b�Z�[�W�A�܂��͕ԐM���邩�ǂ����́A���M���b�Z�[�W���Ƃ� **PR_CONVERSATION_INDEX**��ݒ肷��ڋq�� reponsibility ���܂��B�N���C�A���g�ł́A�蓮�ł��̃v���p�e�B��ݒ肵����A [ScCreateConversationIndex](sccreateconversationindex.md)�AMAPI �ɂ���Ē񋟂���郆�[�e�B���e�B�֐���Ăяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="527f4-p104">**ScCreateConversationIndex**�ɂ́A���ׂĂ̑��M���b�Z�[�W�̃X���b�h �C���f�b�N�X�̒l����������܂��B **ScCreateConversationIndex**�w�b�_�[�̃u���b�N�̒����A0 ������ 22 �o�C�g�Ƃ��āA�C���f�b�N�X���������܂��͂��̑��̎q���e 5 �o�C�g�̒�����u���b�N���܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="527f4-116">�w�b�_�[�̃u���b�N 22 �o�C�g�A�g�݂� 3 �̕����ō\������܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="527f4-p105">1 �͗\��o�C�g�ł��B���̒l�� 1 �ł��B</span><span class="sxs-lookup"><span data-stu-id="527f4-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="527f4-119">�V�X�e���̌��݂̎����� 5 �o�C�g�́A [FILETIME](filetime.md)�\���\`���ɕϊ����܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="527f4-120">16 バイトの[GUID](guid.md)、またはグローバルに一意の識別子を保持します。</span><span class="sxs-lookup"><span data-stu-id="527f4-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="527f4-121">�e�q�u���b�N 5 �o�C�g�A���̂悤�ɕ����ō\������܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="527f4-p106">1 �r�b�g���A���݂̎����ƁA�w�b�_�[�̃u���b�N�Ɋi�[����Ă��鎞�Ԃ̍��ق�\���R�[�h���܂܂�Ă��܂��B���� 2 �ڂ� 2 �N�ԂƂ̍��� 1 �b�����ł���ꍇ�� 1 ���傫�� 56 �N�𒴂���.02 �����ł���ꍇ�́A���̃r�b�g�� 0 �ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="527f4-p107">30 �̂����ꂩ�̃r�b�g�� **FILETIME**�P�ʂŃw�b�_�[�̃u���b�N�̌��݂̎����Ǝ��Ԃ̈Ⴂ���܂܂�Ă��܂��B�ŏ��̃r�b�g�̒l�ɉ����āA2 �̕��@�̂����ꂩ��g�p���Ďq�u���b�N�̂��̕�������������܂��B���̃r�b�g�� 0 �̏ꍇ�́A��� 15 �r�b�g�Ɖ��� 18 �r�b�g **ScCreateConversationIndex**��j�����܂��B���̃r�b�g�� 1 �̏ꍇ�́A���̊֐��́A��� 10 �r�b�g�Ɖ��� 23 �r�b�g��j�����܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="527f4-127">4 �r�b�g��[GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx)Win32 �֐���Ăяo���ɂ���Đ��������A�����_���Ȕԍ����܂܂�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="527f4-128">�V�[�P���X��܂� 4 �r�b�g�̐��̓����_���Ȕԍ��̕�������擾�������܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="527f4-129">���b�Z�[�W�̃X���b�h �C���f�b�N�X��蓮�Őݒ肷��ꍇ�́A���̓_��l�����Ă��������B</span><span class="sxs-lookup"><span data-stu-id="527f4-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="527f4-130">�񓚎҂̃^�C�� �]�[���ł̑���_�𓧖��ɕێ����܂��B���n���Ԃł͂Ȃ��AUTC ������g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="527f4-131">�����傫���Ŋe�X���b�h�̃O���[�v�ɃC���f���g��ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="527f4-132">�������b�Z�[�W�̓��t�ւ̕ԐM����בւ��܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="527f4-133">�����g�s�b�N�̋��L�ɖ�肪��������ʂ̎����ɕʂ̃X���b�h��J�n���܂��B</span><span class="sxs-lookup"><span data-stu-id="527f4-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="527f4-134">メッセージは、トピック別にグループ化されるように分類された並べ替えを実装するには、最初**PR_CONVERSATION_TOPIC**と**PR_CONVERSATION_INDEX**を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="527f4-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="527f4-135">並べ替えの結果を表示するには、22 バイトの長さである会話のインデックスを持つメッセージの場合は 0 に、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="527f4-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="527f4-136">長さの 5 バイト単位ごとの 1 つで**PR_DEPTH**プロパティの値をインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="527f4-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="527f4-137">プロパティの PR_ORIGINAL グループは、会話の追跡にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="527f4-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="527f4-138">元のメッセージに返信または転送メッセージをリンクするのにはこれらのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="527f4-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="527f4-139">すべての PR_ORIGINAL プロパティは、オプションです。</span><span class="sxs-lookup"><span data-stu-id="527f4-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="527f4-140">既定値、または**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) の値にメッセージ ストア プロバイダーが使用できる場合は明示的に設定しない、たとえば、 **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md))プロパティです。</span><span class="sxs-lookup"><span data-stu-id="527f4-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="527f4-141">同様に、 **PR_ORIGINAL_AUTHOR_NAME**または**PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) が設定されていない場合は、これらのプロパティをデフォルトの**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) と**PR_ の値CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティでは、それぞれ。</span><span class="sxs-lookup"><span data-stu-id="527f4-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

