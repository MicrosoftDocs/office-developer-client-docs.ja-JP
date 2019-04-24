---
title: ���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 223dfa2ac990875e98e876ab491bf09caf63e874
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310095"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="9da6c-103">���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B</span><span class="sxs-lookup"><span data-stu-id="9da6c-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="9da6c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9da6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9da6c-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span><span class="sxs-lookup"><span data-stu-id="9da6c-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9da6c-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="9da6c-109">See also</span></span>



<span data-ttu-id="9da6c-110">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="9da6c-110">[Message Store Features](message-store-features.md)</span></span>

