---
title: PidLidAnniversaryEventEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 78096affce8fa03cc3efc8f0ca0c7048c2f9aae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801724"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="0c1f5-103">PidLidAnniversaryEventEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="0c1f5-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0c1f5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c1f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c1f5-105">予定、連絡先の記念日を表すエントリの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c1f5-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c1f5-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="0c1f5-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="0c1f5-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-108">Property set:</span></span>  <br/> |<span data-ttu-id="0c1f5-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="0c1f5-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0c1f5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0c1f5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0c1f5-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="0c1f5-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="0c1f5-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-112">Data type:</span></span>  <br/> |<span data-ttu-id="0c1f5-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0c1f5-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0c1f5-114">領域:</span><span class="sxs-lookup"><span data-stu-id="0c1f5-114">Area:</span></span>  <br/> |<span data-ttu-id="0c1f5-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="0c1f5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c1f5-116">備考</span><span class="sxs-lookup"><span data-stu-id="0c1f5-116">Remarks</span></span>

<span data-ttu-id="0c1f5-117">**DispidAnniversaryEventEID**プロパティで指定された予定は、 **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md))、 **dispidContactLinkSearchKey** ([を使用して、この連絡先にリンクする必要があります。PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md))、および**dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) のプロパティ] で詳細な[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)とします。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c1f5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0c1f5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c1f5-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0c1f5-119">Protocol specifications</span></span>

<span data-ttu-id="0c1f5-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c1f5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c1f5-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c1f5-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c1f5-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c1f5-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c1f5-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0c1f5-124">Header files</span></span>

<span data-ttu-id="0c1f5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c1f5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c1f5-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c1f5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c1f5-127">See also</span></span>



[<span data-ttu-id="0c1f5-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c1f5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c1f5-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c1f5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c1f5-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="0c1f5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c1f5-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="0c1f5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
