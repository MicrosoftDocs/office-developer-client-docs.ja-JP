---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800379"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="e59df-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e59df-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="e59df-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e59df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e59df-105">アドレス帳の既定のコンテナーとして、指定されたコンテナーを確立します。</span><span class="sxs-lookup"><span data-stu-id="e59df-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e59df-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e59df-106">Parameters</span></span>

 <span data-ttu-id="e59df-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e59df-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e59df-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="e59df-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e59df-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e59df-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e59df-110">[in]既定のアドレス帳コンテナーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e59df-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e59df-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e59df-111">Return value</span></span>

<span data-ttu-id="e59df-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e59df-112">S_OK</span></span> 
  
> <span data-ttu-id="e59df-113">既定のアドレス帳コンテナーは正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="e59df-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e59df-114">備考</span><span class="sxs-lookup"><span data-stu-id="e59df-114">Remarks</span></span>

<span data-ttu-id="e59df-115">クライアントとサービス ・ プロバイダーは、新しい既定のアドレス帳コンテナーを確立するために**SetDefaultDir**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e59df-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="e59df-116">既定のコンテナーは、ユーザーに表示されるアドレス帳を最初に開いたときに、アドレス帳に表示されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e59df-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="e59df-117">**SetDefaultDir**は、プロファイル内のエントリとして、既定のコンテナーを保存します。</span><span class="sxs-lookup"><span data-stu-id="e59df-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="e59df-118">コンテナーは、同じセッションで、または別のセッションでは、 **SetDefaultDir**を別の呼び出しが行われるか、コンテナーが削除されるまで、既定値として残ります。</span><span class="sxs-lookup"><span data-stu-id="e59df-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e59df-119">[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティは、アドレス帳のオプション] ダイアログ ボックスで**自動的に選択**の設定に対応しています。</span><span class="sxs-lookup"><span data-stu-id="e59df-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="e59df-120">このプロパティは、 [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx)プロファイル セクション内に存在するし、 **true**に設定されて、アドレス帳ダイアログで不要になった**SetDefaultDir**で指定されたコンテナーのデフォルトですが、Microsoft Outlook を考慮したアドレス帳を選択ダイアログ ボックスが表示されていたコンテキストに適しています。</span><span class="sxs-lookup"><span data-stu-id="e59df-120">When this property exists in the [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="e59df-121">ありますが低い経験ではサード パーティのアドレス帳プロバイダーに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e59df-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e59df-122">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="e59df-122">MFCMAPI reference</span></span>

<span data-ttu-id="e59df-123">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="e59df-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e59df-124">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="e59df-124">**File**</span></span>|<span data-ttu-id="e59df-125">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="e59df-125">**Function**</span></span>|<span data-ttu-id="e59df-126">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="e59df-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e59df-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e59df-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="e59df-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e59df-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="e59df-129">MFCMAPI では、 **SetDefaultDir**メソッドを使用して、既定のいずれかの指定したアドレス帳コンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e59df-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e59df-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e59df-130">See also</span></span>



[<span data-ttu-id="e59df-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e59df-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="e59df-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e59df-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="e59df-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e59df-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="e59df-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="e59df-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="e59df-135">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e59df-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="e59df-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e59df-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
