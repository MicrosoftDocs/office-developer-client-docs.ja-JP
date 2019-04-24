---
title: itabledatahrgetview
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278716"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="91c83-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="91c83-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="91c83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91c83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91c83-105">[IMAPITable](imapitableiunknown.md)実装へのポインターを返すテーブルビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="91c83-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="91c83-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="91c83-106">Parameters</span></span>

 <span data-ttu-id="91c83-107">_lpssortorderset_</span><span class="sxs-lookup"><span data-stu-id="91c83-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="91c83-108">順番テーブルビューの並べ替え順序を記述する並べ替え順序構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="91c83-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="91c83-109">_lpssortorderset_パラメーターで NULL が渡された場合、ビューは並べ替えられません。</span><span class="sxs-lookup"><span data-stu-id="91c83-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="91c83-110">_lpfcallerrelease_</span><span class="sxs-lookup"><span data-stu-id="91c83-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="91c83-111">順番ビューを解放したときに MAPI が呼び出す呼び出し[errelease](callerrelease.md)プロトタイプに基づく、コールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="91c83-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="91c83-112">_lpfcallerrelease_パラメーターで NULL が渡された場合、ビューのリリース時に関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="91c83-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="91c83-113">_ulcallerdata_</span><span class="sxs-lookup"><span data-stu-id="91c83-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="91c83-114">順番新しいビューで保存する必要があり、 _lpfcallerrelease_が指すコールバック関数に渡されるデータ。</span><span class="sxs-lookup"><span data-stu-id="91c83-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="91c83-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="91c83-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="91c83-116">読み上げ新しく作成されたビューへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="91c83-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91c83-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="91c83-117">Return value</span></span>

<span data-ttu-id="91c83-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="91c83-118">S_OK</span></span> 
  
> <span data-ttu-id="91c83-119">ビューが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="91c83-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91c83-120">解説</span><span class="sxs-lookup"><span data-stu-id="91c83-120">Remarks</span></span>

<span data-ttu-id="91c83-121">**itabledata:: hrgetview**メソッドは、テーブル内のデータの読み取り専用のビューを作成します。これは、 _lpssortorderset_パラメーターで示された順序で並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="91c83-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="91c83-122">カーソルは、ビューの最初の行の先頭に配置されます。</span><span class="sxs-lookup"><span data-stu-id="91c83-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="91c83-123">ビューにアクセスするための**IMAPITable**インターフェイスの実装が返されます。</span><span class="sxs-lookup"><span data-stu-id="91c83-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="91c83-124">サービスプロバイダーは、クライアントがテーブルにアクセスできるようにする必要がある場合に**hrgetview**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="91c83-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="91c83-125">**hrgetview**はビューを作成し、 **IMAPITable**ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="91c83-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="91c83-126">その後、サービスプロバイダーはクライアントにポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="91c83-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="91c83-127">表を使用してクライアントが終了し、その[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出すと、 **hrgetview**は_lpfcallerrelease_パラメーターで指定されたコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="91c83-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="91c83-128">サービスプロバイダーが、カスタマイズされた列セットまたは制限を持つビューをクライアントに戻す必要がある場合、プロバイダーはクライアントアクセスを許可する前に、ビューの[IMAPITable:: SetColumns](imapitable-setcolumns.md)および[imapitable:: Restrict](imapitable-restrict.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="91c83-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91c83-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="91c83-129">See also</span></span>



[<span data-ttu-id="91c83-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="91c83-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="91c83-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91c83-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="91c83-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="91c83-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="91c83-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91c83-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

