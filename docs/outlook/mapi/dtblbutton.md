---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2505f555fd8867fdc24a14f523a74b6f478a3e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799975"
---
# <a name="dtblbutton"></a><span data-ttu-id="2f28f-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="2f28f-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="2f28f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2f28f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2f28f-105">ディスプレイ テーブルから作成されたダイアログ ボックスのボタン コントロールに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f28f-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f28f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2f28f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f28f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f28f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2f28f-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="2f28f-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="2f28f-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="2f28f-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="2f28f-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="2f28f-110">Members</span></span>

 <span data-ttu-id="2f28f-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="2f28f-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="2f28f-112">ボタンに表示される文字の文字列のメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="2f28f-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="2f28f-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2f28f-113">**ulFlags**</span></span>
  
> <span data-ttu-id="2f28f-114">**UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="2f28f-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="2f28f-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2f28f-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="2f28f-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2f28f-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2f28f-117">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="2f28f-117">The label is in Unicode format.</span></span> <span data-ttu-id="2f28f-118">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="2f28f-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="2f28f-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="2f28f-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="2f28f-120">PT_OBJECT [IMAPIControl](imapicontroliunknown.md)インターフェイスを実装する種類のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="2f28f-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="2f28f-121">ボタンをクリックすると、MAPI は、このプロパティを取得するために表示された表の[IMAPIProp](imapipropiunknown.md)の実装の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2f28f-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2f28f-122">備考</span><span class="sxs-lookup"><span data-stu-id="2f28f-122">Remarks</span></span>

<span data-ttu-id="2f28f-123">ボタン コントロールを記述する**DTBLBUTTON**構造体をクリックすると、操作を開始するユーザーに許可します。</span><span class="sxs-lookup"><span data-stu-id="2f28f-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="2f28f-124">通常、ボタンをクリックすると、表示されるモーダル ダイアログ ボックスまたはプログラムのタスクが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2f28f-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="2f28f-125">サービス プロバイダーには、ボタン コントロールで何かを実装できます。</span><span class="sxs-lookup"><span data-stu-id="2f28f-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="2f28f-126">ボタンは、他のコントロールの値に基づいてタスクを実行することになって場合、それらのコントロールが、DT_SET_IMMEDIATE フラグを設定した必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f28f-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="2f28f-127">**UlbLpszLabel**メンバーは、ボタンに表示される文字の文字列のメモリ内の位置です。</span><span class="sxs-lookup"><span data-stu-id="2f28f-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="2f28f-128">サービス プロバイダーは、アンパサンド文字を追加できます (&amp;) ボタンのラベルのウィンドウのアクセラレータを指定します。</span><span class="sxs-lookup"><span data-stu-id="2f28f-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="2f28f-129">アクセラレータ キーを押すとボタンをクリックすると同じ効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="2f28f-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="2f28f-130">**UlPRControl**メンバーは、オブジェクトのプロパティを記述する、 **IMAPIProp::OpenProperty**メソッドを使用する開くと、コントロール オブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2f28f-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="2f28f-131">**IMAPIControl**インターフェイスをサポートするコントロール オブジェクトを実装するは、MAPI 機能を拡張し、ボタンがクリックされたときに発生するタスクまたは操作を定義する方法です。</span><span class="sxs-lookup"><span data-stu-id="2f28f-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="2f28f-132">**IMAPIControl**ボタンを操作するための 2 つの方法を提供する: ボタンとボタンのクリックを処理するために[アクティブ化](imapicontrol-activate.md)を有効または無効にするのには、 [GetState](imapicontrol-getstate.md) 。</span><span class="sxs-lookup"><span data-stu-id="2f28f-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="2f28f-133">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f28f-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2f28f-134">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f28f-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f28f-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f28f-135">See also</span></span>



[<span data-ttu-id="2f28f-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2f28f-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="2f28f-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2f28f-137">MAPI Structures</span></span>](mapi-structures.md)
