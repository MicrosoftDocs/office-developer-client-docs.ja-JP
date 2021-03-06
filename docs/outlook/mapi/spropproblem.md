---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407775"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティに関連する操作に関連するエラーについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Members

 **ulIndex**
  
> プロパティ タグの配列内のインデックス。
    
 **ulPropTag**
  
> エラーが発生したプロパティのプロパティ タグ。
    
 **scode**
  
> プロパティの問題を説明するエラー値。 この値には、任意の MAPI [SCODE 値を指定](scode.md) できます。 
    
## <a name="remarks"></a>注釈

**SPropProblem** 構造体の配列は、次のメソッドから返されます。 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
**SPropProblem** 構造体には、MAPI プロパティを変更または削除しようとする操作によって発生する **SCODE** エラー値が含まれる。 
  
**SPropProblem** 構造体がプロパティに関連するエラーでどのように動作する方法の詳細については、「MAPI 名前付きプロパティ」[を参照してください](mapi-named-properties.md)。 
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[MAPI の構造](mapi-structures.md)

