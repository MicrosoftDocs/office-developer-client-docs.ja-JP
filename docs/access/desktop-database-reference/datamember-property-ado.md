---
title: DataMember プロパティ (ADO)
TOCTitle: DataMember Property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a67864ab135c59f146a27f997d4b0df63865a50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479595"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="44715-102">DataMember プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="44715-102">DataMember Property (ADO)</span></span>

<span data-ttu-id="44715-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="44715-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="44715-104">[DataSource](datasource-property-ado.md) プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="44715-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="44715-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="44715-105">Settings and Return Values</span></span>

<span data-ttu-id="44715-p101">**String** の値を設定または取得します。名前の大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="44715-p101">Sets or returns a **String** value. The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="44715-108">解説</span><span class="sxs-lookup"><span data-stu-id="44715-108">Remarks</span></span>

<span data-ttu-id="44715-109">データ環境でのデータ バインド コントロールを作成するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="44715-109">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="44715-110">*.* の[Recordset](recordset-object-ado.md)オブジェクトとして表されるオブジェクト (*データ メンバー*) の名前を格納しているデータ (データ ソース) のコレクションを管理します。</span><span class="sxs-lookup"><span data-stu-id="44715-110">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="44715-111">**DataMember** プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44715-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="44715-p103">**DataMember** プロパティは、 **DataSource** プロパティに指定されたどのオブジェクトを **Recordset** オブジェクトとして表すかを指定します。 **Recordset** オブジェクトは、このプロパティを設定する前に閉じておく必要があります。 **DataSource** プロパティの前に **DataMember** プロパティが設定されていない場合、または **DataMember** 名が、 **DataSource** プロパティに指定されているオブジェクトに認識されない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="44715-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="44715-115">**使用例**</span><span class="sxs-lookup"><span data-stu-id="44715-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```