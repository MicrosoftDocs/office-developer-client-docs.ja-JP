---
title: トランスポート プロバイダーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 140fe97662f7a2ce68c18d8e0eb991d0819da6dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800163"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="f716f-103">トランスポート プロバイダーの処理</span><span class="sxs-lookup"><span data-stu-id="f716f-103">Handling a transport provider</span></span>
  
<span data-ttu-id="f716f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f716f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f716f-105">クライアントは、MAPI スプーラーとトランスポート プロバイダーによって提供される状態オブジェクトを介してトランスポート プロバイダーと通信します。</span><span class="sxs-lookup"><span data-stu-id="f716f-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="f716f-106">クライアントは、状態テーブルを取得するために[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出すことによって状態オブジェクトをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f716f-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="f716f-107">ステータス オブジェクトの実装、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースのプロバイダーを構成する、フラッシュの受信および送信メッセージのキュー、パスワードの設定、および状態の検証の方法があります。</span><span class="sxs-lookup"><span data-stu-id="f716f-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="f716f-108">ステータス オブジェクトの詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f716f-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="f716f-109">[要求時にメッセージを送受信する](sending-or-receiving-a-message-on-demand.md): オン ・ デマンドでメッセージを送受信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f716f-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="f716f-110">[トランスポート オーダを設定](setting-transport-order.md): トランスポートの順番を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f716f-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="f716f-111">[トランスポート プロバイダーを再設定](reconfiguring-a-transport-provider.md): トランスポート プロバイダーを再設定する方法とはどのようなプロパティを設定するのには使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f716f-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    
