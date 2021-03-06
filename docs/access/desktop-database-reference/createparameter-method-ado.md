---
title: createparameter メソッド (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295395"
---
# <a name="createparameter-method-ado"></a>createparameter メソッド (ADO)

**適用先:** Access 2013、Office 2013

指定したプロパティを使用して、新規 [Parameter](parameter-object-ado.md) オブジェクトを作成します。

## <a name="syntax"></a>構文

**設定***パラメーター* = *コマンド*を実行します。createparameter (*Name*、 *Type*、 *Direction*、 *Size*、 *Value*)

## <a name="return-value"></a>戻り値

**Parameter** オブジェクトを返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Name* |省略可能です。 **Parameter** オブジェクト名を含む文字列型 ( **String** ) の値を指定します。|
|*Type* |省略可能です。 [Parameter](datatypeenum.md) オブジェクトのデータ型を **DataTypeEnum** 値で指定します。|
|*Direction* |省略可能です。 [Parameter](parameterdirectionenum.md) オブジェクトのデータ型を **ParameterDirectionEnum** 値で指定します。|
|*Size* |省略可能です。パラメーター値の最大長を文字数またはバイト数で指定する長整数型 ( **Long** ) の値を指定します。|
|*Value* |省略可能です。 **Parameter** オブジェクトの値を指定するバリアント型 ( **Variant** ) の値を指定します。|

## <a name="remarks"></a>注釈

**CreateParameter** メソッドを使用して、名前、種類、方向、サイズ、および値を指定して新規 **Parameter** オブジェクトを作成します。引数に指定した値は、対応する **Parameter** プロパティに書き込まれます。

This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.

*Type* 引数で可変長データ型を指定した場合、**Parameters** コレクションにオブジェクトを追加する前に、*Size* 引数を渡すか、または **Parameter** オブジェクトの [Size](size-property-ado.md) プロパティを設定する必要があります。そのようにしなかった場合はエラーが発生します。

*Type* 引数に数値型 (**adNumeric** または **adDecimal**) を指定する場合は、同時に [NumericScale](numericscale-property-ado.md) プロパティと [Precision](precision-property-ado.md) プロパティも設定する必要があります。

