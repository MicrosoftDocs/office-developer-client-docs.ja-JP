---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 31b2353b76bbac5cd58cd791f4a289c7dbabdb78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801486"
---
# <a name="mapiinit0"></a><span data-ttu-id="87e16-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="87e16-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="87e16-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87e16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87e16-105">[生じます](mapiinitialize.md)にオプションを伝達します。</span><span class="sxs-lookup"><span data-stu-id="87e16-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87e16-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="87e16-106">Header file:</span></span>  <br/> |<span data-ttu-id="87e16-107">MAPIX。H</span><span class="sxs-lookup"><span data-stu-id="87e16-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="87e16-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="87e16-108">Members</span></span>

 <span data-ttu-id="87e16-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="87e16-109">**ulVersion**</span></span>
  
> <span data-ttu-id="87e16-110">**MAPIINIT_0**構造体のバージョン番号を表す整数値。</span><span class="sxs-lookup"><span data-stu-id="87e16-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="87e16-111">**UlVersion**メンバーは、今後の拡張し、MAPI インターフェイスのバージョンではありません。</span><span class="sxs-lookup"><span data-stu-id="87e16-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="87e16-112">現在、 **ulVersion**は、MAPI_INIT_VERSION に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87e16-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="87e16-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="87e16-113">**ulFlags**</span></span>
  
> <span data-ttu-id="87e16-114">MAPI セッションの初期化を制御するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="87e16-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="87e16-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="87e16-115">The following flags can be set:</span></span>
    
<span data-ttu-id="87e16-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="87e16-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="87e16-117">MAPI には、通知の**生じます**を呼び出すために使用する最初のスレッドではなく処理を専用のスレッドを使用して通知を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87e16-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="87e16-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="87e16-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="87e16-119">呼び出し元は、Windows サービスとして実行しています。</span><span class="sxs-lookup"><span data-stu-id="87e16-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="87e16-120">Windows サービスではこのフラグが設定されていない必要がありますように実行されていない呼び出し元サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87e16-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="87e16-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="87e16-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="87e16-122">[CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)の呼び出しで COM を初期化するために**生じます**が試みないように、MAPI_NO_COINT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="87e16-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="87e16-123">**MAPIINIT_0**構造体が渡された場合に**生じます** _ulFlags_ MAPI_NO_COINIT に設定すると、MAPI は、COM が既に初期化されているし、 **CoInitialize**の呼び出しが省略されますと見なされます。</span><span class="sxs-lookup"><span data-stu-id="87e16-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87e16-124">備考</span><span class="sxs-lookup"><span data-stu-id="87e16-124">Remarks</span></span>

<span data-ttu-id="87e16-125">マルチ スレッド クライアントでは、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87e16-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="87e16-126">フラグが設定されていない場合**生じます**への最初の呼び出しを行うために使用するスレッドに通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="87e16-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="87e16-127">このフラグを設定して、クライアントのスレッドの安全性を実装する方法の詳細については、 [MAPI でのスレッド処理](threading-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87e16-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87e16-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="87e16-128">See also</span></span>



[<span data-ttu-id="87e16-129">生じます</span><span class="sxs-lookup"><span data-stu-id="87e16-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="87e16-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="87e16-130">MAPI Structures</span></span>](mapi-structures.md)
