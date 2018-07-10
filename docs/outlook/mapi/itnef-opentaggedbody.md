---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ed433dc1fcf2a366d2ece07ac06d4e12558e4aa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801229"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="5f025-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="5f025-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="5f025-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f025-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f025-105">カプセル化されたメッセージのテキストのストリームのインタ フェースを開きます。</span><span class="sxs-lookup"><span data-stu-id="5f025-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="5f025-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5f025-106">Parameters</span></span>

 <span data-ttu-id="5f025-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5f025-107">_lpMessage_</span></span>
  
> <span data-ttu-id="5f025-108">[in]ストリームが関連付けられているメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f025-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="5f025-109">このメッセージは、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで渡されるのと同じメッセージである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5f025-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="5f025-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5f025-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5f025-111">[in]ストリーム インターフェイスを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5f025-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="5f025-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5f025-112">The following flags can be set:</span></span>
    
<span data-ttu-id="5f025-113">タグ</span><span class="sxs-lookup"><span data-stu-id="5f025-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="5f025-114">現在のメッセージのプロパティがない場合は作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f025-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="5f025-115">プロパティが存在する場合、トランスポート ニュートラル カプセル化形式 (TNEF) ストリームからデータをプロパティの現在のデータを交換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f025-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="5f025-116">実装では、タグのフラグを設定するとき、にも MAPI_MODIFY フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f025-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="5f025-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5f025-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5f025-118">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="5f025-118">Requests read/write permission.</span></span> <span data-ttu-id="5f025-119">デフォルトのインタ フェースは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="5f025-119">The default interface is read-only.</span></span> <span data-ttu-id="5f025-120">タグを設定するたびに、MAPI_MODIFY を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f025-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="5f025-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="5f025-121">_lppStream_</span></span>
  
> <span data-ttu-id="5f025-122">[out]([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティを渡すには、からのテキストを含んでいるストリーム オブジェクトへのポインターへのポインターがメッセージをカプセル化し、 [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx)インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5f025-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5f025-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5f025-123">Return value</span></span>

<span data-ttu-id="5f025-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f025-124">S_OK</span></span> 
  
> <span data-ttu-id="5f025-125">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5f025-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f025-126">備考</span><span class="sxs-lookup"><span data-stu-id="5f025-126">Remarks</span></span>

<span data-ttu-id="5f025-127">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイがカプセル化されたメッセージのテキストのストリーム インターフェイスを開くに**ITnef::OpenTaggedBody**メソッドを呼び出します (つまり、TNEF のオブジェクト)。</span><span class="sxs-lookup"><span data-stu-id="5f025-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="5f025-128">処理の一環として、 **OpenTaggedBody**は挿入するか、またはメッセージのテキスト内のすべての添付ファイルまたは OLE オブジェクトの位置を示すタグを添付ファイルを解析し。</span><span class="sxs-lookup"><span data-stu-id="5f025-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="5f025-129">添付ファイルのタグは、次の形式では。</span><span class="sxs-lookup"><span data-stu-id="5f025-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="5f025-130">**[** **::** の_添付ファイル名_ _n_ **の**_コンテナー名の添付ファイル_ **]**</span><span class="sxs-lookup"><span data-stu-id="5f025-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="5f025-131">_添付ファイル名_が添付ファイルのオブジェクトを説明します。 _n_は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_lpKey_パラメーターに渡された値からインクリメントするシーケンスの一部である添付ファイルを識別する番号_コンテナー名の添付ファイル_が添付ファイルのオブジェクトが存在する物理コンポーネントを説明しています。</span><span class="sxs-lookup"><span data-stu-id="5f025-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="5f025-132">**OpenTaggedBody**メッセージのテキストを読み込んで、attachment オブジェクトは、テキストで表示されていた元の場所に、添付ファイルのタグを挿入します。</span><span class="sxs-lookup"><span data-stu-id="5f025-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="5f025-133">元のメッセージ テキストは変更されません。</span><span class="sxs-lookup"><span data-stu-id="5f025-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="5f025-134">タグを持つメッセージは、ストリームとタグを削除した添付ファイルのオブジェクトは、ストリーム内のタグの位置に再配置されます。</span><span class="sxs-lookup"><span data-stu-id="5f025-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f025-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f025-135">See also</span></span>



[<span data-ttu-id="5f025-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="5f025-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="5f025-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="5f025-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="5f025-138">PidTagBody の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5f025-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="5f025-139">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f025-139">ITnef : IUnknown</span></span>](itnefiunknown.md)
