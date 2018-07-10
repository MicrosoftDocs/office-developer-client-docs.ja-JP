---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800317"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="de704-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="de704-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="de704-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de704-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de704-105">テーブルのすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="de704-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de704-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="de704-106">Header file:</span></span>  <br/> |<span data-ttu-id="de704-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="de704-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="de704-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="de704-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="de704-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="de704-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="de704-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de704-110">Called by:</span></span>  <br/> |<span data-ttu-id="de704-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="de704-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="de704-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="de704-112">Parameters</span></span>

 <span data-ttu-id="de704-113">_参照を必要_</span><span class="sxs-lookup"><span data-stu-id="de704-113">_ptable_</span></span>
  
> <span data-ttu-id="de704-114">[in]行の取得元の MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="de704-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="de704-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="de704-115">_ptaga_</span></span>
  
> <span data-ttu-id="de704-116">[in]プロパティの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインターでは、テーブルの列を示すタグ付けします。</span><span class="sxs-lookup"><span data-stu-id="de704-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="de704-117">これらのタグを使用して、取得する特定の列を選択します。</span><span class="sxs-lookup"><span data-stu-id="de704-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="de704-118">_Ptaga_パラメーターが NULL の場合は、 **HrQueryAllRows**は、全体の列のセット_の参照を必要_パラメーターで渡された現在のテーブル ビューを取得します。</span><span class="sxs-lookup"><span data-stu-id="de704-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="de704-119">_プレス_</span><span class="sxs-lookup"><span data-stu-id="de704-119">_pres_</span></span>
  
> <span data-ttu-id="de704-120">[in]取得の制限を含む[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="de704-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="de704-121">_プレス_パラメーターが NULL の場合は、 **HrQueryAllRows**には制限がありません。</span><span class="sxs-lookup"><span data-stu-id="de704-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="de704-122">_pso_</span><span class="sxs-lookup"><span data-stu-id="de704-122">_psos_</span></span>
  
> <span data-ttu-id="de704-123">[in]取得する列の並べ替え順序を識別する[SSortOrderSet](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="de704-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="de704-124">_Pso_のパラメーターが NULL の場合は、テーブルの既定の並べ替え順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de704-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="de704-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="de704-125">_crowsMax_</span></span>
  
> <span data-ttu-id="de704-126">[in]取得する行の最大数。</span><span class="sxs-lookup"><span data-stu-id="de704-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="de704-127">_CrowsMax_パラメーターの値が 0 の場合は、取得される行の数に制限は設定されていません。</span><span class="sxs-lookup"><span data-stu-id="de704-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="de704-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="de704-128">_pprows_</span></span>
  
> <span data-ttu-id="de704-129">[out]取得したテーブルの行へのポインターの配列を格納する返される[SRowSet](srowset.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="de704-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de704-130">�߂�l</span><span class="sxs-lookup"><span data-stu-id="de704-130">Return value</span></span>

<span data-ttu-id="de704-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="de704-131">S_OK</span></span> 
  
> <span data-ttu-id="de704-132">呼び出しには、予想されるテーブルの行が取得されます。</span><span class="sxs-lookup"><span data-stu-id="de704-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="de704-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="de704-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="de704-134">テーブル内の行の数は、 _crowsMax_パラメーターに渡された値よりも大きくなります。</span><span class="sxs-lookup"><span data-stu-id="de704-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de704-135">備考</span><span class="sxs-lookup"><span data-stu-id="de704-135">Remarks</span></span>

<span data-ttu-id="de704-136">クライアント アプリケーションまたはサービス プロバイダーには、 **HrQueryAllRows**を取得しよう、制限を課すことによって指す_プレス_パラメーター以外の行の数を制御がありません。</span><span class="sxs-lookup"><span data-stu-id="de704-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="de704-137">_CrowsMax_パラメーターは、テーブルのロー数を取得を制限することはできませんではなく取得したすべての行を保持するために使用できるメモリの最大量を定義します。</span><span class="sxs-lookup"><span data-stu-id="de704-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="de704-138">大容量のメモリのオーバーフローに対する唯一の防策は、 _crowsMax_を設定することによって提供される暫定的な機能です。</span><span class="sxs-lookup"><span data-stu-id="de704-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="de704-139">エラーの戻り値が MAPI_E_TABLE_TOO_BIG では、テーブルには、すべてを一度にメモリに保持するが多すぎる行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de704-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="de704-140">メッセージ ストアのテーブルや、プロバイダーのテーブルなど、通常は小さいテーブル通常安全に取得できる**HrQueryAllRows**とします。</span><span class="sxs-lookup"><span data-stu-id="de704-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="de704-141">[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを使用してのサブセクションでは、テーブルの内容のテーブルなど、宛先テーブルも非常に大きな危険にさらさを走査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de704-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="de704-142">プロパティ タイプ PT_NULL および PROP_ID_NULL プロパティの識別子を持つ場合は、テーブルのプロパティに定義された**HrQueryAllRows**が呼び出されたときに、返されます</span><span class="sxs-lookup"><span data-stu-id="de704-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  
