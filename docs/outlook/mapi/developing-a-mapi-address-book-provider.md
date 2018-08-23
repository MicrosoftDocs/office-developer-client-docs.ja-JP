---
title: MAPI アドレス帳プロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799908"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="45607-103">MAPI アドレス帳プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="45607-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="45607-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45607-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45607-105">アドレス帳プロバイダーは、メッセージ ストアと、トランスポート プロバイダーは、クライアント アプリケーションと MAPI 受信者の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="45607-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="45607-106">受信者の情報は、コンテナーと呼ばれるストレージ ・ コンパートメントに階層的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="45607-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="45607-107">プロファイル内のすべてのアドレス帳は、1 つを提供またはより上位、またはセッション内の親コンテナーが MAPI アドレス帳にあるすべてのアドレスから宛先の情報を統合的に表示するブック プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="45607-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="45607-108">クライアントおよびその他のサービス プロバイダーにアクセスするアドレス帳プロバイダーのデータは、MAPI アドレス帳から。</span><span class="sxs-lookup"><span data-stu-id="45607-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="45607-109">MAPI によって統合されたアドレス帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="45607-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="45607-110">各アドレス帳プロバイダーから最上位のコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="45607-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="45607-111">各コンテナーの階層テーブルを取得しています。</span><span class="sxs-lookup"><span data-stu-id="45607-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="45607-112">統合された階層のテーブルに各階層テーブルをコピーしています。</span><span class="sxs-lookup"><span data-stu-id="45607-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="45607-113">クライアントに公開されている統合された階層テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="45607-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="45607-114">MAPI には、アドレス帳プロバイダーの作成者のほとんどの要件が課されません。</span><span class="sxs-lookup"><span data-stu-id="45607-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="45607-115">可能な機能の範囲をアドレス帳のライターとは、多様で柔軟なようで実装できます。</span><span class="sxs-lookup"><span data-stu-id="45607-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="45607-116">プロバイダーでした特定の種類の受信者情報の読み取り専用のビューを指定することに限定するなど、クライアントやプロバイダーは、追加または受信者のデータを変更して適用を受け入れること、機能の完全なセットを実装カスタマイズしたビューを定義するための条件を検索します。</span><span class="sxs-lookup"><span data-stu-id="45607-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="45607-117">プロバイダーのデータは、ファイルまたはデータベースまたはリモート サーバー上でローカルに配置できます。</span><span class="sxs-lookup"><span data-stu-id="45607-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="45607-118">いくつかのアドレス帳プロバイダーは、すべてのメッセージング システムと連携して、他のユーザー中に、トランスポート プロバイダーと密接に関連の特定のメッセージング システムで動作するものです。</span><span class="sxs-lookup"><span data-stu-id="45607-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="45607-119">MAPI では、個人用アドレス帳、または 1 つの変更可能なコンテナーを実装し、受信者の情報を他のコンテナーと同様に直接作成された情報のコピーを保持することができますが、個人用アドレス帳アドレス帳プロバイダーの特殊な型を定義します。</span><span class="sxs-lookup"><span data-stu-id="45607-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="45607-120">任意のアドレス帳プロバイダーは、個人用アドレス帳を実装でき、プロファイルに複数の Pab を追加することができますが、1 つのセッション中に、個人用アドレス帳として動作するこれらのプロバイダーの 1 つだけを指定できます。</span><span class="sxs-lookup"><span data-stu-id="45607-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

