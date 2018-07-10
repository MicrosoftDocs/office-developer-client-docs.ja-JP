---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9295c37a46d3566089f708aaaa0b9fc3b5f30db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799986"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="68fa5-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="68fa5-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="68fa5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68fa5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68fa5-105">ディスプレイ テーブルから作成されたダイアログ ボックスで使用するグループ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68fa5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="68fa5-106">Header file:</span></span>  <br/> |<span data-ttu-id="68fa5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68fa5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="68fa5-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="68fa5-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="68fa5-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="68fa5-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="68fa5-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="68fa5-110">Members</span></span>

 <span data-ttu-id="68fa5-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="68fa5-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="68fa5-112">グループ ボックスに付属している文字列のメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="68fa5-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="68fa5-113">表示されている場合は、ボックスの上端、左側にあるラベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="68fa5-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="68fa5-114">**ulFlags**</span></span>
  
> <span data-ttu-id="68fa5-115">**UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="68fa5-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="68fa5-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="68fa5-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="68fa5-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68fa5-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="68fa5-118">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="68fa5-118">The label is in Unicode format.</span></span> <span data-ttu-id="68fa5-119">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="68fa5-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68fa5-120">備考</span><span class="sxs-lookup"><span data-stu-id="68fa5-120">Remarks</span></span>

<span data-ttu-id="68fa5-121">**DTBLGROUPBOX**構造体では、ダイアログ ボックスで他のコントロールを視覚的に関連付けるために使用される、グループ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="68fa5-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="68fa5-122">強調表示の方法は、ボックスで他のコントロールを囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="68fa5-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="68fa5-123">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68fa5-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="68fa5-124">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68fa5-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68fa5-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="68fa5-125">See also</span></span>



[<span data-ttu-id="68fa5-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="68fa5-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="68fa5-127">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="68fa5-127">MAPI Structures</span></span>](mapi-structures.md)
