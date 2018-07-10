---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800430"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="04a2f-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="04a2f-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="04a2f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04a2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04a2f-105">MAPI テーブルのオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="04a2f-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="04a2f-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="04a2f-106">Parameters</span></span>

 <span data-ttu-id="04a2f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04a2f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="04a2f-108">[in]次の値のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="04a2f-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="04a2f-109">0 (ゼロ)</span><span class="sxs-lookup"><span data-stu-id="04a2f-109">0 (zero)</span></span>
  
> <span data-ttu-id="04a2f-110">**UlRowFlags** 、 [ROWENTRY](rowentry.md)構造体のメンバーの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="04a2f-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="04a2f-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="04a2f-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="04a2f-112">新しい権限を設定します。</span><span class="sxs-lookup"><span data-stu-id="04a2f-112">Sets new rights.</span></span>
    
<span data-ttu-id="04a2f-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="04a2f-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="04a2f-114">ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の詳細を表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="04a2f-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="04a2f-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="04a2f-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="04a2f-116">ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="04a2f-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="04a2f-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="04a2f-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="04a2f-118">テーブル内のすべての行を交換してください。</span><span class="sxs-lookup"><span data-stu-id="04a2f-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="04a2f-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="04a2f-119">_lpMods_</span></span>
  
> <span data-ttu-id="04a2f-120">[in][Rowlist で](rowlist.md)を含む構造体のテーブルのオブジェクトのプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="04a2f-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="04a2f-121">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="04a2f-121">MFCMAPI reference</span></span>

<span data-ttu-id="04a2f-122">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="04a2f-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="04a2f-123">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="04a2f-123">**File**</span></span>|<span data-ttu-id="04a2f-124">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="04a2f-124">**Function**</span></span>|<span data-ttu-id="04a2f-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="04a2f-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04a2f-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="04a2f-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="04a2f-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="04a2f-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="04a2f-128">MFCMAPI では、 **IExchangeModifyTable::ModifyTable**メソッドを使用して、変更したルールをルールのテーブルに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="04a2f-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04a2f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="04a2f-129">See also</span></span>



[<span data-ttu-id="04a2f-130">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04a2f-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="04a2f-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="04a2f-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="04a2f-132">ROWLIST で</span><span class="sxs-lookup"><span data-stu-id="04a2f-132">ROWLIST</span></span>](rowlist.md)


<span data-ttu-id="04a2f-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="04a2f-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
