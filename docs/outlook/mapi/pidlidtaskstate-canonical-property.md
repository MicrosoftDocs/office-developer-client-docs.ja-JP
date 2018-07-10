---
title: PidLidTaskState の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b4bab1948bc563b92dafa16922da3b9760cf1a1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802241"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="13f63-103">PidLidTaskState の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="13f63-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="13f63-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13f63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13f63-105">タスクの現在の割り当ての状態を示します。</span><span class="sxs-lookup"><span data-stu-id="13f63-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13f63-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="13f63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13f63-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="13f63-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="13f63-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="13f63-108">Property set:</span></span>  <br/> |<span data-ttu-id="13f63-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="13f63-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="13f63-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="13f63-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13f63-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="13f63-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="13f63-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="13f63-112">Data type:</span></span>  <br/> |<span data-ttu-id="13f63-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="13f63-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="13f63-114">領域:</span><span class="sxs-lookup"><span data-stu-id="13f63-114">Area:</span></span>  <br/> |<span data-ttu-id="13f63-115">タスク</span><span class="sxs-lookup"><span data-stu-id="13f63-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13f63-116">備考</span><span class="sxs-lookup"><span data-stu-id="13f63-116">Remarks</span></span>

<span data-ttu-id="13f63-117">このプロパティの値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="13f63-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="13f63-118">**値**</span><span class="sxs-lookup"><span data-stu-id="13f63-118">**Value**</span></span>|<span data-ttu-id="13f63-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="13f63-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13f63-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f63-120">0x00000000</span></span>  <br/> |<span data-ttu-id="13f63-121">このタスクは、タスクの辞退に埋め込まれたが、見つかりませんでしたローカルのタスクに対応するように作成されました。</span><span class="sxs-lookup"><span data-stu-id="13f63-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="13f63-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13f63-122">0x00000001</span></span>  <br/> |<span data-ttu-id="13f63-123">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="13f63-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="13f63-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="13f63-124">0x00000002</span></span>  <br/> |<span data-ttu-id="13f63-125">タスクは、割り当てられたタスクのタスク実施者のコピーです。</span><span class="sxs-lookup"><span data-stu-id="13f63-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="13f63-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="13f63-126">0x00000003</span></span>  <br/> |<span data-ttu-id="13f63-127">タスクは、割り当てられたタスクの作業仕事を割り当てた人のコピーです。</span><span class="sxs-lookup"><span data-stu-id="13f63-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="13f63-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="13f63-128">0x00000004</span></span>  <br/> |<span data-ttu-id="13f63-129">辞退されたタスクの作業仕事を割り当てた人のコピーです。</span><span class="sxs-lookup"><span data-stu-id="13f63-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="13f63-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="13f63-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13f63-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="13f63-131">Protocol specifications</span></span>

<span data-ttu-id="13f63-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f63-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f63-133">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="13f63-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13f63-134">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f63-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f63-135">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="13f63-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="13f63-136">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f63-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f63-137">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="13f63-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="13f63-138">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f63-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f63-139">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="13f63-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="13f63-140">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f63-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f63-141">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="13f63-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13f63-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="13f63-142">Header files</span></span>

<span data-ttu-id="13f63-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13f63-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="13f63-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="13f63-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13f63-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="13f63-145">See also</span></span>



[<span data-ttu-id="13f63-146">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="13f63-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13f63-147">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="13f63-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13f63-148">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="13f63-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13f63-149">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="13f63-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
