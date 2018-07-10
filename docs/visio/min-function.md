---
title: MIN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251463
localization_priority: Normal
ms.assetid: b945b7c2-153f-2fc3-b768-1e975254ddf5
description: リストから最小値を返します。 負の無限大に最も近い最小の手段です。
ms.openlocfilehash: a0de95875ea43259d1bd1da19c3e7a4af2ae0f9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805902"
---
# <a name="min-function"></a><span data-ttu-id="961be-104">MIN 関数</span><span class="sxs-lookup"><span data-stu-id="961be-104">MIN Function</span></span>

<span data-ttu-id="961be-105">リストから最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="961be-105">Returns the smallest number from a list.</span></span> <span data-ttu-id="961be-106">負の無限大に最も近い最小の手段です。</span><span class="sxs-lookup"><span data-stu-id="961be-106">Smallest means closest to negative infinity.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="961be-107">構文</span><span class="sxs-lookup"><span data-stu-id="961be-107">Syntax</span></span>

<span data-ttu-id="961be-108">最小 (* * *[数値 1]* * *、* **数値 2* * *,...、* * *numberN* * *)</span><span class="sxs-lookup"><span data-stu-id="961be-108">MIN(** *number1* **, ** *number2* **,..., ** *numberN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="961be-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="961be-109">Parameters</span></span>

|<span data-ttu-id="961be-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="961be-110">**Name**</span></span>|<span data-ttu-id="961be-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="961be-111">**Required/Optional**</span></span>|<span data-ttu-id="961be-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="961be-112">**Data Type**</span></span>|<span data-ttu-id="961be-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="961be-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="961be-114">_number1_</span><span class="sxs-lookup"><span data-stu-id="961be-114">_number1_</span></span> <br/> |<span data-ttu-id="961be-115">必須</span><span class="sxs-lookup"><span data-stu-id="961be-115">Required</span></span>  <br/> |<span data-ttu-id="961be-116">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="961be-116">**Varies**</span></span> <br/> |<span data-ttu-id="961be-117">リスト内の最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="961be-117">The first number in the list.</span></span>  <br/> |
| <span data-ttu-id="961be-118">_number2_</span><span class="sxs-lookup"><span data-stu-id="961be-118">_number2_</span></span> <br/> |<span data-ttu-id="961be-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="961be-119">Optional</span></span>  <br/> |<span data-ttu-id="961be-120">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="961be-120">**Varies**</span></span> <br/> | <span data-ttu-id="961be-121">リスト内の 2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="961be-121">The second number in the list.</span></span>  <br/> |
| <span data-ttu-id="961be-122">_numberN_</span><span class="sxs-lookup"><span data-stu-id="961be-122">_numberN_</span></span> <br/> |<span data-ttu-id="961be-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="961be-123">Optional</span></span>  <br/> |<span data-ttu-id="961be-124">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="961be-124">**Varies**</span></span> <br/> |<span data-ttu-id="961be-125">リスト内の n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="961be-125">The nth number in the list.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="961be-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="961be-126">Return value</span></span>

<span data-ttu-id="961be-127">可変値</span><span class="sxs-lookup"><span data-stu-id="961be-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="961be-128">例</span><span class="sxs-lookup"><span data-stu-id="961be-128">Example</span></span>

<span data-ttu-id="961be-129">MIN(13 in,1 ft, 20 cm)</span><span class="sxs-lookup"><span data-stu-id="961be-129">MIN(13 in,1 ft, 20 cm)</span></span> 
  
<span data-ttu-id="961be-130">20 cm を返します。</span><span class="sxs-lookup"><span data-stu-id="961be-130">Returns 20 centimeters.</span></span> 
  
