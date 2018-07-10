---
title: PidLidEmail2OriginalDisplayName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2b3f59633fcea0b895cd024dbbbc106c8d492bf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801881"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="22b27-103">PidLidEmail2OriginalDisplayName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="22b27-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="22b27-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22b27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22b27-105">連絡先の指定した電子メール アドレスに対応する 2 つ目の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="22b27-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22b27-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="22b27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22b27-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="22b27-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="22b27-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="22b27-108">Property set:</span></span>  <br/> |<span data-ttu-id="22b27-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="22b27-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="22b27-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="22b27-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="22b27-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="22b27-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="22b27-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="22b27-112">Data type:</span></span>  <br/> |<span data-ttu-id="22b27-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="22b27-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="22b27-114">領域:</span><span class="sxs-lookup"><span data-stu-id="22b27-114">Area:</span></span>  <br/> |<span data-ttu-id="22b27-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="22b27-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22b27-116">備考</span><span class="sxs-lookup"><span data-stu-id="22b27-116">Remarks</span></span>

<span data-ttu-id="22b27-117">**DispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) プロパティの値が"SMTP"の場合は、それぞれの**PidLidEmail2OriginalDisplayName**プロパティの値と同じにそれぞれの**の値dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="22b27-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="22b27-118">このプロパティの目的では、 **dispidEmail2EmailAddress**の 1 つに相当する代替のユーザー ・ フレンドリーなアドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="22b27-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22b27-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="22b27-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22b27-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="22b27-120">Protocol specifications</span></span>

<span data-ttu-id="22b27-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22b27-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22b27-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="22b27-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22b27-123">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22b27-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22b27-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="22b27-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22b27-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="22b27-125">Header files</span></span>

<span data-ttu-id="22b27-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22b27-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="22b27-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="22b27-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22b27-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="22b27-128">See also</span></span>



[<span data-ttu-id="22b27-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="22b27-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22b27-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="22b27-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22b27-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="22b27-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22b27-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="22b27-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
