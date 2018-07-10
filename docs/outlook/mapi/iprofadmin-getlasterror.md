---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 250074b28b98269df58fecfcb2d178f73e26c571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801126"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="b04cf-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b04cf-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="b04cf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b04cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b04cf-105">前のプロファイルの管理オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="b04cf-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b04cf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b04cf-106">Parameters</span></span>

 <span data-ttu-id="b04cf-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b04cf-107">_hResult_</span></span>
  
> <span data-ttu-id="b04cf-108">[in]以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="b04cf-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="b04cf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b04cf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b04cf-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b04cf-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b04cf-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b04cf-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b04cf-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b04cf-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b04cf-113">_LppMAPIError_パラメーターに返された[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="b04cf-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b04cf-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b04cf-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b04cf-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b04cf-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b04cf-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b04cf-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b04cf-117">取得する**MAPIERROR**構造体がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b04cf-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b04cf-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b04cf-118">Return value</span></span>

<span data-ttu-id="b04cf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b04cf-119">S_OK</span></span> 
  
> <span data-ttu-id="b04cf-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b04cf-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b04cf-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b04cf-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b04cf-122">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b04cf-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b04cf-123">備考</span><span class="sxs-lookup"><span data-stu-id="b04cf-123">Remarks</span></span>

<span data-ttu-id="b04cf-124">**IProfAdmin::GetLastError**メソッドは、プロファイルの管理オブジェクトのメソッドの呼び出しから返された最後のエラーに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="b04cf-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b04cf-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b04cf-125">Notes to callers</span></span>

<span data-ttu-id="b04cf-126">MAPI が提供を 1 つ**返します**は S_OK を返し、 _lppMAPIError_パラメーター場合にのみが指す場合は、 **MAPIERROR**構造体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b04cf-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b04cf-127">どのような最後のエラーまたはエラーを報告するのにはそれ以上には、MAPI は判断できません。</span><span class="sxs-lookup"><span data-stu-id="b04cf-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b04cf-128">この状況では、NULL へのポインターは_lppMAPIError_で返されます。</span><span class="sxs-lookup"><span data-stu-id="b04cf-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="b04cf-129">**MAPIERROR**構造のため、MAPI によって割り当てられたすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b04cf-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b04cf-130">**GetLastError**メソッドの詳細については、[拡張エラーの使用](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b04cf-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b04cf-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="b04cf-131">See also</span></span>



[<span data-ttu-id="b04cf-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b04cf-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b04cf-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b04cf-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b04cf-134">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b04cf-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
