---
title: FolderUserFields ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800079"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="3c3bc-103">FolderUserFields ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="3c3bc-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="3c3bc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c3bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c3bc-105">このトピックでは、FolderUserFields ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="3c3bc-106">ストリームには、ユーザー定義のフィールドの定義が含まれている`TextField1`。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="3c3bc-107">型は、**テキスト**、および FolderUserFields ストリームには、FolderUserFieldsAnsi と FolderUserFieldsUnicode の両方のパーツが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="3c3bc-108">詳細については、[フォルダー フィールドのストリームの構造体](folder-fields-stream-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="3c3bc-109">データのダンプ</span><span class="sxs-lookup"><span data-stu-id="3c3bc-109">Data dump</span></span>

<span data-ttu-id="3c3bc-110">次のストリームのデータのダンプがバイナリ エディターで表示します。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="3c3bc-111">ストリームのオフセット</span><span class="sxs-lookup"><span data-stu-id="3c3bc-111">Stream offset</span></span>|<span data-ttu-id="3c3bc-112">データのバイト数</span><span class="sxs-lookup"><span data-stu-id="3c3bc-112">Data bytes</span></span>|<span data-ttu-id="3c3bc-113">ASCII データ</span><span class="sxs-lookup"><span data-stu-id="3c3bc-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="3c3bc-114">**FolderUserFields**ストリームのサンプル データの解析は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="3c3bc-115">FolderUserFieldsAnsi: はオフセット 0x0 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="3c3bc-116">FieldDefinitionCount: 0x0 では、4 バイトのオフセット: 0x00000002 (2)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="3c3bc-117">FieldDefinitions: オフセット 0x4、2 つの FolderFieldDefinitionA ストリームの配列。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="3c3bc-118">**配列の最初の要素**。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-118">**First array element**:</span></span>
    
    - <span data-ttu-id="3c3bc-119">FieldType: 0x4、4 バイトのオフセット: 0x00000001 (ftString)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="3c3bc-120">FieldNameLength: 0x8、2 バイトのオフセット: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="3c3bc-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="3c3bc-121">フィールド名: オフセット 0 xa は、10 文字の配列です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="3c3bc-122">ANSI 文字列の値:「TextField1」です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="3c3bc-123">共通: 0x14 をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="3c3bc-124">PropSetGuid: 0x14、16 バイトのオフセット: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="3c3bc-125">fcapm: 0x24、4 バイトのオフセット: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="3c3bc-126">dwString: 4 バイト目の 0x28 にオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-127">dwBitmap: 0x2C、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-128">dwDisplay: 0x30、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-129">iFmt: 0x34, 4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-130">wszFormulaLength: 0x38 は、2 バイトのオフセット: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="3c3bc-131">wszFormula: 0x3A、WCHARs が 0 の配列のオフセット。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="3c3bc-132">空の文字列値です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-132">Empty string value.</span></span>
    
    <span data-ttu-id="3c3bc-133">**2 番目の配列要素**。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="3c3bc-134">FieldType: 0x3A、4 バイトのオフセット: 0x00000000 (ftNone)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="3c3bc-135">FieldNameLength: 0x3E、2 バイトのオフセット: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="3c3bc-136">フィールド名: オフセット 0x40、文字数が 0 の配列です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="3c3bc-137">空の文字列値です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-137">Empty string value.</span></span>
      
    - <span data-ttu-id="3c3bc-138">オフセット 0x40 の一般的な: です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="3c3bc-139">PropSetGuid: 0x40、16 バイトのオフセット: {00000000-0000-0000-0000-000000000000} (GUID_)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="3c3bc-140">fcapm: 0x50、4 バイトのオフセット: 0x00000000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="3c3bc-141">dwString: 0x54、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-142">dwBitmap: 0x58、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-143">dwDisplay: 0x5C、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-144">iFmt: 0x60、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-145">wszFormulaLength: 0x64、2 バイトのオフセット: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="3c3bc-146">wszFormula: 0x66、WCHARs が 0 の配列のオフセット。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="3c3bc-147">空の文字列値です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-147">Empty string value.</span></span>
    
- <span data-ttu-id="3c3bc-148">FolderUserFieldsUnicode: 0x66 をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="3c3bc-149">FieldDefinitionCount: 0x66、4 バイトのオフセット: 0x00000002 (2)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="3c3bc-150">FieldDefinitions: 0x6A、FolderFieldDefinitionW の 2 つのストリームの配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="3c3bc-151">**配列の最初の要素**。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-151">**First array element**:</span></span>
    
    - <span data-ttu-id="3c3bc-152">FieldType: 0x6A、4 バイトのオフセット: 0x00000001 (ftString)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="3c3bc-153">FieldNameLength: 0x6E、2 バイトのオフセット: 0x000A (10)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="3c3bc-154">フィールド名: 0x70、10 WCHARs の配列のオフセットします。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="3c3bc-155">Unicode 文字列の値:「TextField1」です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="3c3bc-156">0x84: 共通のオフセットです。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="3c3bc-157">PropSetGuid: 次の 16 バイトのオフセット: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="3c3bc-158">fcapm: 0x94、4 バイトのオフセット: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="3c3bc-159">dwString: 0x98、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-160">dwBitmap: 0x9C、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-161">dwDisplay: 0xa0 にある、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-162">iFmt: 0xA4、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-163">wszFormulaLength: 0xA8、2 バイトのオフセット: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="3c3bc-164">wszFormula: 0xAA、WCHARs が 0 の配列のオフセット。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="3c3bc-165">空の文字列値です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-165">Empty string value.</span></span>
    
    <span data-ttu-id="3c3bc-166">**2 番目の配列要素**。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="3c3bc-167">FieldType: 0xAA、4 バイトのオフセット: 0x00000000 (ftNone)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="3c3bc-168">FieldNameLength: 0xAE、2 バイトのオフセット: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="3c3bc-169">フィールド名: 0xB0、WCHARs が 0 の配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="3c3bc-170">空の文字列値です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-170">Empty string value.</span></span>
      
    - <span data-ttu-id="3c3bc-171">0xB0: 共通のオフセットです。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="3c3bc-172">PropSetGuid: 0xB0、16 バイトのオフセット: {00000000-0000-0000-0000-000000000000} (GUID_)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="3c3bc-173">fcapm: 0xC0、4 バイトのオフセット: 0x00000000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="3c3bc-174">dwString: 0xC4、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-175">dwBitmap: 0xC8、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-176">dwDisplay: 0xCC、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-177">iFmt: 0xD0、4 バイトのオフセット: 0x00000000 です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="3c3bc-178">wszFormulaLength: 0xD4、2 バイトのオフセット: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="3c3bc-179">wszFormula: ように WCHARs が 0 の配列のオフセット。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="3c3bc-180">空の文字列値です。</span><span class="sxs-lookup"><span data-stu-id="3c3bc-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c3bc-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c3bc-181">See also</span></span>

- [<span data-ttu-id="3c3bc-182">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="3c3bc-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="3c3bc-183">PropertyDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="3c3bc-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="3c3bc-184">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="3c3bc-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="3c3bc-185">SkipBlock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="3c3bc-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="3c3bc-186">FirstSkipBlockContent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="3c3bc-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="3c3bc-187">PackedAnsiString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="3c3bc-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="3c3bc-188">PackedUnicodeString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="3c3bc-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
