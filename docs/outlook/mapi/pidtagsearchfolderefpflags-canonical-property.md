---
title: PidTagSearchFolderEfpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336429"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="e1222-103">PidTagSearchFolderEfpFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1222-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e1222-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1222-105">検索フォルダーの検索フォルダー コンテナーに適用される拡張フォルダー フラグが含まれる。</span><span class="sxs-lookup"><span data-stu-id="e1222-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1222-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e1222-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1222-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e1222-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e1222-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e1222-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1222-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="e1222-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="e1222-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e1222-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1222-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1222-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1222-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e1222-112">Area:</span></span>  <br/> |<span data-ttu-id="e1222-113">検索</span><span class="sxs-lookup"><span data-stu-id="e1222-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1222-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e1222-114">Remarks</span></span>

<span data-ttu-id="e1222-115">このプロパティには、フォルダー **のフィールド b** の PR_EXTENDED_FOLDER_FLAGS ([PidTagExtendedFolderFlags)](pidtagextendedfolderflags-canonical-property.md)プロパティと **ExtendedFlags** サブプロパティのフラグを具体的に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1222-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="e1222-116">フォルダー フラグの詳細については [、「MS-OXOCFG」を参照してください](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e1222-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1222-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e1222-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1222-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e1222-118">Protocol specifications</span></span>

<span data-ttu-id="e1222-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1222-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1222-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e1222-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1222-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1222-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1222-122">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e1222-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="e1222-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1222-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1222-124">共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e1222-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1222-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e1222-125">Header files</span></span>

<span data-ttu-id="e1222-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1222-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1222-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e1222-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1222-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1222-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e1222-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e1222-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1222-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1222-130">See also</span></span>



[<span data-ttu-id="e1222-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e1222-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1222-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1222-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1222-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e1222-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1222-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e1222-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

