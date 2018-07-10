---
title: CharIndex 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798591"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="41a8a-103">CharIndex 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="41a8a-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="41a8a-104">あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。</span><span class="sxs-lookup"><span data-stu-id="41a8a-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="41a8a-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="41a8a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="41a8a-107">構文</span><span class="sxs-lookup"><span data-stu-id="41a8a-107">Syntax</span></span>

<span data-ttu-id="41a8a-108">**CharIndex**(*TextExpression*、 *WithinText*、[*開始*])</span><span class="sxs-lookup"><span data-stu-id="41a8a-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="41a8a-109">**引数名**</span><span class="sxs-lookup"><span data-stu-id="41a8a-109">**Argument Name**</span></span>|<span data-ttu-id="41a8a-110">**必須**</span><span class="sxs-lookup"><span data-stu-id="41a8a-110">**Required**</span></span>|<span data-ttu-id="41a8a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="41a8a-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="41a8a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="41a8a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="41a8a-113">はい</span><span class="sxs-lookup"><span data-stu-id="41a8a-113">Yes</span></span>  <br/> |<span data-ttu-id="41a8a-114">検索するテキストを含むテキスト式。</span><span class="sxs-lookup"><span data-stu-id="41a8a-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="41a8a-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="41a8a-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="41a8a-116">はい</span><span class="sxs-lookup"><span data-stu-id="41a8a-116">Yes</span></span>  <br/> |<span data-ttu-id="41a8a-117">検索するテキスト式。</span><span class="sxs-lookup"><span data-stu-id="41a8a-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="41a8a-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="41a8a-118">*Start*</span></span>  <br/> |<span data-ttu-id="41a8a-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="41a8a-119">No</span></span>  <br/> |<span data-ttu-id="41a8a-120">検索を開始するのには*WithinText*の位置を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="41a8a-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="41a8a-121">*開始*が指定されていないが、負の値または 0 である場合は、 *WithinText*の先頭に、検索が開始されます。</span><span class="sxs-lookup"><span data-stu-id="41a8a-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41a8a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="41a8a-122">Remarks</span></span>

<span data-ttu-id="41a8a-123">*TextExpression*または*WithinText*のいずれかが NULL の場合、 *CharIndex*は NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="41a8a-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="41a8a-124">*WithinText*内で*TextExpression*が見つからない場合、 *CharIndex*は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="41a8a-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="41a8a-125">戻される開始位置は、0 ベースではなく、1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="41a8a-125">The starting position returned is 1-based, not 0-based.</span></span>
  
