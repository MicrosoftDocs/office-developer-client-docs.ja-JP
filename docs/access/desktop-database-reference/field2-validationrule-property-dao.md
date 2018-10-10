---
title: Field2.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc2e2bee3a459c2f2b25b26bba4ca2fadd7fb945
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477327"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="2d215-102">Field2.ValidationRule プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d215-102">Field2.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="2d215-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d215-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d215-p101">データの変更時またはテーブルへの追加時 (Microsoft Access ワークスペースのみ) に、フィールド内のデータを検証する値を設定または取得します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2d215-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d215-106">構文</span><span class="sxs-lookup"><span data-stu-id="2d215-106">Syntax</span></span>

<span data-ttu-id="2d215-107">*式*です。"入力規則"</span><span class="sxs-lookup"><span data-stu-id="2d215-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="2d215-108">\*式\***Field2**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d215-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d215-109">注釈</span><span class="sxs-lookup"><span data-stu-id="2d215-109">Remarks</span></span>

<span data-ttu-id="2d215-p102">設定値または戻り値は、WHERE 予約語のない SQL WHERE 句の形式による比較方法が記述された文字列型 (String) の値です。 **[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="2d215-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="2d215-p103">**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d215-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="2d215-115">**Field2** オブジェクトでは、 **ValidationRule** プロパティの使用方法は、 **Field2** オブジェクトを追加する **Fields** コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="2d215-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d215-116">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="2d215-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="2d215-117">使用例</span><span class="sxs-lookup"><span data-stu-id="2d215-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d215-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="2d215-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2d215-119">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="2d215-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d215-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="2d215-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2d215-121">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2d215-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d215-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="2d215-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="2d215-123">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2d215-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d215-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="2d215-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="2d215-125">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="2d215-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d215-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="2d215-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2d215-127">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="2d215-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d215-128">検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2d215-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="2d215-p104">**Field2** オブジェクトの **ValidationRule** プロパティに指定されている文字列式は、その **Field2** オブジェクトのみを参照できます。この式は、ユーザー定義関数、SQL 集計関数、およびクエリは参照できません。 **Field2** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されている場合に、その **ValidationRule** プロパティを設定するには、文字列式が正常に解析され (明示されないオペランドとしてフィールド名を指定)、 **True** に評価されている必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="2d215-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2d215-133">文字列、整数以外の値に連結するプロパティを設定して、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strRule ="価格&gt;" &amp; lngPrice でと lngPrice = 125,50)、エラーが発生時コードでは、任意のデータを検証しようとしています。</span><span class="sxs-lookup"><span data-stu-id="2d215-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="2d215-134">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Acces データベース エンジンの SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="2d215-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>

