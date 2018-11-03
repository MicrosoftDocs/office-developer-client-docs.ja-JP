---
title: ハイブリッド コマンド (デスクトップ データベース参照のアクセス)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946915"
---
# <a name="hybrid-commands"></a><span data-ttu-id="54fb4-102">ハイブリッド コマンド</span><span class="sxs-lookup"><span data-stu-id="54fb4-102">Hybrid commands</span></span>


<span data-ttu-id="54fb4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="54fb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54fb4-p101">ハイブリッド コマンドとは、部分的にパラメーター化されたコマンドを指します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="54fb4-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="54fb4-106">ハイブリッド コマンドのキャッシュ動作は、通常のパラメーター化されたコマンドと同じです。</span><span class="sxs-lookup"><span data-stu-id="54fb4-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

