---
title: MAPI プロパティのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799842"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="a0ccc-103">MAPI プロパティのコピー</span><span class="sxs-lookup"><span data-stu-id="a0ccc-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="a0ccc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0ccc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0ccc-105">クライアントとサービス ・ プロバイダーにコピーできます 1 つまたは複数オブジェクトのプロパティの次の**IMAPIProp**メソッドおよび API 関数をクリックすると。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="a0ccc-106">[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドは、オプションで選択したプロパティを除く、他のオブジェクトにすべてのオブジェクトのプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="a0ccc-107">**CopyTo**は、コピーまたは任意の種類のオブジェクトを移動するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="a0ccc-108">[IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドは、オブジェクトの選択したプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="a0ccc-109">**CopyProps**は、主に使用するメッセージに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="a0ccc-110">クライアント作成する場合、メッセージの返信、転送されたコピー **CopyProps**ハンドルの元のメッセージから、適切なプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="a0ccc-111">[PropCopyMore](propcopymore.md)関数は、別に、1 つの場所から 1 つのプロパティ値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="a0ccc-112">**PropCopyMore**を使用して、注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="a0ccc-113">できます-一度に 1 つの値をコピーするときに-多くの小さなメモリ ブロックを割り当てるし、メモリをフラグメント化します。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="a0ccc-114">[ScCopyProps](sccopyprops.md)関数では、一括でプロパティの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="a0ccc-115">**ScCopyProps**は、切り離されたメモリ ブロックから構築されているプロパティの値をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="a0ccc-116">新しいプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="a0ccc-117">**ScCopyProps**によって返されるプロパティの配列をディスクに保存する場合は、ポインターを調整する[ScRelocProps](screlocprops.md)関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="a0ccc-118">**ScRelocProps**を 2 回呼び出す必要があります。データの操作を記述する前に、アドレスを調整するには、1 回だけ読み取り操作中にもう一度し。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="a0ccc-119">**ScRelocProps**関数は、プロパティ値の配列が最初に 1 つの割り当てに割り当てられたものとします。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="a0ccc-120">API 関数は、上記リスト プロパティのコピーを別のオブジェクトの 1 つのオブジェクトからではなく、メモリ内で説明します。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="a0ccc-121">これらの関数は現在サポートされていませんが、将来のリリースではサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0ccc-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0ccc-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0ccc-122">See also</span></span>



[<span data-ttu-id="a0ccc-123">MAPI Property Overview</span><span class="sxs-lookup"><span data-stu-id="a0ccc-123">MAPI Property Overview</span></span>](mapi-property-overview.md)
