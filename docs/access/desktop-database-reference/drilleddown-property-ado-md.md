---
title: drilleddown プロパティ (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293687"
---
# <a name="drilleddown-property-ado-md"></a>drilleddown プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

軸上でメンバーの直下に子がないかどうかを示します。

## <a name="return-values"></a>戻り値

ブール型 (**Boolean**) の値を取得します。値の取得のみが可能です。**DrilledDown** プロパティは、軸上の現在のメンバーに子メンバーがない場合、**True** を返します。軸上の現在のメンバーに 1 つ以上の子メンバーがある場合、**DrilledDown** プロパティは **False** を返します。

## <a name="remarks"></a>注釈

**DrilledDown** プロパティを使用すると、軸上の現在のメンバーの直下に少なくとも 1 つの子があるかどうかを調べることができます。この情報は、メンバーを表示する際に役に立ちます。

このプロパティは、[Position](member-object-ado-md.md) オブジェクトに属している [Member](position-object-ado-md.md) オブジェクトのみでサポートされています。 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。

