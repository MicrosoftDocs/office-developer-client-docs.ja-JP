---
title: PidLidAddressBookProviderArrayType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801709"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="69d73-103">PidLidAddressBookProviderArrayType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="69d73-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="69d73-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69d73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69d73-105">連絡先の電子メール アドレスの状態を指定して、ビット フラグのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="69d73-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69d73-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="69d73-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69d73-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="69d73-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="69d73-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="69d73-108">Property set:</span></span>  <br/> |<span data-ttu-id="69d73-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="69d73-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="69d73-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="69d73-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="69d73-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="69d73-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="69d73-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="69d73-112">Data type:</span></span>  <br/> |<span data-ttu-id="69d73-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69d73-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69d73-114">領域:</span><span class="sxs-lookup"><span data-stu-id="69d73-114">Area:</span></span>  <br/> |<span data-ttu-id="69d73-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="69d73-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69d73-116">備考</span><span class="sxs-lookup"><span data-stu-id="69d73-116">Remarks</span></span>

<span data-ttu-id="69d73-117">**DispidABPArrayType**プロパティの値は、連絡先オブジェクトの状態を指定するフラグの組み合わせである必要があります。</span><span class="sxs-lookup"><span data-stu-id="69d73-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="69d73-118">個々 のフラグは、次の表で指定されます。</span><span class="sxs-lookup"><span data-stu-id="69d73-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="69d73-119">このプロパティが設定されている場合、 **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) する必要がありますプロパティ、同様です。</span><span class="sxs-lookup"><span data-stu-id="69d73-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="69d73-120">互いに同期された 2 つのプロパティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69d73-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="69d73-121">などの場合は**dispidABPArrayType**では、ビットが"0x00000001"が設定されて、 **dispidABPEmailList**の値のいずれかの必要があります"0x00000000"です。</span><span class="sxs-lookup"><span data-stu-id="69d73-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="69d73-122">**ビット**</span><span class="sxs-lookup"><span data-stu-id="69d73-122">**Bit**</span></span>|<span data-ttu-id="69d73-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="69d73-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69d73-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="69d73-124">0x00000001</span></span>  <br/> |<span data-ttu-id="69d73-125">連絡先の Email1 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="69d73-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="69d73-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="69d73-126">0x00000002</span></span>  <br/> |<span data-ttu-id="69d73-127">連絡先の電子メール 2 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="69d73-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="69d73-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="69d73-128">0x00000004</span></span>  <br/> |<span data-ttu-id="69d73-129">連絡先の電子メール 3 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="69d73-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="69d73-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="69d73-130">0x00000008</span></span>  <br/> |<span data-ttu-id="69d73-131">連絡先の勤務先ファックスが定義されています。</span><span class="sxs-lookup"><span data-stu-id="69d73-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="69d73-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69d73-132">0x00000010</span></span>  <br/> |<span data-ttu-id="69d73-133">連絡先の自宅の fax が定義されています。</span><span class="sxs-lookup"><span data-stu-id="69d73-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="69d73-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="69d73-134">0x00000020</span></span>  <br/> |<span data-ttu-id="69d73-135">連絡先のプライマリ fax が定義されています。</span><span class="sxs-lookup"><span data-stu-id="69d73-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="69d73-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="69d73-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69d73-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="69d73-137">Protocol specifications</span></span>

<span data-ttu-id="69d73-138">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69d73-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69d73-139">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="69d73-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69d73-140">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69d73-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69d73-141">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="69d73-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69d73-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="69d73-142">Header files</span></span>

<span data-ttu-id="69d73-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69d73-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="69d73-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="69d73-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69d73-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="69d73-145">See also</span></span>



[<span data-ttu-id="69d73-146">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69d73-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69d73-147">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69d73-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69d73-148">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="69d73-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69d73-149">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="69d73-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
