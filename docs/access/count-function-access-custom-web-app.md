---
title: Count 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: クエリまたはテーブルに含まれるレコードの数が返されます。
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419143"
---
# <a name="count-function-access-custom-web-app"></a>Count 関数 (Access カスタム Web アプリ)

クエリまたはテーブルに含まれるレコードの数が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**Count** (*式*) 
  
**Count** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Expression*  <br/> |カウントするデータを含むフィールド、またはフィールド内のデータを使用して計算を実行する式を示す文字列式。 *式のオペランドには*、テーブル フィールドまたは関数の名前を含めできます (組み込み関数またはユーザー定義の場合がありますが、他の集計関数SQLできません)。 テキストを含む任意の種類のデータをカウントできます。  <br/> |
   
## <a name="remarks"></a>注釈

Count 関数を使用すると、元になるクエリのレコード数をカウントできます。たとえば、Count 関数を使用して、特定の国または地域に出荷された注文の数をカウントできます。
  
**Count** (\*) では、グループ内の項目数が返されます。NULL 値および重複する値もカウントされます。 
  

