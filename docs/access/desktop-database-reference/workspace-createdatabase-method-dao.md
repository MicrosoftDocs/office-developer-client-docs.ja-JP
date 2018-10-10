---
title: Workspace.CreateDatabase メソッド (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f246ce2cb29ce3933d8102ce51733652709579e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476388"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="19119-102">Workspace.CreateDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="19119-102">Workspace.CreateDatabase Method (DAO)</span></span>


<span data-ttu-id="19119-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="19119-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19119-104">新しい **[Database](database-object-dao.md)** オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた **Database** オブジェクトとして返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="19119-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="19119-105">構文</span><span class="sxs-lookup"><span data-stu-id="19119-105">Syntax</span></span>

<span data-ttu-id="19119-106">*式*です。データベース (***名前***、***接続***、***オプション***)</span><span class="sxs-lookup"><span data-stu-id="19119-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="19119-107">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="19119-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="19119-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19119-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19119-109">名前</span><span class="sxs-lookup"><span data-stu-id="19119-109">Name</span></span></p></th>
<th><p><span data-ttu-id="19119-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="19119-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="19119-111">データ型</span><span class="sxs-lookup"><span data-stu-id="19119-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="19119-112">説明</span><span class="sxs-lookup"><span data-stu-id="19119-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19119-113">名前</span><span class="sxs-lookup"><span data-stu-id="19119-113">Name</span></span></p></td>
<td><p><span data-ttu-id="19119-114">必須</span><span class="sxs-lookup"><span data-stu-id="19119-114">Required</span></span></p></td>
<td><p><span data-ttu-id="19119-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="19119-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-116">作成するデータベース ファイルの名前は、255 文字までの文字列です。</span><span class="sxs-lookup"><span data-stu-id="19119-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="19119-117">完全なパスとファイル名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="19119-117">It can be the full path and file name.</span></span> <span data-ttu-id="19119-118">ネットワークでサポートされている場合は、指定することもネットワーク パスでは、次のように&quot; \\server1\share1\dir1\db1&quot;。</span><span class="sxs-lookup"><span data-stu-id="19119-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="19119-119">のみ、このメソッドを使用して Microsoft Access データベース ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="19119-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-120">ブラウザでの</span><span class="sxs-lookup"><span data-stu-id="19119-120">Connect</span></span></p></td>
<td><p><span data-ttu-id="19119-121">必須</span><span class="sxs-lookup"><span data-stu-id="19119-121">Required</span></span></p></td>
<td><p><span data-ttu-id="19119-122"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="19119-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="19119-p102">[設定] で指定された、データベースを作成する際の照合順序を表す文字列式。この引数を指定しないと、エラーが発生します。  </span><span class="sxs-lookup"><span data-stu-id="19119-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="19119-125">パスワード文字列を連結して、新しい<strong>Database</strong>オブジェクトのパスワードを作成することもできます (で始まる&quot;; pwd =&quot;) を次のように、引数<em>locale</em>の定数。</span><span class="sxs-lookup"><span data-stu-id="19119-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="19119-126">dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="19119-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="19119-127">既定の <em>locale</em> を使用し、パスワードを指定する場合は、単に <em>locale</em> 引数としてパスワード文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="19119-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="19119-128">&quot;pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="19119-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="19119-p103">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="19119-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-134">オプション</span><span class="sxs-lookup"><span data-stu-id="19119-134">Option</span></span></p></td>
<td><p><span data-ttu-id="19119-135">省略可能</span><span class="sxs-lookup"><span data-stu-id="19119-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="19119-136"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="19119-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-p104">1 つ以上のオプションを示す定数 (または定数の組み合わせ)。オプションを組み合わせるには、対応する定数を追加します。</span><span class="sxs-lookup"><span data-stu-id="19119-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="19119-139">注釈</span><span class="sxs-lookup"><span data-stu-id="19119-139">Remarks</span></span>

<span data-ttu-id="19119-140">次の定数のいずれかを引数 locale に使用して、文字列比較を行うテキストの [CollatingOrder](database-collatingorder-property-dao.md) プロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="19119-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19119-141">定数</span><span class="sxs-lookup"><span data-stu-id="19119-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="19119-142">照合順序</span><span class="sxs-lookup"><span data-stu-id="19119-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19119-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="19119-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-144">英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</span><span class="sxs-lookup"><span data-stu-id="19119-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="19119-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-146">アラビア語</span><span class="sxs-lookup"><span data-stu-id="19119-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="19119-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-148">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="19119-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="19119-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-150">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="19119-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="19119-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-152">ロシア語</span><span class="sxs-lookup"><span data-stu-id="19119-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="19119-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-154">チェコ語</span><span class="sxs-lookup"><span data-stu-id="19119-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="19119-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-156">オランダ語</span><span class="sxs-lookup"><span data-stu-id="19119-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="19119-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-158">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="19119-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="19119-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-160">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="19119-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="19119-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-162">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="19119-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="19119-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-164">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="19119-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="19119-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-166">日本語</span><span class="sxs-lookup"><span data-stu-id="19119-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="19119-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-168">韓国語</span><span class="sxs-lookup"><span data-stu-id="19119-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="19119-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-170">北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</span><span class="sxs-lookup"><span data-stu-id="19119-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="19119-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-172">ノルウェー語およびデンマーク語</span><span class="sxs-lookup"><span data-stu-id="19119-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="19119-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-174">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="19119-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="19119-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-176">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="19119-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="19119-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-178">古スペイン語</span><span class="sxs-lookup"><span data-stu-id="19119-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="19119-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-180">スウェーデン語およびフィンランド語</span><span class="sxs-lookup"><span data-stu-id="19119-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="19119-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-182">タイ語</span><span class="sxs-lookup"><span data-stu-id="19119-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="19119-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-184">トルコ語</span><span class="sxs-lookup"><span data-stu-id="19119-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19119-185">次の定数 (複数可) を options 引数に使用して、データ形式のバージョン、およびデータベースを暗号化するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="19119-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19119-186">定数</span><span class="sxs-lookup"><span data-stu-id="19119-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="19119-187">説明</span><span class="sxs-lookup"><span data-stu-id="19119-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19119-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="19119-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-189">暗号化されたデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="19119-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-191">Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="19119-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-193">Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="19119-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-195">Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="19119-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-197">Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 と互換性がある) を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="19119-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-199">Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="19119-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="19119-201">Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19119-202">暗号化の定数を省略した場合は、 **CreateDatabase** により暗号化されていないデータベースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="19119-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="19119-p105">**CreateDatabase** メソッドは、新しい空のデータベースを作成して開き、 **Database** オブジェクトを取得するために使用します。データベースの構造と内容は、別の DAO オブジェクトを使用して指定する必要があります。既存のデータベースの一部または全体をコピーする場合は、 **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** メソッドを使用してカスタマイズ可能なコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="19119-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="19119-206">例</span><span class="sxs-lookup"><span data-stu-id="19119-206">Example</span></span>

<span data-ttu-id="19119-207">次の例では、 **CreateDatabase** メソッドを使用して、新しい暗号化された **Database** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="19119-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```