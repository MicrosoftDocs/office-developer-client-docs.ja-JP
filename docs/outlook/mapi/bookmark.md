---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418135"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の位置を記憶するブックマーク データを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するメソッド:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>注釈

MAPI では、次に示す 3 つのブックマークを定義します。
  
BOOKMARK_BEGINNING 
  
> テーブルの開始位置を記憶します。 
    
BOOKMARK_CURRENT 
  
> テーブルの現在の位置を記憶します。
    
BOOKMARK_END 
  
> テーブルの終了位置を記憶します。
    
クライアントは、他のテーブル位置を記憶するために他のブックマークを作成できます。 ブックマークは、テーブルが開いている場合にのみ有効です。 クライアントは、関連付けられたテーブルを閉じる前に、作成したブックマークを解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[MAPI のデータ型](mapi-data-types.md)

