---
title: PidTagPreferredByName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPreferredByName
api_type:
- COM
ms.assetid: 102f840c-5cd7-4507-ba42-20ba3669cd05
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4c0ad82f024ccc2effd9ba4d3c38e1a3a60717b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320434"
---
# <a name="pidtagpreferredbyname-canonical-property"></a><span data-ttu-id="fd1a1-103">PidTagPreferredByName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-103">PidTagPreferredByName Canonical Property</span></span>

  
  
<span data-ttu-id="fd1a1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd1a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd1a1-105">受信者が呼び出す名前を含む。</span><span class="sxs-lookup"><span data-stu-id="fd1a1-105">Contains the name that the recipient prefers to be called.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd1a1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fd1a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd1a1-107">PR_PREFERRED_BY_NAME、PR_PREFERRED_BY_NAME_A、PR_PREFERRED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="fd1a1-107">PR_PREFERRED_BY_NAME, PR_PREFERRED_BY_NAME_A, PR_PREFERRED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="fd1a1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fd1a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd1a1-109">0x3A47</span><span class="sxs-lookup"><span data-stu-id="fd1a1-109">0x3A47</span></span>  <br/> |
|<span data-ttu-id="fd1a1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fd1a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd1a1-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd1a1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fd1a1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fd1a1-112">Area:</span></span>  <br/> |<span data-ttu-id="fd1a1-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="fd1a1-113">MAPI mail user</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fd1a1-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fd1a1-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd1a1-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fd1a1-115">Protocol specifications</span></span>

<span data-ttu-id="fd1a1-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd1a1-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd1a1-117">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="fd1a1-117">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd1a1-118">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd1a1-118">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd1a1-119">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1a1-119">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd1a1-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fd1a1-120">Header files</span></span>

<span data-ttu-id="fd1a1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd1a1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd1a1-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fd1a1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd1a1-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd1a1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fd1a1-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="fd1a1-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd1a1-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd1a1-125">See also</span></span>



[<span data-ttu-id="fd1a1-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd1a1-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd1a1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd1a1-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fd1a1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd1a1-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fd1a1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

