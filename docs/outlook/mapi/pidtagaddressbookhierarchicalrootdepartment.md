---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 49c9b0a80f9bc3b45dfafa6f4e037fe55af289d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802483"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="d3ff6-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="d3ff6-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="d3ff6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3ff6-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d3ff6-105">(HAB) の階層構造のアドレスのルートの識別名 (DN) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3ff6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3ff6-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT、PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="d3ff6-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="d3ff6-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-108">Property set:</span></span>  <br/> |<span data-ttu-id="d3ff6-109">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="d3ff6-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="d3ff6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d3ff6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d3ff6-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="d3ff6-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="d3ff6-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-112">Data type:</span></span>  <br/> |<span data-ttu-id="d3ff6-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d3ff6-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d3ff6-114">領域:</span><span class="sxs-lookup"><span data-stu-id="d3ff6-114">Area:</span></span>  <br/> |<span data-ttu-id="d3ff6-115">Exchange アドレス帳</span><span class="sxs-lookup"><span data-stu-id="d3ff6-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3ff6-116">備考</span><span class="sxs-lookup"><span data-stu-id="d3ff6-116">Remarks</span></span>

<span data-ttu-id="d3ff6-117">これは、グローバル アドレス一覧 (GAL) コンテナーのプロパティであり、階層的なアドレスのルートの識別名を表します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="d3ff6-118">このプロパティは、Active Directory ドメイン サービス (AD DS) しないとオフライン アドレス帳に存在だけです。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="d3ff6-119">呼び出し元は、リモート プロシージャ呼び出しを避けるために GetProps 呼び出しに MAPI_CACHE_ONLY を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="d3ff6-120">これが存在しない場合、呼び出し元は、ルート部署が見つかりません PT_OBJECT の種類は、PR_EMS_AB_HAB_ROOT_DEPARTMENT を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="d3ff6-121">ルート部署が取得した後は、MAPI_MAILUSER または MAPI_DISTLIST オブジェクトの種類があります。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="d3ff6-122">オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマを採用します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="d3ff6-123">オブジェクトの種類が MAPI_MAILUSER の場合は、前のスキーマを採用されています。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="d3ff6-124">Microsoft Office Outlook 2007 Service Pack 2 には、両方のスキーマがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="d3ff6-125">Microsoft Outlook 2010 および Microsoft Outlook 2013 は、新しいスキーマをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="d3ff6-126">新しいスキーマで部門のすべてのグループも、配布リスト、MAPI_DISTLIST の種類の。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="d3ff6-127">部門のグループ、および部門別のグループ内の部門のメンバーを取得するには、配布リストのメンバーと同様に PR_EMS_AB_MEMBER を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="d3ff6-128">ルート部署が取得した後は、MAPI_MAILUSER または MAPI_DISTLIST オブジェクトの種類があります。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="d3ff6-129">オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="d3ff6-130">オブジェクトの種類が MAPI_MAILUSER の場合は、古いスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="d3ff6-131">新しいスキーマですべての部門別のグループも Dl、型 MAPI_DISTLIST の。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d3ff6-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d3ff6-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3ff6-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d3ff6-133">Protocol specifications</span></span>

<span data-ttu-id="d3ff6-134">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3ff6-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3ff6-135">プロパティ セットの定義と関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3ff6-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d3ff6-136">Header files</span></span>

<span data-ttu-id="d3ff6-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3ff6-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3ff6-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3ff6-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3ff6-139">See also</span></span>



[<span data-ttu-id="d3ff6-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d3ff6-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3ff6-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d3ff6-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3ff6-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="d3ff6-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3ff6-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="d3ff6-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
