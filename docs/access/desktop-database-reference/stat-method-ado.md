---
title: Stat メソッドの ActiveX データ オブジェクト (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d2b8c69df8caba93f693194573d057d52dffeb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476670"
---
# <a name="stat-method-ado"></a><span data-ttu-id="501b8-102">Stat メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="501b8-102">Stat Method (ADO)</span></span>


<span data-ttu-id="501b8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="501b8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="501b8-104">**Stream** オブジェクトの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="501b8-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="501b8-105">構文</span><span class="sxs-lookup"><span data-stu-id="501b8-105">Syntax</span></span>

<span data-ttu-id="501b8-106">長*ストリーム*。Stat (*StatStg*、 *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="501b8-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="501b8-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="501b8-107">Return Value</span></span>

<span data-ttu-id="501b8-108">操作の状態を示す長整数型 (Long) の値。</span><span class="sxs-lookup"><span data-stu-id="501b8-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="501b8-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="501b8-109">Parameters</span></span>

  - <span data-ttu-id="501b8-110">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="501b8-110">*StatStg*</span></span>

  - <span data-ttu-id="501b8-p101">ストリームの情報が格納される STATSTG 構造体。ADO の Stream オブジェクトに使用される Stat メソッドの実装は、この構造体のすべてのフィールドに情報を格納するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="501b8-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="501b8-113">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="501b8-113">*StatFlag*</span></span>

  - <span data-ttu-id="501b8-p102">STATSTG 構造体の一部のメンバーが返されないように指定して、メモリ割り当て操作を少なくします。このパラメーターには、STATFLAG 列挙の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="501b8-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="501b8-116">STATFLAG 列挙は 2 つの値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="501b8-116">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="501b8-117">定数</span><span class="sxs-lookup"><span data-stu-id="501b8-117">Constant</span></span></p></th>
    <th><p><span data-ttu-id="501b8-118">値</span><span class="sxs-lookup"><span data-stu-id="501b8-118">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="501b8-119">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="501b8-119">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="501b8-120">0</span><span class="sxs-lookup"><span data-stu-id="501b8-120">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="501b8-121">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="501b8-121">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="501b8-122">1</span><span class="sxs-lookup"><span data-stu-id="501b8-122">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="501b8-123">解説</span><span class="sxs-lookup"><span data-stu-id="501b8-123">Remarks</span></span>

<span data-ttu-id="501b8-124">ADO の Stream オブジェクト用に実装された Stat メソッドは、STATSTG 構造体の以下のフィールドに値を格納します。</span><span class="sxs-lookup"><span data-stu-id="501b8-124">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="501b8-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="501b8-125">*pwcsName*</span></span>

  - <span data-ttu-id="501b8-126">STATFLAG の値がある場合、ストリームの名前を含む文字列と、StatFlag\_NONAME は指定されませんでした。</span><span class="sxs-lookup"><span data-stu-id="501b8-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="501b8-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="501b8-127">*cbSize*</span></span>

  - <span data-ttu-id="501b8-128">ストリームまたはバイト配列のバイト単位でのサイズを示します。</span><span class="sxs-lookup"><span data-stu-id="501b8-128">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="501b8-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="501b8-129">*mtime*</span></span>

  - <span data-ttu-id="501b8-130">この記憶域、ストリーム、またはバイト配列の最終変更時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="501b8-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="501b8-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="501b8-131">*ctime*</span></span>

  - <span data-ttu-id="501b8-132">この記憶域、ストリーム、またはバイト配列の作成時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="501b8-132">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="501b8-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="501b8-133">*atime*</span></span>

  - <span data-ttu-id="501b8-134">この記憶域、ストリーム、またはバイト配列の最終アクセス時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="501b8-134">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="501b8-135">場合 STATFLAG\_NONAME StatFlag パラメーターで指定すると、ストリームの名前は返されません。</span><span class="sxs-lookup"><span data-stu-id="501b8-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="501b8-136">場合 STATFLAG\_NONAME は、StatFlag パラメーターで指定されていませんし、ストリームの現在の名前がないは、E\_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="501b8-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>
