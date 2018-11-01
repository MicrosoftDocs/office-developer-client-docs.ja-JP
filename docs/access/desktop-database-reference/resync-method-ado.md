---
title: Resync メソッド (ADO)
TOCTitle: Resync Method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d8e4a863449d8aea5d95002a6183978d9ca953a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884500"
---
# <a name="resync-method-ado"></a><span data-ttu-id="8330a-102">Resync メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="8330a-102">Resync Method (ADO)</span></span>


<span data-ttu-id="8330a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8330a-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="8330a-104">現在の [Recordset](recordset-object-ado.md) オブジェクト、または [Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションのデータを、基になるデータベースのデータで更新します。</span><span class="sxs-lookup"><span data-stu-id="8330a-104">Refreshes the data in the current [Recordset](recordset-object-ado.md) object, or [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, from the underlying database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8330a-105">構文</span><span class="sxs-lookup"><span data-stu-id="8330a-105">Syntax</span></span>

<span data-ttu-id="8330a-106">*レコード セット*です。*AffectRecords*、 *ResyncValues*を再同期します。</span><span class="sxs-lookup"><span data-stu-id="8330a-106">*Recordset*.Resync*AffectRecords*, *ResyncValues*</span></span>

<span data-ttu-id="8330a-107">*レコード*です。</span><span class="sxs-lookup"><span data-stu-id="8330a-107">*Record*.</span></span> <span data-ttu-id="8330a-108">*フィールド*です。*ResyncValues*を再同期します。</span><span class="sxs-lookup"><span data-stu-id="8330a-108">*Fields*.Resync*ResyncValues*</span></span>

## <a name="parameters"></a><span data-ttu-id="8330a-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8330a-109">Parameters</span></span>

  - <span data-ttu-id="8330a-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="8330a-110">*AffectRecords*</span></span>

  - <span data-ttu-id="8330a-p102">省略可能です。 [Resync](affectenum.md) メソッドで操作するレコードの数を決定する **AffectEnum** 値を指定します。既定値は **adAffectAll** です。この値は、 **Record** オブジェクトの **Fields** コレクションに対する **Resync** メソッドでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8330a-p102">Optional. An [AffectEnum](affectenum.md) value that determines how many records the **Resync** method will affect. The default value is **adAffectAll**. This value is not available with the **Resync** method of the **Fields** collection of a **Record** object.</span></span>

  - <span data-ttu-id="8330a-115">*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="8330a-115">*ResyncValues*</span></span>

  - <span data-ttu-id="8330a-p103">省略可能です。基になる値を上書きするかどうかを指定する [ResyncEnum](resyncenum.md) 値を指定します。既定値は **adResyncAllValues** です。</span><span class="sxs-lookup"><span data-stu-id="8330a-p103">Optional. A [ResyncEnum](resyncenum.md) value that specifies whether underlying values are overwritten. The default value is **adResyncAllValues**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8330a-119">解説</span><span class="sxs-lookup"><span data-stu-id="8330a-119">Remarks</span></span>

<span data-ttu-id="8330a-120">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="8330a-120">**Recordset**</span></span>

<span data-ttu-id="8330a-p104">**Resync** メソッドは、現在の **Recordset** のレコードを基になるデータベースと再同期させる場合に使用します。このメソッドは、静的または前方専用のカーソルを使用していて、基になるデータベースの変更を確認する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8330a-p104">Use the **Resync** method to resynchronize records in the current **Recordset** with the underlying database. This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</span></span>

<span data-ttu-id="8330a-123">[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定した場合には、 **Resync** は、読み取り専用ではない **Recordset** オブジェクトに対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8330a-123">If you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**, **Resync** is only available for non-read-only **Recordset** objects.</span></span>

<span data-ttu-id="8330a-p105">[Requery](requery-method-ado.md) メソッドとは異なり、 **Resync** メソッドは、 **Recordset** オブジェクトの基になっているコマンドを再実行しません。基になるデータベースの新しいレコードを参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="8330a-p105">Unlike the [Requery](requery-method-ado.md) method, the **Resync** method does not re-execute the **Recordset** object's underlying command. New records in the underlying database will not be visible.</span></span>

<span data-ttu-id="8330a-p106">基になるデータとの競合 (たとえば、他のユーザーがレコードを削除した場合) が原因で再同期に失敗した場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返し、実行時エラーが発生します。競合しているレコードを特定するには、[Filter](filter-property-ado.md) プロパティ (**adFilterConflictingRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8330a-p106">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterConflictingRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="8330a-128">ダイナミック プロパティ [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) および [Resync Command](resync-command-property-dynamic-ado.md) が設定されていて、 **Recordset** が複数のテーブルに対する JOIN 操作の実行結果である場合、 **Resync** メソッドは、 **Unique Table** プロパティで指定されているテーブルに対してのみ、 **Resync Command** プロパティで指定されているコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8330a-128">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Resync Command](resync-command-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Resync** method will execute the command given in the **Resync Command** property only on the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="8330a-129">**Fields**</span><span class="sxs-lookup"><span data-stu-id="8330a-129">**Fields**</span></span>

<span data-ttu-id="8330a-p107">**Resync** メソッドは、 **Record** オブジェクトの **Fields** コレクションの値を、基になるデータ ソースと再同期させる場合に使用します。 [Count](count-property-ado.md) プロパティは、このメソッドによる影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="8330a-p107">Use the **Resync** method to resynchronize the values of the **Fields** collection of a **Record** object with the underlying data source. The [Count](count-property-ado.md) property is not affected by this method.</span></span>

<span data-ttu-id="8330a-132">*ResyncValues*を**adResyncAllValues** (既定値) に設定し、 [UnderlyingValue](underlyingvalue-property-ado.md)[値](value-property-ado.md)、およびコレクション内の[Field](field-object-ado.md)オブジェクトの[OriginalValue](originalvalue-property-ado.md)プロパティが同期されます。</span><span class="sxs-lookup"><span data-stu-id="8330a-132">If *ResyncValues* is set to **adResyncAllValues** (the default value), then the [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md), and [OriginalValue](originalvalue-property-ado.md) properties of [Field](field-object-ado.md) objects in the collection are synchronized.</span></span> <span data-ttu-id="8330a-133">*ResyncValues*は、**処理**に設定されている場合は、 **UnderlyingValue**プロパティだけが同期されます。</span><span class="sxs-lookup"><span data-stu-id="8330a-133">If *ResyncValues* is set to **adResyncUnderlyingValues**, only the **UnderlyingValue** property is synchronized.</span></span>

<span data-ttu-id="8330a-p109">呼び出し時の各 **Field** オブジェクトの **Status** プロパティの値も、 **Resync** の動作に影響を与えます。 **Status** の値が **adFieldPendingUnknown** または **adFieldPendingInsert** である **Field** オブジェクトに対しては、 **Resync** は何も行いません。 **Status** の値が **adFieldPendingChange** または **adFieldPendingDelete** である場合は、 **Resync** はデータ ソースにまだ存在しているフィールドのデータ値を同期化します。</span><span class="sxs-lookup"><span data-stu-id="8330a-p109">The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**. For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect. For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.</span></span>

<span data-ttu-id="8330a-137">**再同期**は変更されません**フィールド**オブジェクトの**ステータス**の値**の再同期**が呼び出されたときにエラーが発生しません。</span><span class="sxs-lookup"><span data-stu-id="8330a-137">**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called.</span></span> <span data-ttu-id="8330a-138">たとえば、フィールドが存在しない場合、プロバイダーは**adFieldDoesNotExist**など、 **Field**オブジェクトの適切な**ステータス**値を返します。</span><span class="sxs-lookup"><span data-stu-id="8330a-138">For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**.</span></span> <span data-ttu-id="8330a-139">返された**ステータス**値は、 **Status**プロパティの値の中で論理的に組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="8330a-139">Returned **Status** values may be logically combined within the value of the **Status** property.</span></span>

