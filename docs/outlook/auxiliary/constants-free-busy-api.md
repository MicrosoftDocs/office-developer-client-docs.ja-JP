---
title: 定数 (空き時間情報 API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: このトピックでは、空き時間情報 API の定数の定義、クラス識別子、およびインターフェイス識別子について説明します。
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317718"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="eec5e-103">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="eec5e-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="eec5e-104">このトピックでは、空き時間情報 API の定数の定義、クラス識別子、およびインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="eec5e-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="eec5e-105">定数</span><span class="sxs-lookup"><span data-stu-id="eec5e-105">Constants</span></span>

|<span data-ttu-id="eec5e-106">**定数**</span><span class="sxs-lookup"><span data-stu-id="eec5e-106">**Constant**</span></span>|<span data-ttu-id="eec5e-107">**定義**</span><span class="sxs-lookup"><span data-stu-id="eec5e-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eec5e-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="eec5e-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="eec5e-109">*Microsoft Windows Software Development Kit (SDK) ヘッダーファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="eec5e-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="eec5e-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="eec5e-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="eec5e-111">*Windows SDK ヘッダーファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="eec5e-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="eec5e-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="eec5e-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="eec5e-113">*Windows SDK ヘッダーファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="eec5e-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="eec5e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="eec5e-114">S_OK</span></span>  <br/> | <span data-ttu-id="eec5e-115">*Windows SDK ヘッダーファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="eec5e-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="eec5e-116">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="eec5e-116">Interface identifiers</span></span>

<span data-ttu-id="eec5e-117">次のインターフェイス識別子の場合、Windows SDK ヘッダーファイル guiddef で定義されている DEFINE_GUID マクロを使用して、GUID シンボリック名とその値を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eec5e-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="eec5e-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="eec5e-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="eec5e-119">DEFINE_GUID (IID_IEnumFBBlock、0x00067064、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46);</span><span class="sxs-lookup"><span data-stu-id="eec5e-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="eec5e-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="eec5e-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="eec5e-121">DEFINE_GUID (IID_IFreeBusyData、0x00067066、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46);</span><span class="sxs-lookup"><span data-stu-id="eec5e-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="eec5e-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="eec5e-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="eec5e-123">DEFINE_GUID (IID_IFreeBusySupport、0x00067067、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46);</span><span class="sxs-lookup"><span data-stu-id="eec5e-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

