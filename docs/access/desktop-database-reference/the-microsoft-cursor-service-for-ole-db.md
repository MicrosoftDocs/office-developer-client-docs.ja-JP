---
title: OLE DB 用 Microsoft Cursor Service
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314358"
---
# <a name="microsoft-cursor-service-for-ole-db"></a>Microsoft Cursor Service for OLE DB


**適用先:** Access 2013、Office 2013

クライアント側カーソルを選択、つまり **CursorLocation** プロパティを **adUseClient** に設定すると、Microsoft Cursor Service for OLE DB が呼び出されます。"Client Cursor Engine" と呼ばれることもありますが、ADO のコンテキストでは本質的に同じ機能を表します。このサービスは、データ プロバイダーのカーソル サポート機能を補完するものです。その結果、すべてのデータ プロバイダーで、比較的一定した機能を得ることができます。

Cursor Service for OLE DB により、動的プロパティが使用できるようになり、一部のメソッドの動作が拡張されます。たとえば、動的プロパティの **Optimize** を使用すると、一時的なインデックスを作成して、 **Find** メソッドなど一部の操作を円滑化できます。

Cursor Service を使用すると、あらゆる場合にバッチ更新が実行できるようになります。また、データ プロバイダーが、静的カーソルなど、機能が限定されたカーソルしかサポートしていない場合でも、動的カーソルなど、より高機能な種類のカーソルをシミュレートすることもできます。

