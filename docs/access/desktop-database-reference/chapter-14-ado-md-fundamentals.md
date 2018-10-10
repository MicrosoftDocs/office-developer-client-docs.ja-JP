---
title: '14 章:  ADO MD に関する基本事項'
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d595136c229234dfa0cb04a44fbe45f58cd79fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477119"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="a0a5f-102">14 章: ADO MD に関する基本事項</span><span class="sxs-lookup"><span data-stu-id="a0a5f-102">Chapter 14: ADO MD Fundamentals</span></span>


<span data-ttu-id="a0a5f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0a5f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a0a5f-p101">Microsoft ActiveX データ オブジェクト (多次元) (ADO MD) を使用すると、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から多次元データに簡単にアクセスできます。ADO MD は Microsoft ActiveX データ オブジェクト (ADO) を拡張したもので、[CubeDef](cubedef-object-ado-md.md) オブジェクトや [Cellset](cellset-object-ado-md.md) オブジェクトのような多次元データ固有のオブジェクトが含まれています。ADO MD を使用すると、多次元スキーマを参照し、キューブにクエリを行い、その結果を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="a0a5f-p102">ADO MD は、ADO と同様に、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用するには、プロバイダーが、OLE DB for OLAP 仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式で表示する表形式データ プロバイダー (TDP) とは対照的に、多次元表示のデータを表します。プロバイダーがサポートしている特定の構文と動作の詳細については、使用する OLAP OLE DB プロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="a0a5f-p103">このマニュアルは、Visual Basic プログラミング言語についての実践的な知識、および ADO と OLAP についての一般的な知識があることを前提としています。詳細については、「[ADO プログラマ ガイド](ado-programmer-s-guide.md)」および「OLE DB Programmer's Reference」 (英語) の OLE DB for OLAP に関する記述を参照してください。ADO MD に関する概要については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-p103">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP. For more information, see the [ADO Programmer's Guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference. For more overview information about ADO MD, see the following topics:</span></span>

  - [<span data-ttu-id="a0a5f-114">多次元スキーマおよびデータの概要</span><span class="sxs-lookup"><span data-stu-id="a0a5f-114">Overview of Multidimensional Schemas and Data</span></span>](overview-of-multidimensional-schemas-and-data.md)

  - [<span data-ttu-id="a0a5f-115">多次元データを処理する</span><span class="sxs-lookup"><span data-stu-id="a0a5f-115">Working with Multidimensional Data</span></span>](working-with-multidimensional-data.md)

  - [<span data-ttu-id="a0a5f-116">ADO と ADO MD を共に使用する</span><span class="sxs-lookup"><span data-stu-id="a0a5f-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)

  - [<span data-ttu-id="a0a5f-117">ADO MD を使ってプログラミングする</span><span class="sxs-lookup"><span data-stu-id="a0a5f-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
