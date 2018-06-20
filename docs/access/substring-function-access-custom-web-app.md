---
title: SubString 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: 文字列式の一部が返されます。
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798752"
---
# <a name="substring-function-access-custom-web-app"></a>SubString 関数 (カスタム web アプリケーションのアクセス)

文字列式の一部が返されます。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **部分文字列**(*TextExpression*、*開始*、*長さ*) 
  
**SubString** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |文字列式を指定します。  <br/> |
| *Start*  <br/> |返される文字の開始位置を指定する整数式。Start が 1 未満の場合、返される式は式に指定された最初の文字から始まります。 この場合、返される文字列の数は、Start + Length - 1 または 0 のいずれか大きい方になります。開始位置が値式の文字数を超える場合は、長さゼロの式が返されます。  <br/> |
| *Length*  <br/> |返される式の文字数を指定する整数式。長さが負数の場合はエラーは生成され、ステートメントが終了します。Start と Length の合計が式の文字数を超える場合は、値式全体が先頭から返されます。  <br/> |
   
