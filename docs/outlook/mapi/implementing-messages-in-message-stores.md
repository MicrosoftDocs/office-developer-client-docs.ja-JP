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
ms.openlocfilehash: c21fea9b0c8de96f427c4bcdfabfde3a0032f0c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800942"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="94749-103">���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B</span><span class="sxs-lookup"><span data-stu-id="94749-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="94749-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94749-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94749-105">[IMessage: IMAPIProp](imessageimapiprop.md)のようなインターフェイスでは、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)インターフェイスの両方のインターフェイスから派生する、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェース。</span><span class="sxs-lookup"><span data-stu-id="94749-105">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="94749-106">クライアントは、メッセージの内容にアクセスするための**IMAPIProp**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="94749-106">Clients use the **IMAPIProp** methods to access the contents of a message.</span></span> <span data-ttu-id="94749-107">**IMessage**インターフェイスには、メッセージ (添付ファイルを追加または、メッセージの受信者を変更するなど) を操作するための他の方法が用意されています。</span><span class="sxs-lookup"><span data-stu-id="94749-107">The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message).</span></span> <span data-ttu-id="94749-108">**IMessage**インターフェイス内のメソッドは、メッセージのプロパティに直接格納されていないメッセージの属性を変更します。</span><span class="sxs-lookup"><span data-stu-id="94749-108">The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94749-109">�֘A����</span><span class="sxs-lookup"><span data-stu-id="94749-109">See also</span></span>



<span data-ttu-id="94749-110">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="94749-110">[Message Store Features](message-store-features.md)</span></span>
