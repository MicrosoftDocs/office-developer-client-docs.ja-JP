---
title: changefield イベントと FieldChangeComplete イベント (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302486"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>changefield イベントと FieldChangeComplete イベント (ADO)

**適用先:** Access 2013、Office 2013

**WillChangeField** イベントは、保留中の操作で [Recordset](field-object-ado.md) 内の 1 つ以上の [Field](recordset-object-ado.md) オブジェクトの値が変更される前に呼び出されます。 **FieldChangeComplete** イベントは、1 つ以上の **Field** オブジェクトの値が変更された後に呼び出されます。

## <a name="syntax"></a>構文

changefield*cfields*、 *fields*、 *adstatus*、 *precordset*

FieldChangeComplete*cfields*、 *fields*、 **、 *adstatus*、 *precordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*cfields* |*Fields* 内の **Field** オブジェクトの数を表す長整数型 (**Long**) の値です。|
|*フィールド* |**WillChangeField** の場合、*Fields* パラメーターは、元の値と共に **Field** オブジェクトが格納されたバリアント型 (**Variant**) の配列です。 <br/><br/>**FieldChangeComplete** の場合、*Fields* パラメーターは、変更後の値と共に **Field** オブジェクトが格納されたバリアント型 (**Variant**) の配列です。|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 **WillChangeField** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。 <br/><br/>**FieldChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。 <br/><br/>**WillChangeField** から制御が戻る前に保留中の操作の取り消しを要求する場合は、このパラメーターを **adStatusCancel** に設定します。 <br/><br/>**FieldChangeComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*precordset* |**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

**WillChangeField** イベントまたは **FieldChangeComplete** イベントは、[Value](value-property-ado.md) プロパティを設定し、フィールドと値配列パラメーターを指定して [Update](update-method-ado.md) メソッドを呼び出したときに発生します。

