---
title: カスタムの連絡先アイテムを作成する
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 189be01e6e690ad1db3d58d58837ab418b4c2e74
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407346"
---
# <a name="create-a-custom-contact-item"></a><span data-ttu-id="35b44-102">カスタムの連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="35b44-102">Create a custom Contact item</span></span>

<span data-ttu-id="35b44-103">この例では、カスタムの連絡先アイテムを作成し、定義済みのプロパティとユーザー定義プロパティの両方を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="35b44-103">This example shows how to create a custom contact item and set both predefined and user-defined properties.</span></span>

## <a name="example"></a><span data-ttu-id="35b44-104">例</span><span class="sxs-lookup"><span data-stu-id="35b44-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="35b44-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="35b44-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="35b44-106">[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) オブジェクトは連絡先フォルダー内の連絡先を表します。また、[FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) や [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)) など、100 個以上の組み込みプロパティを持っています。</span><span class="sxs-lookup"><span data-stu-id="35b44-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object represents a contact in the Contacts folder, and has more than 100 built-in properties such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) and [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)) . Sometimes, the built-in properties are not sufficient and you need to add custom properties, which you can do by using the UserProperties collection.</span></span> <span data-ttu-id="35b44-107">これらの組み込みプロパティでは不十分な場合もあります。その場合はカスタム プロパティを追加する必要があります。カスタム プロパティは、[UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) コレクションを使用すると追加できます。</span><span class="sxs-lookup"><span data-stu-id="35b44-107">A ContactItem object represents a contact in the Contacts folder, and has more than 100 built-in properties such as FirstName and LastName . Sometimes, the built-in properties are not sufficient and you need to add custom properties, which you can do by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span>

<span data-ttu-id="35b44-108">次のコード例では、CreateCustomItem でカスタム **ContactItem** オブジェクトを作成し、"Shoe Store" という名前を付け、[Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) メソッドを呼び出して、"Shoe Store" という名前のフォルダーに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b44-108">In the following code example,   creates a custom ContactItem object, names it "Shoe Store", and calls the Add(String, Object) method to add it to a folder named "Shoe Store".</span></span> <span data-ttu-id="35b44-109">まず CreateCustomItem は、[GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) メソッドを使用して "Shoe Store" フォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="35b44-109"> first gets the "Shoe Store" folder by using the GetDefaultFolder(OlDefaultFolders) method.</span></span> <span data-ttu-id="35b44-110">"Shoe Store" フォルダーは既定の連絡先フォルダーのサブフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="35b44-110">The "Shoe Store" folder is a subfolder of the default Contacts folder.</span></span> <span data-ttu-id="35b44-111">次に、CreateCustomItem は **FirstName** プロパティと **LastName** プロパティを設定し、**UserProperties** コレクションを使用してユーザー定義プロパティ ("Shoe Size") を作成します。</span><span class="sxs-lookup"><span data-stu-id="35b44-111"> then sets the FirstName and LastName properties, and creates a user-defined property ("Shoe Size") by using the UserProperties collection.</span></span>

<span data-ttu-id="35b44-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="35b44-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="35b44-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35b44-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="35b44-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="35b44-114">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="35b44-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="35b44-115">See also</span></span>

- [<span data-ttu-id="35b44-116">連絡先</span><span class="sxs-lookup"><span data-stu-id="35b44-116">Contacts</span></span>](contacts.md)
