---
title: スパム対策の設定について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook では、迷惑メールからアカウントを保護するために各アカウントの設定を指定することができます。 このような迷惑メール対策設定は、ユーザーのプロファイルで、そのアカウント用に指定されたセクションに格納されます。
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799287"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="a09a9-104">スパム対策の設定について</span><span class="sxs-lookup"><span data-stu-id="a09a9-104">About anti-spam settings</span></span>

<span data-ttu-id="a09a9-105">Outlook では、迷惑メールからアカウントを保護するために各アカウントの設定を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="a09a9-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="a09a9-106">このような迷惑メール対策設定は、ユーザーのプロファイルで、そのアカウント用に指定されたセクションに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a09a9-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="a09a9-107">[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)プロパティを使用すると、スパム対策の設定を含む、このアカウントのユーザーの環境設定が格納されているプロファイルのセクションの固有 ID (UID) を取得します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="a09a9-108">アカウントのスパム対策の設定を取得するのにには、次のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="a09a9-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)-アカウントの禁止された送信者としてユーザーが指定した電子メール アドレスとドメインのセミコロン区切りのリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="a09a9-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)-アカウントのユーザーが指定するスパムのフィルタ リングのレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="a09a9-111">次の表は、サポートされている値を示します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="a09a9-112">サポートされている値</span><span class="sxs-lookup"><span data-stu-id="a09a9-112">Supported value</span></span> |<span data-ttu-id="a09a9-113">Definition</span><span class="sxs-lookup"><span data-stu-id="a09a9-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="a09a9-114">なし</span><span class="sxs-lookup"><span data-stu-id="a09a9-114">None</span></span>  <br/> |<span data-ttu-id="a09a9-115">0 xffffffff</span><span class="sxs-lookup"><span data-stu-id="a09a9-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="a09a9-116">低</span><span class="sxs-lookup"><span data-stu-id="a09a9-116">Low</span></span>  <br/> |<span data-ttu-id="a09a9-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="a09a9-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="a09a9-118">中</span><span class="sxs-lookup"><span data-stu-id="a09a9-118">Medium</span></span>  <br/> |<span data-ttu-id="a09a9-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="a09a9-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="a09a9-120">高</span><span class="sxs-lookup"><span data-stu-id="a09a9-120">High</span></span>  <br/> |<span data-ttu-id="a09a9-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a09a9-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="a09a9-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)-ユーザー アカウントの信頼された受信者として指定する電子メール アドレスとドメインのセミコロン区切りのリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="a09a9-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)-アカウントの信頼された送信者としてユーザーが指定した電子メール アドレスとドメインのセミコロン区切りのリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a09a9-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a09a9-124">See also</span></span>

- [<span data-ttu-id="a09a9-125">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="a09a9-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="a09a9-126">迷惑メール フィルター リストに名前を追加します。</span><span class="sxs-lookup"><span data-stu-id="a09a9-126">Add names to the Junk Email Filter lists</span></span>](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)
