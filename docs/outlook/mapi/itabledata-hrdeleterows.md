---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801212"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="efe96-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="efe96-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="efe96-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="efe96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="efe96-105">複数のテーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="efe96-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="efe96-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="efe96-106">Parameters</span></span>

 <span data-ttu-id="efe96-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efe96-107">_ulFlags_</span></span>
  
> <span data-ttu-id="efe96-108">[in]削除を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="efe96-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="efe96-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="efe96-109">The following flag can be set:</span></span>
    
<span data-ttu-id="efe96-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="efe96-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="efe96-111">テーブルと 1 つの TABLE_RELOAD 通知を送信する、対応するすべてのビューからすべての行を削除します。</span><span class="sxs-lookup"><span data-stu-id="efe96-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="efe96-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="efe96-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="efe96-113">[in]削除する行を表す行セットへのポインター。</span><span class="sxs-lookup"><span data-stu-id="efe96-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="efe96-114">_UlFlags_パラメーターに TAD_ALL_ROWS フラグが設定されている場合は、 _lprowsetToDelete_パラメーターを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="efe96-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="efe96-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="efe96-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="efe96-116">[out]削除された行の数。</span><span class="sxs-lookup"><span data-stu-id="efe96-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efe96-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="efe96-117">Return value</span></span>

<span data-ttu-id="efe96-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="efe96-118">S_OK</span></span> 
  
> <span data-ttu-id="efe96-119">テーブルの行は削除されました。</span><span class="sxs-lookup"><span data-stu-id="efe96-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efe96-120">備考</span><span class="sxs-lookup"><span data-stu-id="efe96-120">Remarks</span></span>

<span data-ttu-id="efe96-121">**ITableData::HrDeleteRows**メソッドは、検索し、行の各**aRow**のエントリの**lpProps**のメンバーによって設定するのにはポイントのプロパティに一致する列を含むテーブルの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="efe96-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="efe96-122">インデックス列を使用して各行を識別します。この列には、 [CreateTable](createtable.md)関数への呼び出し内の_ulPropTagIndexColumn_パラメーターで渡されたプロパティ タグと同じプロパティ タグが必要です。</span><span class="sxs-lookup"><span data-stu-id="efe96-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="efe96-123">_CRowsDeleted_では、実際に削除された行の数が返されます。</span><span class="sxs-lookup"><span data-stu-id="efe96-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="efe96-124">1 つまたは複数の行が見つからなかった場合、エラーは返されません。</span><span class="sxs-lookup"><span data-stu-id="efe96-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="efe96-125">行が削除されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="efe96-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="efe96-126">行を削除するか、テーブルの既存のビューに使用できる列は縮小されません、削除された行が特定の列の値を持つ最後の場合でも以降の表形式ビューに開かれます。</span><span class="sxs-lookup"><span data-stu-id="efe96-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="efe96-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="efe96-127">See also</span></span>



[<span data-ttu-id="efe96-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="efe96-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="efe96-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="efe96-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="efe96-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="efe96-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="efe96-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="efe96-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="efe96-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="efe96-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="efe96-133">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="efe96-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)
