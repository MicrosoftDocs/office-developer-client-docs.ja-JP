---
title: UpdateOptions プロパティ (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309102"
---
# <a name="recordset2updateoptions-property-dao"></a>UpdateOptions プロパティ (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。UpdateOptions

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

バッチモードの **[Update](recordset2-update-method-dao.md)** を実行すると、DAO とクライアント バッチ カーソル ライブラリによって必要な変更を行う一連の SQL UPDATE ステートメントが作成されます。 更新ごとに、 **[RecordStatus](recordset2-recordstatus-property-dao.md)** プロパティによって変更済みのマークが付けられたレコードを分離する SQL WHERE 句が作成されます。 一部のリモート サーバーではトリガーやその他の方法を使用して参照整合性を強制しているため、多くの場合、更新対象のフィールドを変更の影響を受けるフィールドのみに制限することが重要です。 

そのためには、 **UpdateOptions** プロパティを **dbCriteriaKey**、 **dbCriteriaModValues**、 **dbCriteriaAllCols**、 **dbCriteriaTimeStamp** のいずれかの定数に設定します。 こうすると、必要最低限のトリガー コードが実行されます。 結果として、更新操作が速くなり、エラーの可能性も少なくなります。

また、 **dbCriteriaDeleteInsert** 定数または **dbCriteriaUpdate** 定数を連結すると、バッチ変更をサーバーに返信する際に、各更新に対して SQL DELETE ステートメントと INSERT ステートメントのセット、または SQL UPDATE ステートメントを使用するかどうかを指定できます。前者の場合、レコードの更新には、2 つの異なる操作が必要となります。正しい **UpdateOptions** プロパティの設定を選択すると、パフォーマンスを大幅に向上させることができる場合があります (特にリモート システムに DELETE、INSERT、および UPDATE の各トリガーが実装されている場合)。

定数を指定しない場合、 **dbCriteriaUpdate** および **dbCriteriaKey** が使用されます。

新規レコードの追加では常に INSERT ステートメントが生成され、レコードの削除では常に DELETE ステートメントが生成されるため、このプロパティは、カーソル ライブラリによる変更レコードの更新方法にのみ適用されます。

