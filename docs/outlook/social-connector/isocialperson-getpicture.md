---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: ユーザーのピクチャ リソースを含むバイトの配列を取得します。
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406711"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

ユーザーのピクチャ リソースを含むバイトの配列を取得します。 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>パラメーター

_図_
  
> [out]人物のピクチャ リソースを表すバイトの配列を指定する構造体へのポインター。
    
## <a name="remarks"></a>注釈

サポートされているピクチャ リソースは、.bmp .jpeg、または .png形式です。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

