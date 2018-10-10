---
title: Open メソッド (ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad4d1c05637f2ff7ef5ff65ec26ab1b721495067
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476206"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="76f01-102">Open メソッド (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="76f01-102">Open Method (ADO MD)</span></span>


<span data-ttu-id="76f01-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="76f01-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="76f01-104">多次元クエリの結果を取得し、結果をセルセットに返します。</span><span class="sxs-lookup"><span data-stu-id="76f01-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f01-105">構文</span><span class="sxs-lookup"><span data-stu-id="76f01-105">Syntax</span></span>

<span data-ttu-id="76f01-106">*セルセット*。オープン*ソース*、 *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="76f01-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="76f01-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76f01-107">Parameters</span></span>

  - <span data-ttu-id="76f01-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="76f01-108">*Source*</span></span>

  - <span data-ttu-id="76f01-109">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="76f01-109">Optional.</span></span> <span data-ttu-id="76f01-110">Multidimensional Expression (MDX) クエリのような有効な多次元クエリを評価するバリアント型 ( **Variant** ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="76f01-110">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="76f01-111">*変換元*の引数は、 [Source](source-property-ado-md.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="76f01-111">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="76f01-112">MDX の詳細については、Microsoft Data Access Components SDK の OLE DB for OLAP のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="76f01-112">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>

  - <span data-ttu-id="76f01-113">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="76f01-113">*ActiveConnection*</span></span>

  - <span data-ttu-id="76f01-114">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="76f01-114">Optional.</span></span> <span data-ttu-id="76f01-115">有効な ADO **Connection** オブジェクトの変数名、または接続の定義のどちらかを指定する文字列を評価するバリアント型 ( [Variant](connection-object-ado.md) ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="76f01-115">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="76f01-116">[Cellset](cellset-object-ado-md.md)オブジェクトを開くときに接続を*暗黙的*に指定します。</span><span class="sxs-lookup"><span data-stu-id="76f01-116">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="76f01-117">この引数に接続の定義を指定すると、ADO により、指定されたパラメーターを使用して新しい接続が開かれます。</span><span class="sxs-lookup"><span data-stu-id="76f01-117">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="76f01-118">*暗黙的*では、 [ActiveConnection](activeconnection-property-ado-md.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="76f01-118">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f01-119">解説</span><span class="sxs-lookup"><span data-stu-id="76f01-119">Remarks</span></span>

<span data-ttu-id="76f01-120">**Open** メソッドのパラメーターのどちらかが省略され、 **Cellset** を開こうとするよりも前に、対応するプロパティ値が設定されていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="76f01-120">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>
