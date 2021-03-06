---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436434"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数のアドレス帳プロファイルで **2** つのアドレス帳エントリのEXCHANGEします。 この関数は [、IAddrBook::CompareEntryIDs の置換関数です](iaddrbook-compareentryids.md)。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>パラメーター

 _pmsess_
  
> [in]ログオンしている **IMAPISession**。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> [in]この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを含む Exchange サービスを識別する **emsmdbUID** へのポインター。 受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出し[は IAddrBook::D etails](iaddrbook-details.md)のように動作します。 このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。
    
 _pAddrBook_
  
> [in]エントリ識別子を開くのに使用するアドレス帳。 NULL にすることはできません。
    
 _cbEntryID1_
  
> [in]  _lpEntryID1_ パラメーターで指定された最初のエントリ識別子のバイト 数。 
    
 _lpEntryID1_
  
> [in]比較するアドレス帳エントリを表す最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> [in]  _lpEntryID2_ パラメーターで指定された 2 番目のエントリ識別子のバイト 数。 
    
 _lpEntryID2_
  
> [in]比較するアドレス帳エントリを表す比較で使用される 2 番目のエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果を含む場所へのポインター。 
    

