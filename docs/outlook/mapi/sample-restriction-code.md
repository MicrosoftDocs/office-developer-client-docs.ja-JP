---
title: 制限のサンプル コード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b82097c-dbd6-4ba0-a6cb-292301f9402b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cafcb20cbce3019d7623d330721005a674eca36e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411016"
---
# <a name="sample-restriction-code"></a><span data-ttu-id="d1e0f-103">制限のサンプル コード</span><span class="sxs-lookup"><span data-stu-id="d1e0f-103">Sample restriction code</span></span>

<span data-ttu-id="d1e0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1e0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1e0f-105">次のサンプル コードは、件名に "バレー" という単語が含まれるのではなく、Sam から Sue に送信されていないすべてのメッセージをフィルター処理する制限を作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d1e0f-105">The following sample code shows how to create a restriction that filters out all messages that do not contain the word "volleyball" in the subject line and were not sent to Sue from Sam.</span></span> <span data-ttu-id="d1e0f-106">[SRestriction](srestriction.md)構造体のツリーが必要で、上部ノードは [SAndRestriction](sandrestriction.md)構造で実装された **AND** 制限です。</span><span class="sxs-lookup"><span data-stu-id="d1e0f-106">A tree of [SRestriction](srestriction.md) structures is required, with the top node being an **AND** restriction implemented with an [SAndRestriction](sandrestriction.md) structure.</span></span> <span data-ttu-id="d1e0f-107">**AND** 操作によって結合される 3 つの制限は、Sue に送信されるメッセージを検索するサブオブジェクト制限、Sam からのメッセージを検索するコンテンツ制限、および "バレーボール" を含む件名を持つメッセージを検索する別の **AND** 制限です。</span><span class="sxs-lookup"><span data-stu-id="d1e0f-107">The three restrictions that are joined by the **AND** operation are a subobject restriction that searches for messages sent to Sue, a content restriction that searches for messages from Sam, and another **AND** restriction that searches for messages that have a subject containing "volleyball."</span></span> <span data-ttu-id="d1e0f-108">この **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) は必須のプロパティではないので **、Exist** 制限を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1e0f-108">Because **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) is not a required property, an **Exist** restriction must be included.</span></span> 
  
<span data-ttu-id="d1e0f-109">このコードでは、動的割り当てと初期化を使用します。静的に割り当て、初期化することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1e0f-109">This code uses dynamic allocation and initialization; it is possible to allocate and initialize statically as well.</span></span> <span data-ttu-id="d1e0f-110">簡単に説明するために、割り当て呼び出し後に発生する必要があるエラー チェックは、サンプルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="d1e0f-110">In the interest of brevity, the error checking that must occur following the allocation calls is not included in the sample.</span></span> 
  
```cpp
HRESULT BuildRestriction (LPSTR pszSent, LPSTR pszFrom,
                                LPSTR pszSubjectText);
{
    LPSRestriction pRest, pAndRes, pObjRes, pSubjAndRes;
    LPSPropValue pRecip, pSender, pSubject;
    HRESULT hResult;
    ULONG ulResCount = 3, ulSubjCount = 2
    // Allocate and build  restriction to join criteria
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulResCount, pRest,
            (LPVOID *)&pAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Allocate and build subobject restriction to search recipient list
    hResult = MAPIAllocateMore (sizeof(SRestriction), pRest,
            (LPVOID *)&pObjRes);
    pAndRes[0].rt = RES_SUBRESTRICTION;
    pAndRes[0].res.resSub.ulSubObject = PR_MESSAGE_RECIPIENTS;
    pAndRes[0].res.resSub.lpRes = pObjRes;
    // Allocate and build content restriction to look for recipient
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pRecip);
    pObjRes->rt = RES_CONTENT;
    pObjRes->res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pObjRes->res.resContent.ulPropTag = pRecip->ulPropTag =
            PR_DISPLAY_NAME;
    pObjRes->res.resContent.lpProp = pRecip;
    pRecip->Value.LPSZ = pszSent;              // pszSent set to Sue
    // Allocate and build content restriction to look for sender
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSend);
    pAndRes[1].rt = RES_CONTENT;
    pAndRes[1].res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pAndRes[1].res.resContent.ulPropTag = pSend->ulPropTag =
            PR_SENDER_NAME;
    pAndRes[1].res.resContent.lpProp = pSend;
    pSend->Value.LPSZ = pszName;                    // pszName set to Sam
    // Allocate and build  restriction to look for subject
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulSubjCount, pRest,
            (LPVOID *)&pSubjAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Create an  restriction to search for subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubjAndRes);
    pAndRes[2].rt = RES_AND;
    pAndRes[2].res.resAnd.cRes = ulSubjCount;
    pAndRes[2].res.resAnd.lpRes = pSubjAndRes;
    // Exist restriction to check that PR_SUBJECT exists
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[0].rt = RES_EXIST;
    pSubjAndRes[0].res.resExist.ulReserved1 = 0;
    pSubjAndRes[0].res.resExist.ulReserved2 = 0;
    pSubjAndRes[0].res.resExist.ulPropTag = PR_SUBJECT;
    // Content restriction to check for "volleyball" in subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[1].res.resContent.ulFuzzyLevel =
            FL_SUBSTRING | FL_IGNORECASE;
    pSubjAndRes[1].res.resContent.ulPropTag = pSubj->ulPropTag =
            PR_SUBJECT;
    pSubjAndRes[1].res.resContent.lpProp = pSubj;
    pSubj->Value.LPSZ = pszSubjectText;
    return hResult;
}
 
```

## <a name="see-also"></a><span data-ttu-id="d1e0f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1e0f-111">See also</span></span>

- [<span data-ttu-id="d1e0f-112">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="d1e0f-112">MAPI Tables</span></span>](mapi-tables.md)

