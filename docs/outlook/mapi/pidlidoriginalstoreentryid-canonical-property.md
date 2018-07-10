---
title: PidLidOriginalStoreEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOriginalStoreEntryId
api_type:
- COM
ms.assetid: 1b1fc008-9cd5-49f6-9f91-b59e305a1e82
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aaf442b941cfe14f695bf5e7f7ec246d06e5ae0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802068"
---
# <a name="pidlidoriginalstoreentryid-canonical-property"></a><span data-ttu-id="23654-103">PidLidOriginalStoreEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="23654-103">PidLidOriginalStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="23654-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23654-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23654-105">代理人のストアのエントリ ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="23654-105">Specifies the entry ID of the delegator's store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23654-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="23654-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23654-107">dispidOrigStoreEid</span><span class="sxs-lookup"><span data-stu-id="23654-107">dispidOrigStoreEid</span></span>  <br/> |
|<span data-ttu-id="23654-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="23654-108">Property set:</span></span>  <br/> |<span data-ttu-id="23654-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="23654-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="23654-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="23654-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="23654-111">0x00008237</span><span class="sxs-lookup"><span data-stu-id="23654-111">0x00008237</span></span>  <br/> |
|<span data-ttu-id="23654-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="23654-112">Data type:</span></span>  <br/> |<span data-ttu-id="23654-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="23654-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="23654-114">領域:</span><span class="sxs-lookup"><span data-stu-id="23654-114">Area:</span></span>  <br/> |<span data-ttu-id="23654-115">会議</span><span class="sxs-lookup"><span data-stu-id="23654-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23654-116">備考</span><span class="sxs-lookup"><span data-stu-id="23654-116">Remarks</span></span>

<span data-ttu-id="23654-117">作成または代理人によって更新された会議のオブジェクトに対してこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23654-117">This property should be set on meeting objects which have been created or updated by a delegate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="23654-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23654-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23654-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="23654-119">Protocol specifications</span></span>

<span data-ttu-id="23654-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23654-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23654-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="23654-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23654-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23654-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23654-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="23654-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23654-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="23654-124">Header files</span></span>

<span data-ttu-id="23654-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23654-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="23654-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23654-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23654-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="23654-127">See also</span></span>



[<span data-ttu-id="23654-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23654-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23654-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23654-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23654-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="23654-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23654-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="23654-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
