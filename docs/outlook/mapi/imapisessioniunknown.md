---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a37d8138547c8c4e9308dbb0ebbc6750b152d795
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800715"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="8e0e5-103">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e0e5-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="8e0e5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e0e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e0e5-105">MAPI ログオン セッションに関連付けられているオブジェクトを管理します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e0e5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8e0e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e0e5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="8e0e5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="8e0e5-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8e0e5-109">セッション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e0e5-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="8e0e5-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8e0e5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8e0e5-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="8e0e5-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-112">Called by:</span></span>  <br/> |<span data-ttu-id="8e0e5-113">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="8e0e5-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="8e0e5-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8e0e5-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="8e0e5-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="8e0e5-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8e0e5-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="8e0e5-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8e0e5-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="8e0e5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8e0e5-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="8e0e5-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="8e0e5-120">前のセッションのエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="8e0e5-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="8e0e5-122">セッション ・ プロファイル内のすべてのメッセージ ・ ストアに関する情報を含むメッセージ ストアのテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="8e0e5-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="8e0e5-124">メッセージ ストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="8e0e5-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="8e0e5-126">さらにアクセスするための[IAddrBook](iaddrbookimapiprop.md)ポインターを返す MAPI 統合アドレス帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8e0e5-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="8e0e5-128">現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="8e0e5-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="8e0e5-130">ステータス テーブル、セッション内のすべての MAPI リソースに関する情報が含まれているテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8e0e5-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="8e0e5-132">オブジェクトを開き、さらにアクセスするためのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8e0e5-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="8e0e5-134">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-135">アドバイス</span><span class="sxs-lookup"><span data-stu-id="8e0e5-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="8e0e5-136">セッションに影響を与える特定のイベントの通知を受け取ることを登録します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-137">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="8e0e5-138">**アドバイズ**メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="8e0e5-139">**オプション**</span><span class="sxs-lookup"><span data-stu-id="8e0e5-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="8e0e5-140">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="8e0e5-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="8e0e5-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="8e0e5-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="8e0e5-142">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="8e0e5-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="8e0e5-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="8e0e5-144">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-144">Deprecated.</span></span> <span data-ttu-id="8e0e5-145">セッション内のすべてのトランスポート プロバイダーによって処理可能なアドレスの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="8e0e5-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="8e0e5-147">セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="8e0e5-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="8e0e5-149">MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="8e0e5-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="8e0e5-151">セッションの既定のメッセージ ストアとしてのメッセージ ・ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="8e0e5-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="8e0e5-153">メッセージ サービスを変更する場合、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="8e0e5-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="8e0e5-155">フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="8e0e5-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="8e0e5-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="8e0e5-157">**ShowForm**メソッドを使用してメッセージにアクセスする数値のトークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e0e5-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e0e5-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e0e5-158">See also</span></span>



[<span data-ttu-id="8e0e5-159">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8e0e5-159">MAPI Interfaces</span></span>](mapi-interfaces.md)
