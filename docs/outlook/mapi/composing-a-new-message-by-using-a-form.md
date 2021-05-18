---
title: フォームを使用した新しいメッセージの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412801"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="3e67a-103">フォームを使用した新しいメッセージの作成</span><span class="sxs-lookup"><span data-stu-id="3e67a-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="3e67a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e67a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e67a-105">フォームを使用して新しいメッセージを作成するには、まず新しいカスタム メッセージ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3e67a-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="3e67a-106">**フォームを使用して新しいメッセージを作成するには**</span><span class="sxs-lookup"><span data-stu-id="3e67a-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="3e67a-107">フォーム マネージャーの [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) メソッドを呼び出して、フォーム情報オブジェクトへのポインター [(IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) インターフェイスを実装するオブジェクト) を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e67a-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="3e67a-108">[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)への呼び出しでフォーム情報オブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="3e67a-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="3e67a-109">**CreateForm は** 適切なフォーム サーバーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="3e67a-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="3e67a-110">さらに、インターフェイス識別子を **CreateForm** に渡して、新しいメッセージへのアクセスに使用するインターフェイスを指定します。</span><span class="sxs-lookup"><span data-stu-id="3e67a-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="3e67a-111">通常 [、IPersistMessage : IUnknown を](ipersistmessageiunknown.md) CreateForm に渡IID_IPersistMessage **を要求します**。</span><span class="sxs-lookup"><span data-stu-id="3e67a-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="3e67a-112">[IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出して、新しいメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="3e67a-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="3e67a-113">フォーム サーバーは、メッセージを作成するときに、メッセージの必須プロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e67a-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="3e67a-114">[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)または[IMAPISession::P repareForm](imapisession-prepareform.md)の後に[IMAPISession::ShowForm](imapisession-showform.md)の 2 つの戦略のいずれかを使用してメッセージを読み込む。</span><span class="sxs-lookup"><span data-stu-id="3e67a-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="3e67a-115">これらの戦略の詳細については、「メッセージをフォームに読み [込む」を参照してください](loading-a-message-into-a-form.md)。</span><span class="sxs-lookup"><span data-stu-id="3e67a-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="3e67a-116">**ResolveMessageClass** 呼び出しと **CreateForm** 呼び出しに必要な処理の間に、メッセージに関する情報 (メッセージ クラスなど) を既に取得する機会が既に存在する可能性が高いので、フォーム サーバーに新しいカスタム メッセージを読み込む際にパフォーマンスが向上する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3e67a-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="3e67a-117">この理由から **、LoadForm** を呼び出す前に必要な処理を簡略化できます。この処理は、トピック「メッセージをフォームに読み込む」で [説明](loading-a-message-into-a-form.md)されています。</span><span class="sxs-lookup"><span data-stu-id="3e67a-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

