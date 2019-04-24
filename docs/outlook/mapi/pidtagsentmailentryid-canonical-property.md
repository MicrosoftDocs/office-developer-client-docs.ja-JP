---
title: PidTagSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342512"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="7f1af-103">PidTagSentMailEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f1af-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7f1af-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f1af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f1af-105">送信後にメッセージを移動するフォルダーのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="7f1af-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f1af-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7f1af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f1af-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7f1af-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7f1af-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7f1af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f1af-109">0x0e0a</span><span class="sxs-lookup"><span data-stu-id="7f1af-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="7f1af-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7f1af-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f1af-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f1af-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f1af-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7f1af-112">Area:</span></span>  <br/> |<span data-ttu-id="7f1af-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="7f1af-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f1af-114">解説</span><span class="sxs-lookup"><span data-stu-id="7f1af-114">Remarks</span></span>

<span data-ttu-id="7f1af-115">このプロパティは、多くの場合、 **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) プロパティ、クライアントアプリケーションの標準の [送信済みアイテム] フォルダーからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="7f1af-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="7f1af-116">クライアントアプリケーションは、このプロパティを**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティと共に使用して、メッセージが送信された後の処理を制御します。</span><span class="sxs-lookup"><span data-stu-id="7f1af-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="7f1af-117">どちらか一方を設定する必要がありますが、両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="7f1af-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f1af-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7f1af-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f1af-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7f1af-119">Protocol specifications</span></span>

<span data-ttu-id="7f1af-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f1af-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f1af-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f1af-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f1af-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f1af-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f1af-123">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f1af-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7f1af-124">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f1af-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f1af-125">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="7f1af-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f1af-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7f1af-126">Header files</span></span>

<span data-ttu-id="7f1af-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f1af-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f1af-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f1af-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f1af-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7f1af-129">Mapitags.h</span></span>
  
> <span data-ttu-id="7f1af-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f1af-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f1af-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f1af-131">See also</span></span>



[<span data-ttu-id="7f1af-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7f1af-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f1af-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f1af-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f1af-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7f1af-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f1af-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7f1af-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

