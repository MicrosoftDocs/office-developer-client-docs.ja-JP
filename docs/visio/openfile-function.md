---
title: OPENFILE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: まだ開いていない場合Visio Microsoft ドキュメントを開き、ドキュメント ウィンドウをアクティブにします。
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419577"
---
# <a name="openfile-function"></a>OPENFILE 関数

まだ開いていない場合Visio Microsoft ドキュメントを開き、ドキュメント ウィンドウをアクティブにします。
  
## <a name="syntax"></a>構文

 **OPENFILE**( _"filename" )_
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |必須  <br/> |**String** <br/> |開くファイル パスを含むファイルの名前。  <br/> |
   
## <a name="remarks"></a>注釈

複数の OPENFILE 関数を呼び出すと待ち行列に入り、評価する順序に従って実行されます。視覚的な編集ができるように、現在の Visio 図面をアクティブにすると (埋め込み先編集モード)、新しい Visio インスタンスが要求されたファイル名で起動されます。 
  
この関数は常に FALSE を返します。 
  
以前のバージョンの Visio アプリケーションでは、この関数は _OPENFILE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example"></a>例

 `OPENFILE("C:/MyFile.vsdx")`
  
指定したファイル "MyFile.vsdx" を新しいウィンドウで開くか、ファイルが既に開いている場合はウィンドウをアクティブにします。 
  

