---
title: PidLidTaskAssigner の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5b711b1e0db0fab93016d3f1c979d81a142c9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802195"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="bd53a-103">PidLidTaskAssigner の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bd53a-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="bd53a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd53a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="bd53a-105">名が前回したユーザーにタスクが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="bd53a-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd53a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bd53a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd53a-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="bd53a-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="bd53a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="bd53a-108">Property set:</span></span>  <br/> |<span data-ttu-id="bd53a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="bd53a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="bd53a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bd53a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bd53a-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="bd53a-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="bd53a-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bd53a-112">Data type:</span></span>  <br/> |<span data-ttu-id="bd53a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bd53a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bd53a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="bd53a-114">Area:</span></span>  <br/> |<span data-ttu-id="bd53a-115">タスク</span><span class="sxs-lookup"><span data-stu-id="bd53a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd53a-116">備考</span><span class="sxs-lookup"><span data-stu-id="bd53a-116">Remarks</span></span>

<span data-ttu-id="bd53a-117">タスクが割り当てられていない場合は、このプロパティが未設定のままにします。</span><span class="sxs-lookup"><span data-stu-id="bd53a-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="bd53a-118">クライアントは、タスク実施者が仕事の依頼を受信した後にこのプロパティを設定、ために、タスクの作業仕事を割り当てた人のコピーのプロパティが設定できません。</span><span class="sxs-lookup"><span data-stu-id="bd53a-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="bd53a-119">クライアントを追加または**dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) は、 **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) のプロパティの [タスク] 仕事を割り当てた人リストから仕事を割り当てた人タスクを削除するときに、追加設定をする必要があります。または、タスクが削除された仕事を割り当てた人。</span><span class="sxs-lookup"><span data-stu-id="bd53a-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd53a-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bd53a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd53a-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bd53a-121">Protocol specifications</span></span>

<span data-ttu-id="bd53a-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd53a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd53a-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd53a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd53a-124">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd53a-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd53a-125">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="bd53a-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd53a-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bd53a-126">Header files</span></span>

<span data-ttu-id="bd53a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd53a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd53a-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd53a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd53a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd53a-129">See also</span></span>



[<span data-ttu-id="bd53a-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd53a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd53a-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd53a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd53a-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bd53a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd53a-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bd53a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
