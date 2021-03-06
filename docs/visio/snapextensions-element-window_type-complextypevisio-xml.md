---
title: SnapExtensions 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。 値には、次の表の値の合計を指定できます。
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540323"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>SnapExtensions 要素 (Window_Type complexType) (Visio XML)

アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。 値には、次の表の値の合計を指定できます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>注釈

**SnapExtensions** 要素の値は、次の表の値の合計になります。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |何もスナップしません。  <br/> |
|1  <br/> |スナップボックスの拡張子に変更します。  <br/> |
|2  <br/> |スナップ軸の拡張子に移動します。  <br/> |
|4  <br/> |スナップ接線の延長に移動します。  <br/> |
|8  <br/> |スナップエンドポイント拡張機能にアクセスします。  <br/> |
|16   <br/> |スナップ中点の拡張子に変更します。  <br/> |
|32  <br/> |スナップの拡張を指定します。  <br/> |
|64  <br/> |スナップに移動します。  <br/> |
|128  <br/> |スナップ垂直な拡張子に移動します。  <br/> |
|256  <br/> |スナップ垂直な拡張に移動します。  <br/> |
|512  <br/> |スナップの拡張をエンドポイントに移動します。  <br/> |
|1024  <br/> |スナップ垂直方向の拡張機能に移動します。  <br/> |
|2048  <br/> |スナップ中心の拡張子に変換します。  <br/> |
|4096  <br/> |スナップ等角角度の拡張を指定します。  <br/> |
   

