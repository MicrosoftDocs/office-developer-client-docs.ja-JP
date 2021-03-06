---
title: フォーム 管理者がサポートしていない機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419381"
---
# <a name="capabilities-not-supported-by-form-managers"></a>フォーム 管理者がサポートしていない機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の機能は、パフォーマンス上の理由から既定のフォーム マネージャーではサポートされていませんが、カスタム フォーム マネージャーでサポートできます。
  
- フォーム ライブラリ全体でフォームをグループ化または分類できる階層。 フォーム ライブラリは、フォームのフラット ファイル データベースです。
    
- メッセージ クラスまたはスーパークラスに対応するフォームのカテゴリのアクセス制御。
    
- 1 つのフォーム ライブラリで同じフォームの複数の言語バージョンをサポートします。
    
これらは実装の問題です。 カスタム フォーム マネージャーがこれらの機能を実装するのを防ぐものは何もありません。
  
MAPI フォーム アーキテクチャでは、同時に実行される複数のフォーム マネージャーはサポートされていません。 MAPI は複数の同時メッセージ ストア プロバイダー、トランスポート プロバイダー、アドレス帳プロバイダーをサポートしますが、サポートされるフォーム マネージャーは 1 人のみです。
  
一度に実行できるのは 1 つのフォーム マネージャーだけなので、カスタム フォーム マネージャーを実装する場合は、必要な既定のフォーム マネージャーから任意の機能を再実装する必要があります。 カスタム フォーム マネージャーは既定のフォーム マネージャーを完全に置き換えるので、カスタム フォーム マネージャーで重複しない限り、既定のフォーム マネージャーの機能は使用できません。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

