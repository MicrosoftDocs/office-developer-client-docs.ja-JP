---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800546"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="ba921-103">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba921-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="ba921-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba921-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba921-105">分散コンピューティング環境では、構成可能な実行時のフォームの使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ba921-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba921-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ba921-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba921-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="ba921-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ba921-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="ba921-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ba921-109">ファクトリ オブジェクトのフォーム</span><span class="sxs-lookup"><span data-stu-id="ba921-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="ba921-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ba921-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba921-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="ba921-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="ba921-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ba921-112">Called by:</span></span>  <br/> |<span data-ttu-id="ba921-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="ba921-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="ba921-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="ba921-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ba921-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="ba921-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="ba921-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="ba921-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ba921-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="ba921-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ba921-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="ba921-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ba921-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="ba921-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="ba921-120">フォームのクラス ファクトリ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="ba921-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="ba921-121">発生しました</span><span class="sxs-lookup"><span data-stu-id="ba921-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="ba921-122">前の工場出荷時のフォーム オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ba921-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="ba921-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="ba921-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="ba921-124">開いているフォームのサーバーは、メモリ内に保持します。</span><span class="sxs-lookup"><span data-stu-id="ba921-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba921-125">備考</span><span class="sxs-lookup"><span data-stu-id="ba921-125">Remarks</span></span>

<span data-ttu-id="ba921-126">[IClassFactory](http://msdn.microsoft.com/ja-jp/library/ms694364%28VS.85%29.aspx)インターフェイスは、 **IMAPIFormFactory**インターフェイスがベースし、 **IMAPIFormFactory**を実装するオブジェクトは、 **IClassFactory**からも継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba921-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](http://msdn.microsoft.com/ja-jp/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="ba921-127">**IMAPIFormFactory**は、フォーム サーバーが 1 つ以上のメッセージ クラスをサポートしている場合、新しいフォーム オブジェクトを作成するフォームの閲覧者が使用するインターフェイス (つまり、1 つ以上の入力フォームのオブジェクトの)。</span><span class="sxs-lookup"><span data-stu-id="ba921-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ba921-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba921-128">See also</span></span>



[<span data-ttu-id="ba921-129">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ba921-129">MAPI Interfaces</span></span>](mapi-interfaces.md)
