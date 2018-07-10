---
title: PidLidCategories の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801840"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="f010a-103">PidLidCategories の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f010a-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="f010a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f010a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f010a-105">アイテムのカテゴリの一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="f010a-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f010a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f010a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f010a-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="f010a-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="f010a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f010a-108">Property set:</span></span>  <br/> |<span data-ttu-id="f010a-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="f010a-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="f010a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f010a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f010a-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="f010a-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="f010a-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f010a-112">Data type:</span></span>  <br/> |<span data-ttu-id="f010a-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f010a-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f010a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="f010a-114">Area:</span></span>  <br/> |<span data-ttu-id="f010a-115">Common</span><span class="sxs-lookup"><span data-stu-id="f010a-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f010a-116">備考</span><span class="sxs-lookup"><span data-stu-id="f010a-116">Remarks</span></span>

<span data-ttu-id="f010a-117">キーワード ヘッダー フィールドを生成するには、クライアントは、目的の値にこのプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f010a-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="f010a-118">このプロパティは、複数の文字列です。各カテゴリは、1 つのキーワードにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f010a-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="f010a-119">多目的インターネット メール拡張 (MIME) の作成者は、[キーワード] ヘッダー フィールドの (U + 002 C) コンマとスペース (U + 0020) に分離することで別のキーワードをこのプロパティの各部分の値をコピーする必要がありますそれぞれのキーワードです。</span><span class="sxs-lookup"><span data-stu-id="f010a-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="f010a-120">MIME ライターは、さまざまな組織内のカテゴリの別のセットの間に競合を避けるために、[キーワード] ヘッダー フィールドにコピーすることではなく、このプロパティを削除可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f010a-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f010a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f010a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f010a-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f010a-122">Protocol specifications</span></span>

<span data-ttu-id="f010a-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f010a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f010a-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f010a-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f010a-125">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f010a-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f010a-126">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="f010a-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f010a-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f010a-127">Header files</span></span>

<span data-ttu-id="f010a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f010a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f010a-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f010a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f010a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f010a-130">See also</span></span>



[<span data-ttu-id="f010a-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f010a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f010a-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f010a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f010a-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f010a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f010a-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f010a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
