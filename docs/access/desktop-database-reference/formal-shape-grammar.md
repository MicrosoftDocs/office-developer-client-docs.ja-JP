---
title: 正式な Shape 文法
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06548b96a3c23014f23b5123965476c5d1149b6d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479282"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="7b1c7-102">正式な Shape 文法</span><span class="sxs-lookup"><span data-stu-id="7b1c7-102">Formal Shape Grammar</span></span>


<span data-ttu-id="7b1c7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b1c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7b1c7-104">すべての Shape コマンドの作成における正式な文法を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="7b1c7-105">文法的に必須の項は、山かっこ ("\<\>") で区切られたテキスト文字列です。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="7b1c7-106">オプションの項は、角かっこで区切られます ("\[ \]")。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="7b1c7-107">パイプ記号 ("|") は、代替項目であることを示します。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="7b1c7-108">省略符号 ("...") は、繰り返し代替項目であることを示します。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="7b1c7-109">*アルファ*は、アルファベット文字の文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="7b1c7-110">*数字*は、数値の文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="7b1c7-111">*Unicode 文字*は、unicode 数字の文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="7b1c7-112">その他のすべての項はリテラルです。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b1c7-113">項</span><span class="sxs-lookup"><span data-stu-id="7b1c7-113">Term</span></span></p></th>
<th><p><span data-ttu-id="7b1c7-114">定義</span><span class="sxs-lookup"><span data-stu-id="7b1c7-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-115">&lt;shape コマンド&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-116">図形 [&lt;テーブル exp&gt; [AS]&lt;別名&gt;] [&lt;] 図形の操作&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-117">&lt;テーブル exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-118">{&lt;プロバイダー]&gt;} |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="7b1c7-119">(&lt;図形コマンド&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="7b1c7-120">テーブル&lt;引用符で囲まれた名前&gt; |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="7b1c7-121">&lt;引用符で囲まれた名前&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-122">&lt;図形操作&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-123">追加&lt;エイリアス]&gt; |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="7b1c7-124">計算&lt;エイリアス]&gt; [BY&lt;フィールド リスト&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-125">&lt;エイリアスのフィールドの一覧&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-126">&lt;エイリアス フィールド&gt;[、&lt;の別名フィールド.&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-127">&lt;エイリアス フィールド&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-128">&lt;フィールド exp&gt; [AS]&lt;別名&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-129">&lt;フィールド exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-130">(&lt;関係 exp&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-131">&lt;計算 exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="7b1c7-132">&lt;集計 exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="7b1c7-133">&lt;新しい exp 関数&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-135">&lt;テーブル exp&gt; [AS]&lt;別名&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="7b1c7-136">&lt;テーブル exp&gt; [AS]&lt;別名&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-137">&lt;関係の条件の一覧&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-138">&lt;関係条件&gt;[、&lt;関係条件&gt;...]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-139">&lt;関係条件&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-140">&lt;フィールド名&gt;TO&lt;子参照&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-141">&lt;子参照&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-142">&lt;フィールド名&gt; |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="7b1c7-143">パラメーター&lt;パラメーター渡し&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-144">&lt;パラメーター渡し&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-145">&lt;番号&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-146">&lt;フィールド リスト&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-147">&lt;フィールド名&gt;[、&lt;フィールド名&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-148">&lt;集計 exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-149">合計 (&lt;修飾フィールド名&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-150">AVG (&lt;修飾フィールド名&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-151">MIN (&lt;修飾フィールド名&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-152">MAX (&lt;修飾フィールド名&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-153">カウント (&lt;修飾エイリアス&gt; | &lt;修飾名&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-154">STDEV (&lt;修飾フィールド名&gt;)。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7b1c7-155">任意 (&lt;修飾フィールド名&gt;)</span><span class="sxs-lookup"><span data-stu-id="7b1c7-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-156">&lt;計算 exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-157">再計算実行 (&lt;式&gt;)</span><span class="sxs-lookup"><span data-stu-id="7b1c7-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-158">&lt;修飾フィールド名&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-159">&lt;エイリアス&gt;。[&lt;別名&gt;...]&lt;フィールド名&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-160">&lt;エイリアス&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-161">&lt;引用符で囲まれた名前&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-162">&lt;フィールド名&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-163">&lt;引用符で囲まれた名前&gt;[AS]&lt;別名&gt;]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-164">&lt;引用符で囲まれた名前&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-165">&quot;&lt;文字列&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="7b1c7-166">'&lt;文字列&gt;' |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="7b1c7-167">[&lt;文字列&gt;] |</span><span class="sxs-lookup"><span data-stu-id="7b1c7-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="7b1c7-168">&lt;名&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-169">&lt;修飾された名前&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-170">エイリアス [.alias.]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-171">&lt;名&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-172">alpha [アルファ | 数字 | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-173">&lt;番号&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-174">数字 [桁]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-175">&lt;新しい exp 関数&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-176">新しい&lt;フィールドの型&gt;[(&lt;数&gt;[、&lt;数&gt;])]</span><span class="sxs-lookup"><span data-stu-id="7b1c7-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-177">&lt;フィールドの型&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-178">OLE DB または ADO のデータ型</span><span class="sxs-lookup"><span data-stu-id="7b1c7-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1c7-179">&lt;文字列&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-180">unicode 文字 [unicode 文字です..]。</span><span class="sxs-lookup"><span data-stu-id="7b1c7-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1c7-181">&lt;式&gt;</span><span class="sxs-lookup"><span data-stu-id="7b1c7-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="7b1c7-182">同じ行でオペランドが他の非 CALC 列の Visual Basic for Application 式</span><span class="sxs-lookup"><span data-stu-id="7b1c7-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>
