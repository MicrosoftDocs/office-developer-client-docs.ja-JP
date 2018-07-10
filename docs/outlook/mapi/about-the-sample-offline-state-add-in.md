---
title: アドインの状態をオフラインのサンプルについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a6bdf408-114a-2203-189f-101251a65a8c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9a4dbe6757ae7ce5eccee3c3a366660db412cfe6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799615"
---
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="3eea0-103">アドインの状態をオフラインのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="3eea0-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="3eea0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3eea0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3eea0-105">オフライン状態の API には、Outlook のユーザーの接続の状態が変更されたことを示すコールバックがサポートされています-などのオフライン中に Outlook でオンラインにしているからです。</span><span class="sxs-lookup"><span data-stu-id="3eea0-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="3eea0-106">オフライン状態のサンプル アドインは、COM アドインの接続状態の変更の通知を受信する方法と、オフライン状態 API を使用して現在の状態を変更する方法を説明する C++ で書かれました。</span><span class="sxs-lookup"><span data-stu-id="3eea0-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="3eea0-107">オフライン状態 API の詳細については、[の「オフライン状態 API](about-the-offline-state-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3eea0-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="3eea0-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="3eea0-108">In this section</span></span>

- [<span data-ttu-id="3eea0-109">サンプル オフライン状態のアドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="3eea0-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="3eea0-110">ダウンロードして、オフライン状態のサンプル アドインをインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="3eea0-111">オフライン状態のアドインを設定します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="3eea0-112">オフライン状態のアドインを使用するために接続、初期化、およびセットアップ機能を実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="3eea0-113">接続状態の監視は、アドインを使用して、オフライン状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="3eea0-114">監視し、接続状態を変更するオフラインのオブジェクトを取得する**[HrOpenOfflineObj](hropenofflineobj.md)** 関数を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="3eea0-115">オフライン状態の追加の接続を切断します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="3eea0-116">正しく終了し、アドインが切断されたときに、オフライン状態アドインをクリーンアップする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3eea0-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3eea0-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="3eea0-117">See also</span></span>



[<span data-ttu-id="3eea0-118">オフラインの状態の API について</span><span class="sxs-lookup"><span data-stu-id="3eea0-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
