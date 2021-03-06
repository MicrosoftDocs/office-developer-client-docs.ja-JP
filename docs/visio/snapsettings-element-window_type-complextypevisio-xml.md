---
title: SnapSettings 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。
ms.openlocfilehash: 0fbe54f56f79d84e6c6bd8ddc11aa28b7e5ba1dc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540316"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a>SnapSettings 要素 (Window_Type complexType) (Visio XML)

ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio インスタンスで開いているウィンドウを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>注釈

値は、次の表の値の合計である場合があります。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |何もスナップしません。  <br/> |
|1  <br/> |スナップサブディビジョンに設定します。  <br/> |
|2  <br/> |スナップグリッドに移動します。  <br/> |
|4  <br/> |ガイドにスナップします。  <br/> |
|8  <br/> |選択ハンドルにスナップします。  <br/> |
|16   <br/> |頂点にスナップします。  <br/> |
|32  <br/> |接続ポイントにスナップします。  <br/> |
|256  <br/> |スナップ図形の可視エッジに対して表示されます。  <br/> |
|512  <br/> |スナップボックスに配置します。  <br/> |
|1024  <br/> |図形の補助線オプションにスナップします。  <br/> |
|32768  <br/> |スナップ無効です。  <br/> |
|65536  <br/> |交点にスナップします。  <br/> |
   

