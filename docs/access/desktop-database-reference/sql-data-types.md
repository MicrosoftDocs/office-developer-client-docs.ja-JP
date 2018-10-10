---
title: SQL データ型 (Access データベースをデスクトップ リファレンス)
TOCTitle: SQL Data Types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bb3ce5e0f9c2f89b31a7b7c74fe8eab807116368
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476405"
---
# <a name="sql-data-types"></a><span data-ttu-id="77154-102">SQL データ型</span><span class="sxs-lookup"><span data-stu-id="77154-102">SQL Data Types</span></span>


<span data-ttu-id="77154-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="77154-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="77154-104">Microsoft Access データベース エンジン SQL のデータ型は、Microsoft® Jet データベース エンジンで定義される 13 種類の基本データ型と、それらのデータ型として認識されるいくつかの別名で構成されます。</span><span class="sxs-lookup"><span data-stu-id="77154-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft® Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="77154-p101">これらの基本データ型を次の表に示します。同義語については、「[SQL 予約語](sql-reserved-words.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77154-p101">The following table lists the primary data types. The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77154-107">データ型</span><span class="sxs-lookup"><span data-stu-id="77154-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="77154-108">記憶領域サイズ</span><span class="sxs-lookup"><span data-stu-id="77154-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="77154-109">説明</span><span class="sxs-lookup"><span data-stu-id="77154-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77154-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="77154-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="77154-111">1 文字につき 1 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="77154-p102">このデータ型のフィールドには、どの型のデータでも格納できます。テキスト型 (Text) など、他のデータ型への変換は行われません。フィールドに入力された形式のまま、データが出力されます。</span><span class="sxs-lookup"><span data-stu-id="77154-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-115">BIT</span><span class="sxs-lookup"><span data-stu-id="77154-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="77154-116">1 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="77154-117">Yes または No の値。または、2 つの値のうちのどちらかしか格納できないフィールド。</span><span class="sxs-lookup"><span data-stu-id="77154-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77154-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="77154-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="77154-119">1 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="77154-120">0 ～ 255 の整数値。</span><span class="sxs-lookup"><span data-stu-id="77154-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="77154-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="77154-122">8 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-123">-922,337,203,685,477.5808 ～ 922,337,203,685,477.5807 の範囲の整数。</span><span class="sxs-lookup"><span data-stu-id="77154-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77154-124">DATETIME (ダブルを参照してください)</span><span class="sxs-lookup"><span data-stu-id="77154-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="77154-125">8 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-126">100 ～ 9999 年の日付または時刻の値。</span><span class="sxs-lookup"><span data-stu-id="77154-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="77154-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="77154-128">128 ビット</span><span class="sxs-lookup"><span data-stu-id="77154-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="77154-129">リモート プロシージャ コールで使用される一意な識別番号。</span><span class="sxs-lookup"><span data-stu-id="77154-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77154-130">REAL</span><span class="sxs-lookup"><span data-stu-id="77154-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="77154-131">4 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-132">-3.402823E38 ～ -1.401298E-45 の負の値、1.401298E-45 ～ 3.402823E38 の正の値、および 0 の単精度浮動小数点値</span><span class="sxs-lookup"><span data-stu-id="77154-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="77154-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="77154-134">8 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-135">-1.79769313486232E308 ～ -4.94065645841247E-324 の負の値、4.94065645841247E-324 ～ 1.79769313486232E308 の正の値、および 0 の倍精度浮動小数点値。</span><span class="sxs-lookup"><span data-stu-id="77154-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77154-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="77154-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="77154-137">2 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-p103">-32,768 ～ 32,767 の整数値 (次の「メモ」を参照)。</span><span class="sxs-lookup"><span data-stu-id="77154-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="77154-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="77154-141">4 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-p104">-2,147,483,648 ～ 2,147,483,647 の整数値 (次の「メモ」を参照)。</span><span class="sxs-lookup"><span data-stu-id="77154-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77154-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="77154-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="77154-145">17 バイト</span><span class="sxs-lookup"><span data-stu-id="77154-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="77154-p105">-1028-1 ～ 1028-1 の値を格納する数値データ型。精度 (1 ～ 28) と桁数 (0 ～精度の数値) の両方を定義できます。既定の精度は 18、桁数は 0 です。</span><span class="sxs-lookup"><span data-stu-id="77154-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="77154-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="77154-150">1 文字につき 2 バイト (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="77154-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="77154-151">0 ～ 2.14 GB のデータ。</span><span class="sxs-lookup"><span data-stu-id="77154-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77154-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="77154-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="77154-153">可変</span><span class="sxs-lookup"><span data-stu-id="77154-153">As required</span></span></p></td>
<td><p><span data-ttu-id="77154-p106">0 ～ 2.14 GB のデータ。OLE オブジェクトに使用します。</span><span class="sxs-lookup"><span data-stu-id="77154-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77154-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="77154-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="77154-157">1 文字につき 2 バイト (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="77154-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="77154-158">0 ～ 255 バイトの文字列。</span><span class="sxs-lookup"><span data-stu-id="77154-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="77154-p107"><A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE ステートメント</A>を使用して、シード値とインクリメント値を変更できます。変更した後にテーブルに挿入された行の列には、新しいシード値とインクリメント値に従って自動的に作成された値が格納されます。変更前と変更後のシード値およびインクリメント値に従って作成された値が一致する場合は、複製が作成されます。列が主キーである場合は、新しい列を挿入すると、複製の作成時にエラーになります。</span><span class="sxs-lookup"><span data-stu-id="77154-p107">Both the seed and the increment can be modified using an <A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE statement</A>. New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span></P>
> <LI>
> <P><span data-ttu-id="77154-p108">自動インクリメントが設定されている列に対して最後に使用された値を調べるために、SELECT @@IDENTITY ステートメントを使用することができます。テーブル名を指定することはできません。最後に更新されたテーブルで、自動インクリメントが設定された列に格納されている値が返されます。</span><span class="sxs-lookup"><span data-stu-id="77154-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span></P></LI></UL>

