---
title: 配布リストのメンバーへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412388"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>配布リストのメンバーへのアクセス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **配布リストのメンバーを取得するには**
  
1. PR_ENTRYID ([PidTagEntryId)](pidtagentryid-canonical-property.md) **、PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) **、PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)など、取得するメンバーのプロパティを含むサイズのプロパティ タグ **配列を** 作成します。
    
2. [IAddrBook::OpenEntry を呼び出して](iaddrbook-openentry.md)配布リストを開きます。 
    
3. 配布リストの **IABContainer::GetContentsTable** メソッドを呼び出して、そのコンテンツ テーブルにアクセスします。 
    
4. [HrQueryAllRows を](hrqueryallrows.md)呼び出して、配布リストのメンバーを表すテーブルのすべての行を取得します。 
    

