---
title: PidLidCommonEnd の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4aaa8f1c0bb2d9eb43cd1850ea2148151a0f02fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801847"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="9a088-103">PidLidCommonEnd の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9a088-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="9a088-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a088-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a088-105">メッセージの終了日時を表します。</span><span class="sxs-lookup"><span data-stu-id="9a088-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a088-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9a088-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a088-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="9a088-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="9a088-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9a088-108">Property set:</span></span>  <br/> |<span data-ttu-id="9a088-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9a088-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9a088-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9a088-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9a088-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="9a088-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="9a088-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9a088-112">Data type:</span></span>  <br/> |<span data-ttu-id="9a088-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9a088-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9a088-114">領域:</span><span class="sxs-lookup"><span data-stu-id="9a088-114">Area:</span></span>  <br/> |<span data-ttu-id="9a088-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="9a088-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a088-116">備考</span><span class="sxs-lookup"><span data-stu-id="9a088-116">Remarks</span></span>

<span data-ttu-id="9a088-117">このプロパティは、アイテムの終了時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="9a088-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="9a088-118">**DispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) プロパティの値以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a088-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9a088-119">この値は**dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) のプロパティの [世界協定時刻 (UTC) と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a088-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9a088-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9a088-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a088-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9a088-121">Protocol specifications</span></span>

<span data-ttu-id="9a088-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a088-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a088-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a088-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9a088-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a088-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a088-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="9a088-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9a088-126">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a088-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a088-127">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a088-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a088-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9a088-128">Header files</span></span>

<span data-ttu-id="9a088-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a088-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a088-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a088-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a088-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a088-131">See also</span></span>



[<span data-ttu-id="9a088-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a088-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a088-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a088-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a088-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9a088-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a088-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9a088-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
