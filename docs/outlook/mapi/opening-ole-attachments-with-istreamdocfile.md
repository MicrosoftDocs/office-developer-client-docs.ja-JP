---
title: IStreamDocfile で OLE 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326230"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>IStreamDocfile で OLE 添付ファイルを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE オブジェクト添付ファイルを開く場合は、IStream または [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx)ではなく **IStreamDocfile** インターフェイスを使用します。 [](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) 

**IStreamDocfile は** 、構造化ストレージを使用してオブジェクトに直接アクセスできます。コピー操作を実行する必要がなくなります。オーバーヘッドを削減します。 **IStreamDocfile** は **IStream** の特定の実装で、ストリームのコンテンツは構造化ストレージとして書式設定されます。 **IStreamDocfile は** 、メッセージ ストア プロバイダーによって実装されます。 
  

