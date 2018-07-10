---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801067"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="68b7e-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="68b7e-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="68b7e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68b7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68b7e-105">メッセージ ストアのオブジェクトに対して発生した最後のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="68b7e-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="68b7e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="68b7e-106">Parameters</span></span>

 <span data-ttu-id="68b7e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="68b7e-107">_hResult_</span></span>
  
> <span data-ttu-id="68b7e-108">[in]メッセージ ストア オブジェクトの以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="68b7e-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="68b7e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68b7e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="68b7e-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="68b7e-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="68b7e-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="68b7e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="68b7e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68b7e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="68b7e-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="68b7e-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="68b7e-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="68b7e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="68b7e-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="68b7e-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="68b7e-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="68b7e-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="68b7e-117">返すには、 **MAPIERROR**がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="68b7e-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68b7e-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="68b7e-118">Return value</span></span>

<span data-ttu-id="68b7e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="68b7e-119">S_OK</span></span> 
  
> <span data-ttu-id="68b7e-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="68b7e-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="68b7e-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="68b7e-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="68b7e-122">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="68b7e-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68b7e-123">備考</span><span class="sxs-lookup"><span data-stu-id="68b7e-123">Remarks</span></span>

<span data-ttu-id="68b7e-124">最後に、メッセージ ストアのオブジェクトのメソッドの呼び出しから返されるエラーに関するユーザーへのメッセージに表示するのに情報を取得するために**IMSLogon::GetLastError**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="68b7e-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="68b7e-125">返された**MAPIERROR**構造体は、MAPI によって割り当てられたすべてのメモリを解放するには、クライアント アプリケーションにのみ、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="68b7e-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="68b7e-126">**GetLastError**からの戻り値は、 **MAPIERROR**を使用するアプリケーションの S_OK をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="68b7e-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="68b7e-127">戻り値が S_OK の場合であって、 **MAPIERROR**が返されません。</span><span class="sxs-lookup"><span data-stu-id="68b7e-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="68b7e-128">実装は、最後のエラーが特定できない場合、または、 **MAPIERROR**は、エラー、 **GetLastError**のポインターを返します NULL に_lppMAPIError_の代わりには使用できません。</span><span class="sxs-lookup"><span data-stu-id="68b7e-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68b7e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="68b7e-129">See also</span></span>



[<span data-ttu-id="68b7e-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="68b7e-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="68b7e-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="68b7e-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="68b7e-132">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="68b7e-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)
