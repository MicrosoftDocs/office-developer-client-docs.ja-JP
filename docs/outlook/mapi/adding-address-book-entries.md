---
title: アドレス帳のエントリを追加します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: adbfbb73ac0f5f1e1cba547fa7a91393891fdb1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799628"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="9d079-103">アドレス帳のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="9d079-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="9d079-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d079-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d079-105">コンテナー、 [IAddrBook::NewEntry](iaddrbook-newentry.md)のクライアントの呼び出し、またはプロバイダーに、メッセージングのユーザーまたは配布リストを追加するのには、 _lpEIDContainer_パラメーター内の移行先コンテナーのエントリの識別子を使用して[IMAPISupport::NewEntry](imapisupport-newentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9d079-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="9d079-106">MAPI は、次に、一時テーブルから 1 回限りのテンプレートを使用してエントリを作成するコンテナーの[IABContainer::CreateEntry](iabcontainer-createentry.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9d079-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="9d079-107">1 回限りのテンプレートは、特定の種類の新しい受信者を作成するクライアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="9d079-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="9d079-108">ほとんどのフィールドは、編集できます。</span><span class="sxs-lookup"><span data-stu-id="9d079-108">Most of the fields are editable.</span></span> <span data-ttu-id="9d079-109">_LpEntryID_パラメーターで指定されたテンプレートでは、いずれかのプロバイダーを提供する可能性がありますか、プロバイダーが外部のテンプレートをサポートしている場合、外部プロバイダーからのテンプレートがあります。</span><span class="sxs-lookup"><span data-stu-id="9d079-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="9d079-110">**CreateEntry**の外部のテンプレートからの受信者を作成できるプロバイダーの実装は、常にすることはできませんプロバイダーの実装よりも複雑です。</span><span class="sxs-lookup"><span data-stu-id="9d079-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="9d079-111">**IABContainer::CreateEntry を実装するには**</span><span class="sxs-lookup"><span data-stu-id="9d079-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="9d079-112">_LpEntryID_パラメーターで指定されたエントリの識別子の種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="9d079-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="9d079-113">場合はエントリの識別子では、メッセージングのユーザー、配布リスト、または、プロバイダーが所有する、アドレス帳コンテナーのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="9d079-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="9d079-114">作成し、適切なオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9d079-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="9d079-115">プロバイダーは、必要な場合、いくつかの初期プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9d079-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="9d079-116">これらのプロパティは、作成される受信者の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9d079-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="9d079-117">_LppMAPIPropEntry_パラメーターの内容でのオブジェクトの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9d079-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="9d079-118">場合はエントリの識別子は、外部プロバイダーのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="9d079-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="9d079-119">外部オブジェクトを開くには、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9d079-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="9d079-120">そのプロパティを取得するプロパティ タグ配列の NULL を渡すオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9d079-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="9d079-121">プロパティ タグを変更するすべてのプロパティの新しいオブジェクトには適用されませんし、転送してはいけません PR_NULL、 **GetProps**から返されるプロパティ値の配列を編集します。</span><span class="sxs-lookup"><span data-stu-id="9d079-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="9d079-122">新しいオブジェクトのエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="9d079-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="9d079-123">適切なオブジェクトを新規作成、いずれかのメッセージのユーザーまたは配布リストを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d079-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="9d079-124">既定のプロパティを設定することによって新しいオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9d079-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="9d079-125">外部のオブジェクトが**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートしているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9d079-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="9d079-126">外部オブジェクトは、 **PR_TEMPLATEID**をサポートする場合は、外部プロバイダーからのプロパティのオブジェクトのインターフェイスを取得し、 _lppMAPIPropEntry_パラメーターの内容を外部のプロパティを設定する[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出すオブジェクトの実装です。</span><span class="sxs-lookup"><span data-stu-id="9d079-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="9d079-127">外部オブジェクトが**PR_TEMPLATEID**をサポートしていない場合は、新しいオブジェクトのプロバイダーの実装に_lppMAPIPropEntry_パラメーターの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="9d079-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="9d079-128">外部オブジェクトから適切なプロパティを設定するのには_lppMAPIPropEntry_パラメーターが指すオブジェクトの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9d079-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    
