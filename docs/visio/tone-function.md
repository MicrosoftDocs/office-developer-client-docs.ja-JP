---
title: TONE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: 色を変更するには、int パラメーターで指定した量によって鮮やかさを減少します。
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806675"
---
# <a name="tone-function"></a><span data-ttu-id="c155f-103">TONE 関数</span><span class="sxs-lookup"><span data-stu-id="c155f-103">TONE Function</span></span>

<span data-ttu-id="c155f-104">色を変更するには、 _int_パラメーターで指定した量によって鮮やかさを減少します。</span><span class="sxs-lookup"><span data-stu-id="c155f-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c155f-105">構文</span><span class="sxs-lookup"><span data-stu-id="c155f-105">Syntax</span></span>

<span data-ttu-id="c155f-106">トーン (* **色** *、* * *int* * *)</span><span class="sxs-lookup"><span data-stu-id="c155f-106">TONE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c155f-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="c155f-107">Parameters</span></span>

|<span data-ttu-id="c155f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c155f-108">**Name**</span></span>|<span data-ttu-id="c155f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c155f-109">**Required/Optional**</span></span>|<span data-ttu-id="c155f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c155f-110">**Data Type**</span></span>|<span data-ttu-id="c155f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c155f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c155f-112">_color_</span><span class="sxs-lookup"><span data-stu-id="c155f-112">_color_</span></span> <br/> |<span data-ttu-id="c155f-113">必須</span><span class="sxs-lookup"><span data-stu-id="c155f-113">Required</span></span>  <br/> |<span data-ttu-id="c155f-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="c155f-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c155f-115">Microsoft Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c155f-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="c155f-116">_int_</span><span class="sxs-lookup"><span data-stu-id="c155f-116">_int_</span></span> <br/> |<span data-ttu-id="c155f-117">必須</span><span class="sxs-lookup"><span data-stu-id="c155f-117">Required</span></span>  <br/> |<span data-ttu-id="c155f-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c155f-118">**Integer**</span></span> <br/> |<span data-ttu-id="c155f-p101">色の鮮やかさを減少する量を指定します。正または負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c155f-p101">The amount by which to decrease the saturation of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c155f-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c155f-121">Return value</span></span>

 <span data-ttu-id="c155f-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="c155f-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c155f-123">備考</span><span class="sxs-lookup"><span data-stu-id="c155f-123">Remarks</span></span>

<span data-ttu-id="c155f-124">鮮やかさの上限と下限は、それぞれ 0 と 240 です。</span><span class="sxs-lookup"><span data-stu-id="c155f-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="c155f-125">_Int_パラメーターに渡すことができます、整数のサイズに制限はありませんが、鮮やかさがこの制限を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="c155f-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  
