---
title: DATE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: システムの地域設定の短い形式の日付形式に従って、年、月、および日によって表される日付が書式設定を返します。 年、月、および日の値は、グレゴリオ暦のカレンダーを反映します。
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805189"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="ca9e5-104">DATE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ca9e5-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ca9e5-105">システムの地域設定の短い形式の日付形式に従って、*年、月*、*日*によって表される日付が書式設定を返します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="ca9e5-106">*年**月*、および*日*の値は、グレゴリオ暦のカレンダーを反映します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ca9e5-107">構文</span><span class="sxs-lookup"><span data-stu-id="ca9e5-107">Syntax</span></span>

<span data-ttu-id="ca9e5-108">日 (* **年** *、* **月** *、* **日** *)</span><span class="sxs-lookup"><span data-stu-id="ca9e5-108">DATE(** *year* **, ** *month* **, ** *day* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ca9e5-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca9e5-109">Parameters</span></span>

|<span data-ttu-id="ca9e5-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-110">**Name**</span></span>|<span data-ttu-id="ca9e5-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-111">**Required/Optional**</span></span>|<span data-ttu-id="ca9e5-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-112">**Data Type**</span></span>|<span data-ttu-id="ca9e5-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ca9e5-114">_year_</span><span class="sxs-lookup"><span data-stu-id="ca9e5-114">_year_</span></span> <br/> |<span data-ttu-id="ca9e5-115">必須</span><span class="sxs-lookup"><span data-stu-id="ca9e5-115">Required</span></span>  <br/> |<span data-ttu-id="ca9e5-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-116">**Integer**</span></span> <br/> |<span data-ttu-id="ca9e5-117">年を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-117">The year.</span></span>  <br/> |
| <span data-ttu-id="ca9e5-118">_month_</span><span class="sxs-lookup"><span data-stu-id="ca9e5-118">_month_</span></span> <br/> |<span data-ttu-id="ca9e5-119">必須</span><span class="sxs-lookup"><span data-stu-id="ca9e5-119">Required</span></span>  <br/> |<span data-ttu-id="ca9e5-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-120">**Integer**</span></span> <br/> |<span data-ttu-id="ca9e5-121">月を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-121">The month.</span></span>  <br/> |
| <span data-ttu-id="ca9e5-122">_day_</span><span class="sxs-lookup"><span data-stu-id="ca9e5-122">_day_</span></span> <br/> |<span data-ttu-id="ca9e5-123">必須</span><span class="sxs-lookup"><span data-stu-id="ca9e5-123">Required</span></span>  <br/> |<span data-ttu-id="ca9e5-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="ca9e5-124">**Integer**</span></span> <br/> |<span data-ttu-id="ca9e5-125">日を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="ca9e5-126">例 1</span><span class="sxs-lookup"><span data-stu-id="ca9e5-126">Example 1</span></span>

<span data-ttu-id="ca9e5-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="ca9e5-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="ca9e5-128">07.06.99 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ca9e5-129">例 2</span><span class="sxs-lookup"><span data-stu-id="ca9e5-129">Example 2</span></span>

<span data-ttu-id="ca9e5-130">DATE(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="ca9e5-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="ca9e5-131">6/11/1999 を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ca9e5-132">例 3</span><span class="sxs-lookup"><span data-stu-id="ca9e5-132">Example 3</span></span>

<span data-ttu-id="ca9e5-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="ca9e5-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="ca9e5-134">1999 年 10 月 14 日、火曜日を表す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ca9e5-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  
