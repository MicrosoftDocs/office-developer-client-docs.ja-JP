---
title: ActiveConnection プロパティ (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 037ae753f427c42f147972170dbb2e645b260623
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282531"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection プロパティ (ADO)

**適用先:** Access 2013、Office 2013

指定された [Command](connection-object-ado.md) オブジェクト、 [Recordset](command-object-ado.md) オブジェクト、または [Record](recordset-object-ado.md) オブジェクトが現在属している [Connection](record-object-ado.md) オブジェクトを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

接続が閉じている場合には接続の定義が格納された文字列型 ( **String** ) の値を、接続が開いている場合には現在の **Connection** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を設定または取得します。既定は、Null オブジェクト参照です。 [ConnectionString](connectionstring-property-ado.md) プロパティの説明を参照してください。

## <a name="remarks"></a>注釈

**ActiveConnection** プロパティを使用すると、指定された **Command** オブジェクトを実行する、または指定された **Recordset** を開く **Connection** オブジェクトを調べることができます。

### <a name="command"></a>Command

**Command** オブジェクトの場合、**ActiveConnection** プロパティは値の設定も取得も可能です。

開いている [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) オブジェクトまたは有効な接続文字列をこのプロパティに設定する前に、 **Command** オブジェクトに対して **Execute** を呼び出そうとすると、エラーが発生します。

**Microsoft Visual Basic**: **ActiveConnection**プロパティを*Nothing*に設定すると、現在の**接続**から**Command**オブジェクトを切り離し、プロバイダーがデータに関連付けられているリソースを解放します。ソース. その後は、その **Command** オブジェクトを同じまたは別の **Connection** オブジェクトに関連付けることができます。 プロバイダーによっては、プロパティを*Nothing*に設定しなくても、ある接続から別の**接続**にプロパティ設定を変更することができます。

**Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクションにプロバイダーから供給されたパラメーターが格納されている場合は、**ActiveConnection** プロパティを *Nothing* に設定したり、他の **Connection** オブジェクトに設定したりすると、コレクションがクリアされます。手作業で [Parameter](parameter-object-ado.md) オブジェクトを作成し、それを使用して **Command** オブジェクトの **Parameters** コレクションにデータを格納した場合は、**ActiveConnection** プロパティを *Nothing* や他の **Connection** オブジェクトに設定しても、**Parameters** コレクションはそのまま残されます。

**Command** オブジェクトが関連付けられている **Connection** オブジェクトを閉じると、**ActiveConnection** プロパティが *Nothing* に設定されます。このプロパティに閉じている **Connection** オブジェクトを設定すると、エラーが発生します。

### <a name="recordset"></a>Recordset

開いている **Recordset** オブジェクト、および **Source** プロパティが有効な [Command](source-property-ado-recordset.md) オブジェクトに設定されている **Recordset** オブジェクトについては、 **ActiveConnection** プロパティは値の取得のみ可能です。それ以外の場合は、値の取得および設定が可能です。

このプロパティは、有効な **Connection** オブジェクトまたは有効な接続文字列に設定できます。この場合、プロバイダーが、この定義を使用して新しい **Connection** オブジェクトを作成し、接続を開きます。さらに、プログラマが **Connection** オブジェクトにアクセスして拡張エラー情報を取得したり、その他のコマンドを実行したりできるように、プロバイダーがこのプロパティを新しい **Connection** オブジェクトに設定する場合もあります。

[Open](open-method-ado-recordset.md) メソッドの *ActiveConnection* 引数を使用して **Recordset** オブジェクトを開いた場合、**ActiveConnection** プロパティは引数の値を継承します。

**Recordset** オブジェクトの **Source** プロパティを有効な **Command** オブジェクト変数に設定すると、**Recordset** の **ActiveConnection** プロパティは、**Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。

**リモートデータサービスの使用法**: クライアント側の Recordset オブジェクトで使用されている場合、このプロパティは、接続文字列または (Microsoft visual basic または visual basic, Scripting Edition では) *Nothing*にのみ設定できます。

### <a name="record"></a>Record

このプロパティは、**Record** オブジェクトが閉じている場合には値の設定および取得が可能で、接続文字列または開いている **Connection** オブジェクトの参照を格納できます。**Record** オブジェクトが開いている場合は値の取得のみ可能で、開いている **Connection** オブジェクトの参照が格納されています。

**Connection** オブジェクトは、URL から **Record** オブジェクトが開かれたときに暗黙的に作成されます。 既存の、開いている **Connection** オブジェクトで **Record** を開くには、 **Connection** オブジェクトをこのプロパティに代入するか、または **Connection** オブジェクトを [Open](open-method-ado-record.md) メソッド呼び出しのパラメーターとして使用します。 **record**を既存の**record**または[recordset](recordset-object-ado.md)から開いた場合は、そのレコードまたは**** **recordset**オブジェクトの**Connection**オブジェクトに自動的に関連付けられます。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。



