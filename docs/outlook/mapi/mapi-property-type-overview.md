---
title: MAPI プロパティの型の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ce3cd37247f37c4e70adb07769f00b2df07307a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801428"
---
# <a name="mapi-property-type-overview"></a><span data-ttu-id="6908d-103">MAPI プロパティの型の概要</span><span class="sxs-lookup"><span data-stu-id="6908d-103">MAPI property type overview</span></span>
  
<span data-ttu-id="6908d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6908d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6908d-105">プロパティの型は、MAPIDEFS では、MAPI によって定義されている定数です。H ヘッダー ファイルのプロパティ値の基になるデータ型を示す。</span><span class="sxs-lookup"><span data-stu-id="6908d-105">Property types are constants defined by MAPI in the MAPIDEFS.H header file that indicate the underlying data type of a property value.</span></span> <span data-ttu-id="6908d-106">すべてのプロパティは、MAPI、クライアント アプリケーション、またはサービス ・ プロバイダーに定義されているかどうかを使用して、これらの種類のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="6908d-106">All properties, whether they are defined by MAPI, by client applications, or by service providers, use one of these types.</span></span> 
  
<span data-ttu-id="6908d-107">プロパティの型は、次のような名前付け規則のプロパティ タグを使用に設定します。</span><span class="sxs-lookup"><span data-stu-id="6908d-107">Property types follow a similar naming convention to the one used for property tags.</span></span> <span data-ttu-id="6908d-108">多くのプロパティの種類には、単一値と複数値の両方のバージョンがインストールされています。</span><span class="sxs-lookup"><span data-stu-id="6908d-108">Many property types have both a single-value and multiple-value version.</span></span> <span data-ttu-id="6908d-109">1 つの値を持つプロパティには、1 つの整数や文字列などの型の 1 つの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6908d-109">Single valued properties contain one value of its type such as a single integer or character string.</span></span> <span data-ttu-id="6908d-110">単一値のプロパティを表すために使用する定数には、2 つの部分: プレフィックス PT_ と時間の長い、STRING8 など、実際の型を記述する文字列。</span><span class="sxs-lookup"><span data-stu-id="6908d-110">The constant used to represent a single value property has two parts: the prefix PT_ and a string describing the actual type, such as LONG or STRING8.</span></span> 
  
<span data-ttu-id="6908d-111">複数値プロパティには、その型の 1 つ以上の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6908d-111">Multiple-value properties contain more than one value of its type.</span></span> <span data-ttu-id="6908d-112">OLE バリアント型の配列とは異なりは、同じ種類の複数値を持つプロパティに含まれる値です。</span><span class="sxs-lookup"><span data-stu-id="6908d-112">Unlike OLE variant arrays, every value in a multivalued property is of the same type.</span></span> <span data-ttu-id="6908d-113">複数値を持つプロパティを表すために使用する定数は、対応する 1 つの値を表す定数基本型と、MV_FLAG フラグを組み合わせることによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="6908d-113">The constant used to represent multivalued properties is created by combining the MV_FLAG flag with the corresponding single value constant representing the base type.</span></span> <span data-ttu-id="6908d-114">次の 3 つの部分があります: MV_ の後に PT_ というプレフィックスの後に型を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6908d-114">There are three parts: the prefix PT_ followed by MV_ followed by a string that describes the type.</span></span> <span data-ttu-id="6908d-115">たとえば、複数の整数を格納しているプロパティの型は、PT_MV_LONG、PT_MV_STRING8 は、複数の文字列をします。</span><span class="sxs-lookup"><span data-stu-id="6908d-115">For example, the type for a property containing multiple integers is PT_MV_LONG and for multiple character strings is PT_MV_STRING8.</span></span>
  
<span data-ttu-id="6908d-116">次の図は、複数値の整数では、PT_MV_LONG の種類のプロパティを記述する[SPropValue](spropvalue.md)構造体の構造を示します。</span><span class="sxs-lookup"><span data-stu-id="6908d-116">The following illustration shows the structure of an [SPropValue](spropvalue.md) structure to describe a multiple-value integer, a property of type PT_MV_LONG.</span></span> <span data-ttu-id="6908d-117">**値**のメンバーは、プロパティとそれらの値の配列へのポインターに整数値の数のカウントを含むように拡張されます。</span><span class="sxs-lookup"><span data-stu-id="6908d-117">The **Value** member is expanded to include a count of the number of integer values in the property and a pointer to an array of those values.</span></span> 
  
<span data-ttu-id="6908d-118">**複数値のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="6908d-118">**Multiple-value properties**</span></span>
  
<span data-ttu-id="6908d-119">![複数値のプロパティ](media/amapi_12.gif "複数値のプロパティ")</span><span class="sxs-lookup"><span data-stu-id="6908d-119">![Multiple-value properties](media/amapi_12.gif "Multiple-value properties")</span></span>
  
<span data-ttu-id="6908d-120">複数値をサポートするプロパティは省略可能、MAPI は、クライアントとサービス ・ プロバイダーをサポートして両方の種類のプロパティのため、有効に MAPI 準拠のコンポーネント間の対話をよりことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6908d-120">Although support for multiple-value properties is optional, MAPI recommends that clients and service providers support both types of properties because doing so enables greater interaction between MAPI-compliant components.</span></span>
  
<span data-ttu-id="6908d-121">次の図では、すべて**SPropValue**構造体に格納されている場所を示すさまざまなプロパティ型の定数の一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="6908d-121">The following illustration lists all of the different property type constants, showing where they are stored in an **SPropValue** structure.</span></span> <span data-ttu-id="6908d-122">**値**のメンバーのサイズは、特定のタイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6908d-122">The size of the **Value** member is dependent on the particular type.</span></span> <span data-ttu-id="6908d-123">対応する複数値があるすべての単一値の型に注意してください。</span><span class="sxs-lookup"><span data-stu-id="6908d-123">Notice that not all of the single-value types have multiple-value equivalents.</span></span> 
  
<span data-ttu-id="6908d-124">**プロパティの型の定数**</span><span class="sxs-lookup"><span data-stu-id="6908d-124">**Property type constants**</span></span>
  
<span data-ttu-id="6908d-125">![プロパティの型の定数](media/amapi_11.gif "プロパティの型の定数")</span><span class="sxs-lookup"><span data-stu-id="6908d-125">![Property type constants](media/amapi_11.gif "Property type constants")</span></span>
  
<span data-ttu-id="6908d-126">クライアントとサービス プロバイダーのプロパティは、2 つの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="6908d-126">Clients and service providers working with a property need to follow two steps:</span></span>
  
1. <span data-ttu-id="6908d-127">プロパティが使用可能または使用できないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6908d-127">Determine if the property is available or unavailable.</span></span>
    
2. <span data-ttu-id="6908d-128">可能な場合、プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6908d-128">If available, retrieve the property's value.</span></span>
    
<span data-ttu-id="6908d-129">クライアントまたはサービス プロバイダーが必要なプロパティの存在をチェックだけ場合があります。それ以外の場合は、特定の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6908d-129">Sometimes a client or service provider need only check for the existence of a property; other times it is necessary to check for a specific value.</span></span> <span data-ttu-id="6908d-130">たとえば、トランスポート プロバイダーが処理のためのアクションの 3 つの異なるコースをある、 **PR\_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティ、メッセージで送信されるかどうかを示すブール値書式設定されたテキストです。</span><span class="sxs-lookup"><span data-stu-id="6908d-130">For example, transport providers have three different courses of action for processing the **PR\_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property, a Boolean value that indicates whether or not a message should be transmitted with formatted text.</span></span> <span data-ttu-id="6908d-131">場合**PR\_SEND_RICH_INFO**は、トランスポート プロバイダーは、TRUE に設定すると、書式設定されたテキストを送信します。</span><span class="sxs-lookup"><span data-stu-id="6908d-131">If **PR\_SEND_RICH_INFO** is set to TRUE, the transport provider transmits the formatted text.</span></span> <span data-ttu-id="6908d-132">FALSE に設定されている場合は、伝送する前に書式設定されたテキストが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="6908d-132">If it is set to FALSE, the formatted text is discarded before transmission.</span></span> <span data-ttu-id="6908d-133">**PR_SEND_RICH_INFO**では、トランスポート プロバイダーは、次のようにアクションのどのような場合は、その既定コースは特定のプロバイダーにします。</span><span class="sxs-lookup"><span data-stu-id="6908d-133">If **PR_SEND_RICH_INFO** is unavailable, the transport provider follows its default course of action, whatever that is for the particular provider.</span></span> 
  
<span data-ttu-id="6908d-134">MAPI は、PT_UNSPECIFIED は、クライアントまたはサービス プロバイダーは、プロパティの型が不明の場合は、プロパティを取得するために使用できる特殊なプロパティ型を定義します。型の事前知識がないプロパティを取得するには、クライアントまたはサービス プロバイダーはオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すし、プロパティ タグのプロパティの識別子と、PT_UNSPECIFIED プロパティのデータ型を渡します。</span><span class="sxs-lookup"><span data-stu-id="6908d-134">MAPI defines a special property type, PT_UNSPECIFIED, that a client or service provider can use to retrieve a property when the property type is unknown.To retrieve a property without advance knowledge of its type, a client or service provider calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method and passes a property tag made up of the property's identifier and the PT_UNSPECIFIED property type.</span></span> <span data-ttu-id="6908d-135">**GetProps**に、PT_UNSPECIFIED を適切な型に置き換えてプロパティの[SPropValue](spropvalue.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="6908d-135">**GetProps** returns an [SPropValue](spropvalue.md) structure for the property, replacing PT_UNSPECIFIED with the appropriate type.</span></span> <span data-ttu-id="6908d-136">**GetProps**を実装するサービス プロバイダーは、PT_UNSPECIFIED をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6908d-136">Service providers implementing **GetProps** are required to support PT_UNSPECIFIED.</span></span> 
  
<span data-ttu-id="6908d-137">MAPI オブジェクトのいくつかは、オブジェクトを自体はプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6908d-137">Some MAPI objects support properties that are themselves objects.</span></span> <span data-ttu-id="6908d-138">PT_OBJECT 型は、オブジェクトのプロパティであります。</span><span class="sxs-lookup"><span data-stu-id="6908d-138">Object properties have the type PT_OBJECT.</span></span> <span data-ttu-id="6908d-139">通常これらのプロパティ、クライアント、サービス プロバイダーにアクセスするのには**IMAPIProp::GetProps**を使用する代わりにユーザーのいずれかの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッド、オブジェクトのアクセス、またはメソッドの適切なインターフェイスを指定します。プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6908d-139">Instead of using **IMAPIProp::GetProps** to access these properties, clients and service providers typically user either the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying the appropriate interface for access, or a method on the object supporting the property.</span></span> 
  
<span data-ttu-id="6908d-140">オブジェクトのプロパティの値にアクセスするため、オブジェクトの使用するインタ フェースのいずれかの**GetProps**が適切ではありませんが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6908d-140">Because accessing the value of an object property involves using one of the interfaces for the object, **GetProps** is inappropriate.</span></span> <span data-ttu-id="6908d-141">**GetProps**、呼び出し元がプロパティの値をアクセス**SPropValue**構造体を使用。</span><span class="sxs-lookup"><span data-stu-id="6908d-141">With **GetProps**, the caller accesses a property's value through an **SPropValue** structure.</span></span> <span data-ttu-id="6908d-142">**IMAPIProp::OpenProperty**では、呼び出し元は、オブジェクトにアクセスできるインターフェイスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="6908d-142">With **IMAPIProp::OpenProperty**, the caller retrieves a pointer to an interface that can access the object.</span></span> <span data-ttu-id="6908d-143">**OpenProperty**は、オブジェクトのプロパティを取得するために常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6908d-143">**OpenProperty** can always be used to retrieve an object property.</span></span> <span data-ttu-id="6908d-144">すべてのオブジェクト プロパティを使用して、オブジェクトのメソッドを呼び出して、他のオプションが得られません。</span><span class="sxs-lookup"><span data-stu-id="6908d-144">The other option, calling a method on the object, is not available with every object property.</span></span> 
  
<span data-ttu-id="6908d-145">たとえば、すべてのフォルダーには、2 つのテーブル、階層テーブルおよび内容のテーブルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6908d-145">For example, every folder supports two tables, a hierarchy table and a contents table.</span></span> <span data-ttu-id="6908d-146">これらのテーブルには、フォルダーのプロパティプロパティ タグは、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) および**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="6908d-146">These tables are properties of the folder; their property tags are **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) and **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span></span> <span data-ttu-id="6908d-147">テーブルは、アクセスの**IMAPITable**インターフェイスを必要とするオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="6908d-147">Tables are objects that require the **IMAPITable** interface for access.</span></span> <span data-ttu-id="6908d-148">クライアントは、階層テーブルの内容のテーブル、またはフォルダーの[IMAPIProp::OpenProperty にアクセスするためのフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドにアクセスするためのフォルダーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出すことができます。](imapiprop-openproperty.md)いずれかのテーブルにアクセスするメソッドです。</span><span class="sxs-lookup"><span data-stu-id="6908d-148">A client can call the folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table, the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table, or the folder's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to access either table.</span></span> <span data-ttu-id="6908d-149">**OpenProperty**を呼び出すには、クライアントは、最初のパラメーターと 2 番目のパラメーターとしてのアクセスに使用するインターフェイスのインターフェイス識別子とプロパティのプロパティ タグを渡します。</span><span class="sxs-lookup"><span data-stu-id="6908d-149">To call **OpenProperty**, a client passes the property tag for the property as the first parameter and an interface identifier for the interface to be used for access as the second parameter.</span></span> <span data-ttu-id="6908d-150">これらのパラメーターは、 **PR_CONTAINER_HIERARCHY**または**PR_CONTAINER_CONTENTS**と**IID_IMAPITable**になります。</span><span class="sxs-lookup"><span data-stu-id="6908d-150">These parameters would be **PR_CONTAINER_HIERARCHY** or **PR_CONTAINER_CONTENTS** and **IID_IMAPITable**.</span></span>
  
<span data-ttu-id="6908d-151">単一値および複数値プロパティの型の完全なリストは、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6908d-151">For a complete list of the single-value and multiple-value property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6908d-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="6908d-152">See also</span></span>

- [<span data-ttu-id="6908d-153">MAPI Property Overview</span><span class="sxs-lookup"><span data-stu-id="6908d-153">MAPI Property Overview</span></span>](mapi-property-overview.md)
