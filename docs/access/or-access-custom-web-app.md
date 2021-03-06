---
title: OR (カスタム Web アプリへのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: 2 つの条件を結合します。2 つの条件のいずれかが true の場合に TRUE を返します。
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414761"
---
# <a name="or-access-custom-web-app"></a>OR (カスタム Web アプリへのアクセス)

2 つの条件を結合します。2 つの条件のいずれかが true の場合に TRUE を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *BooleanExpression* **Or** *BooleanExpression* 
  
**Or** 演算子の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *BooleanExpression*  <br/> |TRUE または FALSE を返す任意の有効な式を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

1 つのステートメント内に複数の論理演算子が使用されている場合、 **Or** 演算子は **And** 演算子の後に評価されます。ただし、かっこを使用すると評価の順序を変更できます。 
  
**Or** 演算子の結果を次の表に示します。 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

