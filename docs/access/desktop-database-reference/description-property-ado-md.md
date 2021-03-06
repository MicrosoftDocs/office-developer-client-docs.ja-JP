---
title: Description プロパティ (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293939"
---
# <a name="description-property-ado-md"></a>Description プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

現在のオブジェクトを説明するテキストを取得します。

## <a name="return-values"></a>戻り値

文字列型 (**String**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

[Member](member-object-ado-md.md) オブジェクトでは、 **Description** プロパティはメジャー メンバーと数式メンバーのみに適用されます。これ以外のメンバーに対しては、 **Description** は空の文字列 ("") を返します。メンバーの種類の詳細については、「 [Type プロパティ (ADO MD)](type-property-ado-md.md)」を参照してください。

このプロパティは、**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされています。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。

