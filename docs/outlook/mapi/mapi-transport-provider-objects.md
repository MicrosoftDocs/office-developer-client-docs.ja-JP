---
title: MAPI トランスポート プロバイダー オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801476"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="d081d-103">MAPI トランスポート プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d081d-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="d081d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d081d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d081d-105">だけでなく、標準のプロバイダーとログオン オブジェクトがすべてのサービス プロバイダーによって実装される、トランスポート プロバイダーは、状態オブジェクトを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d081d-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="d081d-106">その他のサービス プロバイダーの種類、状態オブジェクトを実装することは、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="d081d-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="d081d-107">ただし、MAPI は、トランスポート プロバイダーの。</span><span class="sxs-lookup"><span data-stu-id="d081d-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="d081d-108">リモート サーバーからのメッセージ ヘッダーのダウンロードをサポートするトランスポート プロバイダーは、フォルダーと、テーブルにも実装します。</span><span class="sxs-lookup"><span data-stu-id="d081d-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="d081d-109">各トランスポート プロバイダーは、対応するインターフェイスを実装できるオブジェクトを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d081d-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="d081d-110">図では、MAPI またはクライアントは、オブジェクトのユーザーかどうかも示しています。</span><span class="sxs-lookup"><span data-stu-id="d081d-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="d081d-111">![トランスポート プロバイダーを実装するオブジェクト](media/amapi_66.gif "トランスポート プロバイダーを実装するオブジェクト")</span><span class="sxs-lookup"><span data-stu-id="d081d-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d081d-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="d081d-112">See also</span></span>

- [<span data-ttu-id="d081d-113">MAPI サービス プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d081d-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)
