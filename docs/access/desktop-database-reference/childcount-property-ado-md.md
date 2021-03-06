---
title: childcount プロパティ (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f8e0fc98d7868eb5462bd7d8714e1a8eda1cfcf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296382"
---
# <a name="childcount-property-ado-md"></a>childcount プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

階層内で、現在の [Member](member-object-ado-md.md) オブジェクトが親であるメンバーの数を示します。

## <a name="return-values"></a>戻り値

長整数型 (**Long**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

**ChildCount** プロパティを使用して、 **Member** が持つ子の数の概算を取得します。 **Member** の子自体は、 [Children](children-property-ado-md.md) プロパティを使用して取得します。

**Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトから取得される値は、最大で 65536 です。子の実際の数が 65536 を超える場合でも、取得される値は 65536 となります。そのため、 **ChildCount** が 65536 である場合、アプリケーションは子の数が 65536 または以上であると解釈する必要があります。

**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトの場合、ADO コレクションの [Count](count-property-ado.md) プロパティを **Children** コレクションに使用して、子の正確な数を調べます。コレクション内にある子の数が多い場合、子の正確な数を確認するのに時間がかかることがあります。

