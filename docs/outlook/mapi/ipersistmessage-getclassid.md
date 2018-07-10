---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801109"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="d87f4-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="d87f4-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="d87f4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d87f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d87f4-105">フォームを管理するフォームのサーバーを表す識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="d87f4-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="d87f4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d87f4-106">Parameters</span></span>

 <span data-ttu-id="d87f4-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="d87f4-107">_lpClassID_</span></span>
  
> <span data-ttu-id="d87f4-108">[で [チェック アウト]フォームのクラス識別子 (CLSID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d87f4-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d87f4-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d87f4-109">Return value</span></span>

<span data-ttu-id="d87f4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d87f4-110">S_OK</span></span> 
  
> <span data-ttu-id="d87f4-111">クラス識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="d87f4-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d87f4-112">備考</span><span class="sxs-lookup"><span data-stu-id="d87f4-112">Remarks</span></span>

<span data-ttu-id="d87f4-113">**IPersistMessge::GetClassID**メソッドは、フォーム サーバーのクラス id に_lpClassID_パラメーターの内容を設定し、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="d87f4-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="d87f4-114">フォーム ビューアーは、 **GetClassID**を呼び出すし、正常に返されます、フォームが[初期化されていない](uninitialized-state.md)状態で配置されます。</span><span class="sxs-lookup"><span data-stu-id="d87f4-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="d87f4-115">構造化ストレージ オブジェクトのクラス識別子を使用する方法の詳細については、 [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx)メソッドのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d87f4-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d87f4-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d87f4-116">See also</span></span>



[<span data-ttu-id="d87f4-117">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d87f4-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
