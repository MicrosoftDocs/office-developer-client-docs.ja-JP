---
title: MAPI で書式設定されたテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6b82a755cbf2c8bd0f1d3676d4560e131dce3bd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800118"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="3f2fb-103">MAPI で書式設定されたテキスト</span><span class="sxs-lookup"><span data-stu-id="3f2fb-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="3f2fb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f2fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f2fb-105">メッセージのテキストは格納できるテキスト形式を使用して転送したり、書式設定されたテキスト。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="3f2fb-106">書式設定されたテキストで、1 つまたは複数のフォント、フォント サイズなど、テキストの色の外観を変更することによりメッセージのテキストを強化します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="3f2fb-107">お勧めしますがすべてのクライアントとすべてのメッセージ ストア プロバイダーが書式設定されたテキストをサポート可能な限り、します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="3f2fb-108">メッセージの読みやすさを向上し、容易かつ効率的にメッセージの処理をすることによって値を追加するメッセージの書式設定されたテキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="3f2fb-109">書式設定されたテキストは、さまざまな方法で実装できます。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="3f2fb-110">リッチ テキスト形式 (RTF) で、最も一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="3f2fb-111">MAPI メッセージのテキスト情報を保持するための 3 つの転送可能なプロパティを定義する: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、HTML、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)のテキストに) 圧縮された rtf 形式のテキストにします。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="3f2fb-112">メッセージ テキストの書式設定されたバージョンであるため 2 回バージョンと同じサイズ、書式を設定せず、rtf 形式のテキストは、メッセージの転送、 **PR_RTF_COMPRESSED**プロパティに格納する前に圧縮されています。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="3f2fb-113">画面にメッセージを表示するのには時間がある場合は、MAPI によって提供されるユーティリティ関数を使用して圧縮されたことはできません。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="3f2fb-114">MAPI は、これら 2 つのメッセージ テキストのプロパティを定義し、それらの間の変換のためのメカニズム RTF に対応していないクライアントはクライアントとサポートしないメッセージング システムと相互運用できるように書式設定されたテキストです。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="3f2fb-115">テキストを同期して、書式設定</span><span class="sxs-lookup"><span data-stu-id="3f2fb-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="3f2fb-116">RTF メッセージ テキストの書式設定と同期を維持する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="3f2fb-117">送信メッセージ内のテキストを書式設定のサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="3f2fb-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="3f2fb-118">送信するメッセージの書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="3f2fb-119">受信メッセージ内のテキストを書式設定のサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="3f2fb-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="3f2fb-120">受信メッセージの書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="3f2fb-121">メッセージ ・ ストアの責任を書式設定されたテキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="3f2fb-122">書式設定されたテキストをサポートするためのメッセージ ストアの役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="3f2fb-123">添付ファイルを表示する書式設定されたテキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="3f2fb-124">添付ファイルを表示する場所を選択する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="3f2fb-125">ゲートウェイの役割を書式設定されたテキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="3f2fb-126">書式設定されたテキスト メッセージを送信および受信のゲートウェイの役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f2fb-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    
