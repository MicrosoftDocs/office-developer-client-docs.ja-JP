---
title: imapiforminfoopenformcontainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414005"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="b22bf-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="b22bf-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="b22bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b22bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b22bf-105">特定のフォームがインストールされているフォームコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b22bf-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="b22bf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b22bf-106">Parameters</span></span>

 <span data-ttu-id="b22bf-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="b22bf-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="b22bf-108">読み上げ返される form container オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b22bf-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b22bf-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="b22bf-109">Return value</span></span>

<span data-ttu-id="b22bf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b22bf-110">S_OK</span></span> 
  
> <span data-ttu-id="b22bf-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b22bf-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b22bf-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="b22bf-112">See also</span></span>



[<span data-ttu-id="b22bf-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b22bf-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

