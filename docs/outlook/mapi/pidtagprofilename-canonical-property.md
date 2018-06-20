---
title: PidTagProfileName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803197"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="f84a4-103">PidTagProfileName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f84a4-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="f84a4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f84a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f84a4-105">プロファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f84a4-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f84a4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f84a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f84a4-107">PR_PROFILE_NAME、PR_PROFILE_NAME_A、PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f84a4-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f84a4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f84a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f84a4-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="f84a4-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="f84a4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="f84a4-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f84a4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f84a4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f84a4-112">Area:</span></span>  <br/> |<span data-ttu-id="f84a4-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="f84a4-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f84a4-114">備考</span><span class="sxs-lookup"><span data-stu-id="f84a4-114">Remarks</span></span>

<span data-ttu-id="f84a4-115">これらのプロパティは、サービス プロバイダーによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="f84a4-115">These properties are computed by service providers.</span></span> <span data-ttu-id="f84a4-116">**ServiceEntry**関数のプロバイダーの実装では、プロファイル名を検出するのにはこれらのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f84a4-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="f84a4-117">クライアント アプリケーションでは、MAPI サブシステムの状態テーブルの行の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを調べることによって、プロファイル名を取得するための便利な方法として、これらのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f84a4-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="f84a4-118">これらのプロパティが一意でくださいない時、たとえば、プロファイルが削除され、同じ名前の後で再作成で。</span><span class="sxs-lookup"><span data-stu-id="f84a4-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="f84a4-119">MAPI と呼ばれるハード コーディングされたプロファイル セクションで完全に一意の**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティを提供する**MUID_PROFILE_INSTANCE です**。</span><span class="sxs-lookup"><span data-stu-id="f84a4-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f84a4-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f84a4-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f84a4-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f84a4-121">Header files</span></span>

<span data-ttu-id="f84a4-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f84a4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f84a4-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f84a4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f84a4-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f84a4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f84a4-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f84a4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f84a4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f84a4-126">See also</span></span>



[<span data-ttu-id="f84a4-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f84a4-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f84a4-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f84a4-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f84a4-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f84a4-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f84a4-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f84a4-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

