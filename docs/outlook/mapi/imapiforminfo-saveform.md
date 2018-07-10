---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5e2d757fe329f9a57447723d72a859c7d82fc2b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800545"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="f2565-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="f2565-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="f2565-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f2565-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f2565-105">構成ファイル内の特定のフォームの説明を保存します。</span><span class="sxs-lookup"><span data-stu-id="f2565-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="f2565-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f2565-106">Parameters</span></span>

 <span data-ttu-id="f2565-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="f2565-107">_szFileName_</span></span>
  
> <span data-ttu-id="f2565-108">[in]説明が保存されているフォームの説明のメッセージ ファイルの名前を示す文字列です。</span><span class="sxs-lookup"><span data-stu-id="f2565-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="f2565-109">このファイル名には、.fdm 拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="f2565-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2565-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f2565-110">Return value</span></span>

<span data-ttu-id="f2565-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2565-111">S_OK</span></span> 
  
> <span data-ttu-id="f2565-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f2565-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f2565-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="f2565-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="f2565-114">構成ファイルに書き込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="f2565-114">The configuration file could not be written.</span></span> <span data-ttu-id="f2565-115">エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2565-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="f2565-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f2565-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f2565-117">**SaveForm**は、ローカルのフォームのコンテナー内のフォームを保存する可能性がありますと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f2565-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="f2565-118">**SaveForm**は、ローカルのフォームのコンテナーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f2565-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f2565-119">備考</span><span class="sxs-lookup"><span data-stu-id="f2565-119">Remarks</span></span>

<span data-ttu-id="f2565-120">クライアント アプリケーションは、指定したファイル名を持つファイルの現在のフォームの説明を保存するのには**IMAPIFormInfo::SaveForm**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2565-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="f2565-121">**SaveForm**は、構成ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2565-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f2565-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f2565-122">Notes to callers</span></span>

<span data-ttu-id="f2565-123">フォーム ライブラリ プロバイダーの表示] ダイアログ ボックスでフォーム記述子メッセージの一覧から選択してフォームを再インストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="f2565-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="f2565-124">フォーム記述子のメッセージに推奨される拡張子は、.fdm です。</span><span class="sxs-lookup"><span data-stu-id="f2565-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="f2565-125">MAPI_E_EXTENDED_ERROR、 **SaveForm**場合、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出すし、エラーが発生した状態を判断するのには返された**MAPIERROR**構造体をチェックします。</span><span class="sxs-lookup"><span data-stu-id="f2565-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2565-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2565-126">See also</span></span>



[<span data-ttu-id="f2565-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f2565-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="f2565-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f2565-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f2565-129">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f2565-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
