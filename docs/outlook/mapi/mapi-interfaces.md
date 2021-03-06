---
title: MAPI のインターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422664"
---
# <a name="mapi-interfaces"></a>MAPI のインターフェイス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
各インターフェイスのドキュメントは、インターフェイスの目的の簡単な説明と、次の情報を含むテーブルを含む概要セクションで構成されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |インターフェイスが定義され、ソース コードをコンパイルするときに含める必要があるヘッダー ファイル。  <br/> |
|次のユーザーによって公開されます。  <br/> |インターフェイスを公開するオブジェクト。  <br/> |
|実装元:  <br/> |インターフェイスの実装を提供するコンポーネントの一覧。  <br/> |
|呼び出し元:  <br/> |通常、インターフェイスのメソッドを呼び出すコンポーネントの一覧。  <br/> |
|インターフェイス識別子:  <br/> |インターフェイス識別子 GUID。  <br/> |
|ポインターの種類:  <br/> |インターフェイスを公開するオブジェクトのポインターの種類。  <br/> |
|トランザクション モデル:  <br/> |IMAPIProp から派生した [インターフェイスの場合](imapipropiunknown.md)。 変換されていない場合、変更は直ちに有効になります。トランザクションを実行した場合 [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) が呼び出されるまで、変更は有効ではありません。  <br/> |
   
最初の表の後に、このインターフェイスのすべてのメソッドを vtable の順序で一覧表示する別の表を示します。 vtable は、MAPI オブジェクトのメソッドごとに 1 つの関数ポインターを含むコンパイラによって作成された関数ポインターの配列です。 メソッドは、宣言された順序と同じ順序で一覧表示されます。 他のインターフェイスから継承されたメソッドは、Vtable Order テーブルには表示されませんが、それらを定義するインターフェイスに記載されているのと同じ方法で使用できます。
  
各インターフェイス トピックの後、インターフェイスのメソッドはアルファベット順に文書化されます。 各メソッドについて、ドキュメントには簡単な目的のステートメント、構文ブロック、および次の情報が含まれています。
  
|**見出し**|**Content**|
|:-----|:-----|
|パラメーター  <br/> |メソッド内の各パラメーターの説明。  <br/> |
|戻り値  <br/> |メソッドが返す一意の値の説明。 これらは、呼び出し元がコードでチェックする必要がある値です。  <br/> |
|注釈  <br/> |メソッドの使用理由と使い方の説明。  <br/> |
|関連項目  <br/> |このリファレンスの他のトピックへの相互参照。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI リファレンス](mapi-reference.md)

