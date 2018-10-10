---
title: Document.CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 95c2454b81cc46ee2df59b05ce7ea06f78a783ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477803"
---
# <a name="documentcreateproperty-method-dao"></a><span data-ttu-id="fd575-102">Document.CreateProperty メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="fd575-102">Document.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="fd575-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd575-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fd575-104">新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fd575-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd575-105">構文</span><span class="sxs-lookup"><span data-stu-id="fd575-105">Syntax</span></span>

<span data-ttu-id="fd575-106">*式*です。CreateProperty (***名前***、***型***、***値***、 ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="fd575-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="fd575-107">\*式\***ドキュメント**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="fd575-107">*expression* A variable that represents a **Document** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="fd575-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fd575-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd575-109">名前</span><span class="sxs-lookup"><span data-stu-id="fd575-109">Name</span></span></p></th>
<th><p><span data-ttu-id="fd575-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="fd575-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="fd575-111">データ型</span><span class="sxs-lookup"><span data-stu-id="fd575-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="fd575-112">説明</span><span class="sxs-lookup"><span data-stu-id="fd575-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd575-113">名前</span><span class="sxs-lookup"><span data-stu-id="fd575-113">Name</span></span></p></td>
<td><p><span data-ttu-id="fd575-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="fd575-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="fd575-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="fd575-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="fd575-p101">新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="fd575-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd575-118">種類</span><span class="sxs-lookup"><span data-stu-id="fd575-118">Type</span></span></p></td>
<td><p><span data-ttu-id="fd575-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="fd575-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="fd575-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="fd575-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="fd575-p102">新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="fd575-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd575-123">値</span><span class="sxs-lookup"><span data-stu-id="fd575-123">Value</span></span></p></td>
<td><p><span data-ttu-id="fd575-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="fd575-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="fd575-125"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="fd575-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="fd575-p103">初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="fd575-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd575-128">DDL</span><span class="sxs-lookup"><span data-stu-id="fd575-128">DDL</span></span></p></td>
<td><p><span data-ttu-id="fd575-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="fd575-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="fd575-130"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="fd575-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="fd575-131"><strong>バリアント型</strong>(<strong>ブール型</strong>のサブタイプ)<strong>プロパティ</strong>は、DDL オブジェクトであるかどうかを示す。</span><span class="sxs-lookup"><span data-stu-id="fd575-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="fd575-132">既定では <strong>False です</strong> 。</span><span class="sxs-lookup"><span data-stu-id="fd575-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="fd575-133">DDL が<strong>True</strong>の場合は、ユーザーが変更または<strong>dbSecWriteDef</strong>権限を持たない<strong>プロパティ</strong>オブジェクトを削除できません。</span><span class="sxs-lookup"><span data-stu-id="fd575-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fd575-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="fd575-134">Return Value</span></span>

<span data-ttu-id="fd575-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd575-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="fd575-136">注釈</span><span class="sxs-lookup"><span data-stu-id="fd575-136">Remarks</span></span>

<span data-ttu-id="fd575-137">ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。</span><span class="sxs-lookup"><span data-stu-id="fd575-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="fd575-p105">**CreateProperty** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd575-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="fd575-141">名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="fd575-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="fd575-p106">ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 [Properties](fields-delete-method-dao.md) コレクションの \*\*\*\*Delete\*\*\*\* メソッドを使用します。組み込みのプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="fd575-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd575-144">DDL 引数を省略した場合のデフォルト値は False (DDL 以外)。</span><span class="sxs-lookup"><span data-stu-id="fd575-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="fd575-145">対応する DDL プロパティは公開されていないので、DDL から DDL 以外に変更する <STRONG>Property</STRONG> オブジェクトを削除し、再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd575-145">Because no corresponding DDL property is exposed, you must delete and re-create a <STRONG>Property</STRONG> object you want to change from DDL to non-DDL.</span></span></P>

