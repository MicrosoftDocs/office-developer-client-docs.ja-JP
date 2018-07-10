---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799990"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="267fb-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="267fb-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="267fb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="267fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="267fb-105">ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するボックスの一覧について説明します。</span><span class="sxs-lookup"><span data-stu-id="267fb-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="267fb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="267fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="267fb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="267fb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="267fb-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="267fb-108">Members</span></span>

 <span data-ttu-id="267fb-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="267fb-109">**ulFlags**</span></span>
  
> <span data-ttu-id="267fb-110">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="267fb-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="267fb-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="267fb-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="267fb-112">PT_MV_TSTRING の種類の複数値を持つプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="267fb-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="267fb-113">このプロパティの値は、ドロップ ダウン リストの個別のエントリとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="267fb-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="267fb-114">備考</span><span class="sxs-lookup"><span data-stu-id="267fb-114">Remarks</span></span>

<span data-ttu-id="267fb-115">**DTBLMVDDLBOX**構造体では、複数値を持つドロップ ダウン リスト項目の読み取り専用の一覧について説明します。</span><span class="sxs-lookup"><span data-stu-id="267fb-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="267fb-116">複数値を持つドロップ ダウン リストを使用すると、ユーザーがスクロール バーをクリックすると値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="267fb-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="267fb-117">データが表示される**ulMVPropTag**のメンバーで識別されるプロパティに由来します。</span><span class="sxs-lookup"><span data-stu-id="267fb-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="267fb-118">ディスプレイ テーブルに関連付けられているプロパティのインターフェイスから参照する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="267fb-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="267fb-119">また、ユーザーがこれらの種類のリスト ボックスから項目を選択をすることができないため、データはプロパティのインターフェイスに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="267fb-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="267fb-120">複数値を持つドロップ ダウン リストの複数値を持つ文字列のプロパティだけがサポートされています。他の複数値を持つプロパティの型はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="267fb-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="267fb-121">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="267fb-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="267fb-122">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="267fb-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="267fb-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="267fb-123">See also</span></span>



[<span data-ttu-id="267fb-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="267fb-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="267fb-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="267fb-125">MAPI Structures</span></span>](mapi-structures.md)
