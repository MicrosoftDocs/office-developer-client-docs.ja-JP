---
title: ゲートウェイのマッピング責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422755"
---
# <a name="gateway-mapping-responsibilities"></a>ゲートウェイのマッピング責任

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 対応ゲートウェイが、ゲートウェイマップ可能なプロパティを含む特別なプロパティ セットの 1 つで名前付きプロパティを含むメッセージを受信すると、ゲートウェイは、すべてのプロパティを宛先メッセージング システムのプロトコルにマップする必要があります。 MAPI では、ゲートウェイが特別なプロパティ セット内のすべての名前付きプロパティを処理する方法をお勧めしますが、ゲートウェイは、電子メール アドレスとアドレスの種類の 2 つのみを処理する必要があります。 電子メール アドレスとアドレスの種類のプロパティはメッセージの送信に直接影響を与えるので、ゲートウェイがこれら 2 つのプロパティのマッピングをサポートする必要があります。 検索キーはユーザーのアドレスの種類とアドレスで構成されるので、可能な限り翻訳する必要があります。
  
エントリ識別子は頻繁に処理されません。 あるメッセージング システムから別のメッセージング システムで使用できるエントリ識別子へのエントリ識別子のマッピングを有効にするには、ゲートウェイが両方のシステムの形式を使用できる必要があります。 ほとんどのゲートウェイはエントリ識別子の形式を認識しないので、エントリ識別子の変換はまれです。
  
頻繁に変換されないマップ可能なプロパティの 1 つが表示名です。 ゲートウェイは、表示名を保存して送信する必要がありますが、必ずしも変換する必要はありません。 
  

