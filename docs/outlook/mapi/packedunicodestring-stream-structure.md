---
title: PackedUnicodeString ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801710"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="13c09-103">PackedUnicodeString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="13c09-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="13c09-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13c09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13c09-105">PackedUnicodeString ストリームの構造体には、Unicode (utf-16) 形式文字列にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="13c09-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="13c09-106">この文字列は null 文字で終了していません。</span><span class="sxs-lookup"><span data-stu-id="13c09-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="13c09-107">このストリーム内のデータ要素は、以下に示す順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。</span><span class="sxs-lookup"><span data-stu-id="13c09-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="13c09-108">存在する実際のデータ要素は、utf-16 形式で文字列の長さによって異なります。</span><span class="sxs-lookup"><span data-stu-id="13c09-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="13c09-109">Utf-16 形式には、255 バイト未満の WCHARs が含まれている文字列のデータ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="13c09-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="13c09-110">長さ: バイト (1 バイト)、utf-16 文字列表現の長さ、WCHARs の数です。</span><span class="sxs-lookup"><span data-stu-id="13c09-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="13c09-111">文字: wchar 型の配列。</span><span class="sxs-lookup"><span data-stu-id="13c09-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="13c09-112">この配列は長さのデータ要素になります。</span><span class="sxs-lookup"><span data-stu-id="13c09-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="13c09-113">配列内のデータは、文字列の utf-16 表現です。</span><span class="sxs-lookup"><span data-stu-id="13c09-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="13c09-114">Utf-16 形式には、255 ~ 65535 WCHARs が含まれている文字列のデータ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="13c09-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="13c09-115">プレフィックス: バイト (1 バイト) で、値の 255 (0 xff) です。</span><span class="sxs-lookup"><span data-stu-id="13c09-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="13c09-116">長さ: ワード (2 バイト)、utf-16 文字列表現の長さ、WCHARs、数です。</span><span class="sxs-lookup"><span data-stu-id="13c09-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="13c09-117">文字: wchar 型の配列。</span><span class="sxs-lookup"><span data-stu-id="13c09-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="13c09-118">この配列は長さのデータ要素になります。</span><span class="sxs-lookup"><span data-stu-id="13c09-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="13c09-119">配列内のデータは、文字列の utf-16 表現です。</span><span class="sxs-lookup"><span data-stu-id="13c09-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13c09-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="13c09-120">See also</span></span>



[<span data-ttu-id="13c09-121">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="13c09-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="13c09-122">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="13c09-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="13c09-123">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="13c09-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
