---
title: フォルダー フォーム ライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414285"
---
# <a name="folder-form-libraries"></a>フォルダー フォーム ライブラリ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
場合によっては、1 つ以上のフォームを特定のフォルダーに関連付ける必要があります。 たとえば、組織内の従業員はすべて、進行状況レポートを作成および保存するための個人用メッセージ ストアに進行状況レポート フォルダーを持つ可能性があります。 進行状況レポートは各ユーザーの進行状況レポート フォルダーに固有なので、進捗レポート フォームをシステム全体のフォーム ライブラリに保存する場合は適切ではない可能性があります。 ただし、進行状況レポート フォームのコピーは、各ユーザーの進行状況レポート フォルダーの関連コンテンツ テーブルに保持できます。 これにより、指定したフォルダーの外部で進行状況レポート フォームを使用するユーザーが制限されます。
  
概念的には、フォーム サーバーがインストールされていない場合でも、メッセージ ストア内のすべてのフォルダーに 1 つのフォルダー フォーム ライブラリがあります。 フォルダー フォーム ライブラリは、他のフォーム ライブラリと同様に実装され、フォルダーの代替部分に関連コンテンツ テーブルとして格納されます。 フォルダー フォーム ライブラリはフォルダーに含まれているため、コピー操作で親フォルダーと共にコピーされます。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

