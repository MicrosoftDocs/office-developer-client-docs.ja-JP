---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799988"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="500bc-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="500bc-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="500bc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="500bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="500bc-105">ディスプレイ テーブルから組み込まれているダイアログ ボックスに表示される複数値の一覧について説明します。</span><span class="sxs-lookup"><span data-stu-id="500bc-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="500bc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="500bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="500bc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="500bc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="500bc-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="500bc-108">Members</span></span>

 <span data-ttu-id="500bc-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="500bc-109">**ulFlags**</span></span>
  
> <span data-ttu-id="500bc-110">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="500bc-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="500bc-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="500bc-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="500bc-112">PT_MV_TSTRING の種類の複数値を持つプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="500bc-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="500bc-113">備考</span><span class="sxs-lookup"><span data-stu-id="500bc-113">Remarks</span></span>

<span data-ttu-id="500bc-114">**DTBLMVLISTBOX**構造体では、項目の読み取り専用リストを持つ標準的な複数値を持つリストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="500bc-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="500bc-115">標準的な複数値リストを使用すると、すぐに値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="500bc-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="500bc-116">データが表示される**ulMVPropTag**のメンバーで識別されるプロパティに由来します。</span><span class="sxs-lookup"><span data-stu-id="500bc-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="500bc-117">ディスプレイ テーブルに関連付けられているプロパティのインターフェイスから参照する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="500bc-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="500bc-118">また、ユーザーがこれらの種類のリストから項目を選択することができないため、データはプロパティのインターフェイスに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="500bc-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="500bc-119">複数値リストの複数値を持つ文字列のプロパティだけがサポートされて他の複数値を持つプロパティの型はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="500bc-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="500bc-120">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="500bc-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="500bc-121">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="500bc-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="500bc-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="500bc-122">See also</span></span>



[<span data-ttu-id="500bc-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="500bc-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="500bc-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="500bc-124">MAPI Structures</span></span>](mapi-structures.md)
