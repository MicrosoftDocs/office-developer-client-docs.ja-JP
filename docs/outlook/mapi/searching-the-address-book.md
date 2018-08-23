---
title: アドレス帳を検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6673e1d51a7c030a35a7c5c3cbc955341afba299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803856"
---
# <a name="searching-the-address-book"></a><span data-ttu-id="60e2a-103">アドレス帳を検索</span><span class="sxs-lookup"><span data-stu-id="60e2a-103">Searching the address book</span></span>

<span data-ttu-id="60e2a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="60e2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="60e2a-105">MAPI �ł́A�����@�\�� 2 �̃��x�����������A�h���X���̃v���o�C�_�[���L���ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-105">MAPI enables address book providers to implement two levels of search functionality:</span></span>
  
- <span data-ttu-id="60e2a-106">アドレス帳のエントリの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを使用して指定した名前に一致する基本的なレベルです。</span><span class="sxs-lookup"><span data-stu-id="60e2a-106">A basic level that matches a specified name with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of address book entries.</span></span> <span data-ttu-id="60e2a-107">このレベルでは、ユーザー、たとえば、北西で始まる名前の配布リストを表示またはブラウンは個々 のメッセージングのユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-107">This level allows users, for example, to view distribution lists with names beginning with Northwest or locate individual messaging users whose last name is Brown.</span></span>
    
- <span data-ttu-id="60e2a-p102">���x�� **PR_DISPLAY_NAME**�ȊO�̃v���p�e�B�Ɉ�v���܂��B���̃��x���ɂ́A���b�Z�[�W���O����Ƃ������O�̎�ނ����̃A�h���X�ƃ��[�U�[�̌����ƌ�����i�荞�ނȂǁA���[�U�[���ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-p102">An advanced level that matches on properties other than **PR_DISPLAY_NAME**. This level allows users, for example, to further narrow their searches and find messaging users named Brown with a particular address type.</span></span>
    
<span data-ttu-id="60e2a-110">アドレス帳プロバイダーでは、両方のレベルで、基本的なレベルでは、そのコンテナーのそれぞれの検索をサポートしたり、まったくサポートしないように選択することが、ためにしない標準機能として実装することを検索します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-110">Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature.</span></span> <span data-ttu-id="60e2a-111">特定のコンテナーが検索をサポートしているかどうかは、その[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドの呼び出しで検索条件を確立するためにしようとします。</span><span class="sxs-lookup"><span data-stu-id="60e2a-111">To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> <span data-ttu-id="60e2a-112">**SetSearchCriteria**では、MAPI_E_NO_SUPPORT が返された場合、コンテナーは、検索をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="60e2a-112">If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches.</span></span> 
  
<span data-ttu-id="60e2a-113">検索をサポートするコンテナー、 [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md)を呼び出すことによって確立された条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-113">In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md).</span></span> <span data-ttu-id="60e2a-114">コンテナーの内容のテーブルが表示される前に、ユーザーを検索条件を求められる点を要求することもできます。</span><span class="sxs-lookup"><span data-stu-id="60e2a-114">You can also request that the user be prompted for search criteria before a container's contents table is displayed.</span></span> <span data-ttu-id="60e2a-115">このオプションを選択するには、コンテナーの**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) のプロパティの AB_FIND_ON_OPEN フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-115">To choose this option, set the AB_FIND_ON_OPEN flag of the container's **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span> <span data-ttu-id="60e2a-116">抽出条件を入力すると後、は、制限として保存され、 **SetSearchCriteria**メソッドに渡されることが。</span><span class="sxs-lookup"><span data-stu-id="60e2a-116">After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method.</span></span> <span data-ttu-id="60e2a-117">設定 AB_FIND_ON_OPEN は、オンライン サービス、またはそのデータを低速リンクしているすべてのアドレス帳プロバイダーを使用する場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="60e2a-117">Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data.</span></span> 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a><span data-ttu-id="60e2a-118">�A�h���X���R���e�i�[�̊�{�I�Ȍ�������s����ɂ�</span><span class="sxs-lookup"><span data-stu-id="60e2a-118">To perform a basic search in an address book container</span></span>
  
1. <span data-ttu-id="60e2a-119">���̓�e�̃e�[�u����J�����߂̃R���e�i�[��[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)���\�b�h��Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-119">Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
2. <span data-ttu-id="60e2a-p105">�j�[�Y�ɍ������������@��I����܂��B[�I����ڂ͎��̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-p105">Choose a search technique that meets your needs. The choices include:</span></span>
    
   - <span data-ttu-id="60e2a-122">�\��̓���̍s���������[IMAPITable::FindRow](imapitable-findrow.md)�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-122">[IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table.</span></span> 
    
   - <span data-ttu-id="60e2a-123">�e�[�u���̍s�̏�����[IMAPITable::SortTable](imapitable-sorttable.md)�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-123">[IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table.</span></span> 
    
   - <span data-ttu-id="60e2a-124">�\�\`���r���[�𐧌�����[IMAPITable::Restrict](imapitable-restrict.md)�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-124">[IMAPITable::Restrict](imapitable-restrict.md) to limit the table view.</span></span> 
    
   - <span data-ttu-id="60e2a-125">プロパティのあいまいな名前を解決するため、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用して制限します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-125">Property restriction using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property for resolving ambiguous names.</span></span> <span data-ttu-id="60e2a-126">この制限を課すために**IMAPITable::Restrict**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-126">Call **IMAPITable::Restrict** to impose this restriction.</span></span> 
    
   - <span data-ttu-id="60e2a-127">�����܂��Ȗ��O��������̂ɂ�[IABContainer::ResolveNames](iabcontainer-resolvenames.md)�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-127">[IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names.</span></span> 
    
3. <span data-ttu-id="60e2a-p107">�K�p���ꂽ��������Ɉ�v���邷�ׂĂ̍s��擾����[IMAPITable::QueryRows](imapitable-queryrows.md)���₢���킹���������B **QueryRows**�ɂ́A1 �ȏ�̈�v����s��Ԃ����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="60e2a-p107">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows.</span></span> 
    
<span data-ttu-id="60e2a-130">**FindRow**、 **SortTable**、および**Restrict**メソッドは、クライアントまたはサービス プロバイダーによって作成できる任意のテーブルで利用可能なテーブルのメソッドです。</span><span class="sxs-lookup"><span data-stu-id="60e2a-130">The **FindRow**, **SortTable**, and **Restrict** methods are table methods that are available for any table that can be created, either by a client or a service provider.</span></span> <span data-ttu-id="60e2a-131">**PR\_ANR**プロパティの制限および**IABContainer::ResolveNames**メソッドは、アドレス帳プロバイダーに固有のものし、あいまいな名前を解決するために使用します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-131">The **PR\_ANR** property restriction and **IABContainer::ResolveNames** method are specific to address book providers and are used for resolving ambiguous names.</span></span> <span data-ttu-id="60e2a-132">あいまいな名前は、それらに関連付けられている**PR_ENTRYID**プロパティを持たない受信者リスト内のエントリです。</span><span class="sxs-lookup"><span data-stu-id="60e2a-132">Ambiguous names are entries in a recipient list that do not have a **PR_ENTRYID** property associated with them.</span></span> 
  
<span data-ttu-id="60e2a-133">**PR\_ANR**制限は、文字の文字列を単語に分割し、プレフィックス一致を使用してアドレス帳の情報を使用してこれらの単語と一致するアルゴリズムを起動します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-133">The **PR\_ANR** restriction invokes an algorithm that separates a character string into words and matches those words with information in the address book using prefix-matching.</span></span> <span data-ttu-id="60e2a-134">一致するのに使用される情報は、アドレス帳プロバイダーに依存します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-134">The information used for the matching depends on the address book provider.</span></span> <span data-ttu-id="60e2a-135">アドレス帳コンテナーの**PR_ANR**の制限をサポートするすべてのアドレス帳プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="60e2a-135">All address book providers are required to support the **PR_ANR** restriction for their address book containers.</span></span> <span data-ttu-id="60e2a-136">詳細については、[名前解決の実装](implementing-name-resolution.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60e2a-136">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="60e2a-137">**IABContainer::ResolveNames**は、 **PR_ANR**の制限がコンテナーの内容のテーブルを開くことを必要とせず、複数の名前で処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-137">**IABContainer::ResolveNames** performs **PR_ANR** restriction processing on multiple names without requiring the container's contents table to be open.</span></span> <span data-ttu-id="60e2a-138">呼び出すよりもはるかに高速にすることができます複数の名前を解決するのには**ResolveNames**を 1 回の呼び出し、 **PR\_ANR**複数回に制限します。</span><span class="sxs-lookup"><span data-stu-id="60e2a-138">Calling **ResolveNames** once to resolve multiple names can be much faster than invoking a **PR\_ANR** restriction multiple times.</span></span> <span data-ttu-id="60e2a-139">ただし、アドレス帳プロバイダーは、 **ResolveNames**をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="60e2a-139">However, address book providers are not required to support **ResolveNames**.</span></span>
  

