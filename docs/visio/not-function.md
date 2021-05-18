---
title: NOT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: 論理式が FALSE の場合は TRUE (1) を返します。 それ以外の場合は、FALSE (0) を返します。
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413333"
---
# <a name="not-function"></a><span data-ttu-id="17e82-104">NOT 関数</span><span class="sxs-lookup"><span data-stu-id="17e82-104">NOT Function</span></span>

<span data-ttu-id="17e82-105">論理式が FALSE の場合は TRUE (1)  _を_ 返します。</span><span class="sxs-lookup"><span data-stu-id="17e82-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="17e82-106">それ以外の場合は、FALSE (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="17e82-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="17e82-107">構文</span><span class="sxs-lookup"><span data-stu-id="17e82-107">Syntax</span></span>

<span data-ttu-id="17e82-108">NOT(\*\* *logicalexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="17e82-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="17e82-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="17e82-109">Parameters</span></span>

|<span data-ttu-id="17e82-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="17e82-110">**Name**</span></span>|<span data-ttu-id="17e82-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="17e82-111">**Required/Optional**</span></span>|<span data-ttu-id="17e82-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="17e82-112">**Data Type**</span></span>|<span data-ttu-id="17e82-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="17e82-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="17e82-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="17e82-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="17e82-115">必須</span><span class="sxs-lookup"><span data-stu-id="17e82-115">Required</span></span>  <br/> |<span data-ttu-id="17e82-116">**String**</span><span class="sxs-lookup"><span data-stu-id="17e82-116">**String**</span></span> <br/> |<span data-ttu-id="17e82-117">評価する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="17e82-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="17e82-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="17e82-118">Return value</span></span>

<span data-ttu-id="17e82-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="17e82-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="17e82-120">例</span><span class="sxs-lookup"><span data-stu-id="17e82-120">Example</span></span>

<span data-ttu-id="17e82-121">NOT(Height \> 0.75 in)</span><span class="sxs-lookup"><span data-stu-id="17e82-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="17e82-p103">Height が 0.75 インチ以下の場合は、1 を返します。Height が 0.75 インチより大きい場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="17e82-p103">Returns 1 if Height is less than or equal to 0.75 inches. Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

