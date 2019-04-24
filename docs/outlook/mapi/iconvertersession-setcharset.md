---
title: iconvertersessionsetcharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336660"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="f0af1-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="f0af1-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="f0af1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0af1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0af1-105">mapi メッセージを mime ストリームに変換するときに mapi から mime コンバータが使用するオプションの文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="f0af1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f0af1-106">Parameters</span></span>

 <span data-ttu-id="f0af1-107">_fapply_</span><span class="sxs-lookup"><span data-stu-id="f0af1-107">_fApply_</span></span>
  
> <span data-ttu-id="f0af1-108">順番変換に特定の文字セットを使用するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="f0af1-109">このパラメーターを**true**に設定すると、その後の変換で文字セットが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f0af1-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="f0af1-110">特定の文字セットを適用しない場合は、このパラメーターを**false**に設定し、以降のメッセージの既定値に戻します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="f0af1-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="f0af1-111">_hcharset_</span></span>
  
> <span data-ttu-id="f0af1-112">順番Windows メールの mimeole で定義されている文字セットへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="f0af1-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="f0af1-113">特定の文字セットを適用しないように指定するには、 **null**を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="f0af1-114">**null**以外の値の場合は、 [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx)などの関数を使用して、文字セットのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="f0af1-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="f0af1-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="f0af1-116">順番Windows メールの mimeole で定義されているように、文字セットを適用してメッセージを変換する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0af1-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="f0af1-117">Return value</span></span>

<span data-ttu-id="f0af1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0af1-118">S_OK</span></span>
  
> <span data-ttu-id="f0af1-119">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="f0af1-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f0af1-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f0af1-120">MFCMAPI reference</span></span>

<span data-ttu-id="f0af1-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0af1-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f0af1-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f0af1-122">**File**</span></span>|<span data-ttu-id="f0af1-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="f0af1-123">**Function**</span></span>|<span data-ttu-id="f0af1-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f0af1-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0af1-125">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="f0af1-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="f0af1-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="f0af1-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="f0af1-127">mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="f0af1-128">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="f0af1-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="f0af1-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="f0af1-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="f0af1-130">mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="f0af1-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0af1-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0af1-131">See also</span></span>



[<span data-ttu-id="f0af1-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0af1-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="f0af1-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="f0af1-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="f0af1-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="f0af1-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="f0af1-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="f0af1-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="f0af1-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="f0af1-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="f0af1-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="f0af1-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="f0af1-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="f0af1-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

