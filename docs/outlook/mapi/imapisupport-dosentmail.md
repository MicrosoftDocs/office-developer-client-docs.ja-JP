---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423952"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="6a624-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="6a624-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="6a624-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a624-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a624-105">���M���ꂽ���b�Z�[�W��������܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="6a624-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a624-106">Parameters</span></span>

 <span data-ttu-id="6a624-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a624-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6a624-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6a624-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="6a624-109">_lpMessage_</span></span>
  
> <span data-ttu-id="6a624-110">[����]�|�C���^�[��J���Ă��郁�b�Z�[�W�𑗐M�ς݃A�C�e����ۗ��Ɏw�肳��Ă���t�H���_�[�Ƀ��b�Z�[�W�𐶐�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a624-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a624-111">Return value</span></span>

<span data-ttu-id="6a624-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a624-112">S_OK</span></span> 
  
> <span data-ttu-id="6a624-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a624-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6a624-114">Remarks</span></span>

<span data-ttu-id="6a624-115">**IMAPISupport::D oSentMail** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="6a624-115">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="6a624-116">メッセージ ストア プロバイダーは、メッセージの処理が完了すると MAPI スプーラーによって呼び出される [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)メソッドの実装から **DoSentMail** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6a624-116">Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message.</span></span> <span data-ttu-id="6a624-117">**FinishedMsg は** メッセージのロックを解除し、メッセージの参照カウントが 1 で **、DoSentMail を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="6a624-117">**FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="6a624-118">**DoSentMail**�ł́A���̃^�X�N����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="6a624-119">送信後にメッセージを **PR_DELETE_AFTER_SUBMITする必要** があるかどうかを確認するメッセージ ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティをチェックします。</span><span class="sxs-lookup"><span data-stu-id="6a624-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="6a624-120">���M�ς݃A�C�e�� �t�H���_�[�̏ꏊ����肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="6a624-121">���b�Z�[�W�̂������M�ς݃A�C�e��] �ɐݒ肷��A�t�b�N�̏�����J�n���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="6a624-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span><span class="sxs-lookup"><span data-stu-id="6a624-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="6a624-123">���b�Z�[�W�������܂��B</span><span class="sxs-lookup"><span data-stu-id="6a624-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a624-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a624-124">See also</span></span>



[<span data-ttu-id="6a624-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="6a624-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="6a624-126">PidTagDeleteAfterSubmit ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="6a624-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="6a624-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a624-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

