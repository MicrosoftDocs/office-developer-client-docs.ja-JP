---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799874"
---
# <a name="createtable"></a><span data-ttu-id="a68d8-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="a68d8-103">CreateTable</span></span>

  
  
<span data-ttu-id="a68d8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a68d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a68d8-105">構造とテーブルの内容を作成するのに使用できる[ITableData](itabledataiunknown.md)オブジェクトのオブジェクト ハンドルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a68d8-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a68d8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a68d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a68d8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a68d8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a68d8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a68d8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a68d8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a68d8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a68d8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a68d8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a68d8-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a68d8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a><span data-ttu-id="a68d8-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a68d8-112">Parameters</span></span>

 <span data-ttu-id="a68d8-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a68d8-113">_lpInterface_</span></span>
  
> <span data-ttu-id="a68d8-114">[in]テーブルのデータ オブジェクトのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a68d8-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="a68d8-115">有効なインタ フェース識別子は、IID_IMAPITableData です。</span><span class="sxs-lookup"><span data-stu-id="a68d8-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="a68d8-116">テーブルのデータ オブジェクトの標準的なインターフェイスにキャストするのには_lppTableData_パラメーターで返されるテーブルのデータ オブジェクトは、 _lpInterface_パラメーターに NULL を渡すことも。</span><span class="sxs-lookup"><span data-stu-id="a68d8-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="a68d8-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a68d8-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a68d8-118">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a68d8-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="a68d8-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="a68d8-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="a68d8-120">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a68d8-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="a68d8-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="a68d8-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a68d8-122">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a68d8-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="a68d8-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="a68d8-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="a68d8-124">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a68d8-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="a68d8-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="a68d8-125">_ulTableType_</span></span>
  
> <span data-ttu-id="a68d8-126">[in]表形式ビューの[IMAPITable::GetStatus](imapitable-getstatus.md)の戻り値のデータの一部としてクライアント アプリケーションまたはサービス プロバイダーに提供されるテーブルの型。</span><span class="sxs-lookup"><span data-stu-id="a68d8-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="a68d8-127">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a68d8-127">Possible values are:</span></span> 
    
<span data-ttu-id="a68d8-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="a68d8-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="a68d8-129">テーブルの内容は動的で、基になるデータの変化に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="a68d8-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="a68d8-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="a68d8-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="a68d8-131">テーブル内の行は固定ですが、これらの行の値は動的で、基になるデータの変化に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="a68d8-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="a68d8-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="a68d8-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="a68d8-133">テーブルは静的であり、基になるデータが変更された内容も変更されません。</span><span class="sxs-lookup"><span data-stu-id="a68d8-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="a68d8-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="a68d8-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="a68d8-135">[in]テーブルのデータを変更するときに使用される列のインデックス番号です。</span><span class="sxs-lookup"><span data-stu-id="a68d8-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="a68d8-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="a68d8-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="a68d8-137">[in]オブジェクト データを保持するテーブルに必要なプロパティを示すプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a68d8-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="a68d8-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="a68d8-138">_lppTableData_</span></span>
  
> <span data-ttu-id="a68d8-139">[out]返されるテーブルのデータ オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a68d8-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a68d8-140">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a68d8-140">Return value</span></span>

<span data-ttu-id="a68d8-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="a68d8-141">S_OK</span></span> 
  
> <span data-ttu-id="a68d8-142">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a68d8-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a68d8-143">����</span><span class="sxs-lookup"><span data-stu-id="a68d8-143">Remarks</span></span>

<span data-ttu-id="a68d8-144">_LpAllocateBuffer_、 _lpAllocateMore_、および_lpFreeBuffer_の入力パラメーターは、それぞれ[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数では、] をポイントします。</span><span class="sxs-lookup"><span data-stu-id="a68d8-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="a68d8-145">**CreateTable**を呼び出すクライアント アプリケーションが MAPI の関数を同じ名前でポインターを渡しますサービス プロバイダーの初期化の呼び出しで受信した、 [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドの呼び出しで取得するこれらの関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="a68d8-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a68d8-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="a68d8-146">See also</span></span>



[<span data-ttu-id="a68d8-147">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a68d8-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
