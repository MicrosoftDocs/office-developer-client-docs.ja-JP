---
title: QueryDef メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301121"
---
# <a name="querydefcancel-method-dao"></a>QueryDef メソッド (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。キャンセル

*式***QueryDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Cancel**メソッドを使用して、非同期の**Execute**メソッドまたは**openconnection**メソッドの呼び出し (つまり、dbrunasync オプションを指定してメソッドが呼び出された場合) の実行を終了します。 終了しようとしているメソッドで dbrunasync が使用されていない場合、 **Cancel**は実行時エラーを返します。

