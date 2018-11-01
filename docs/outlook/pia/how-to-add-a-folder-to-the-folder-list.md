---
title: フォルダー一覧にフォルダーを追加する
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dc8ead207261cfd4835e230981d923211771de7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405526"
---
# <a name="add-a-folder-to-the-folder-list"></a><span data-ttu-id="cccbe-102">フォルダー一覧にフォルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="cccbe-102">Add a folder to the folder list</span></span>

<span data-ttu-id="cccbe-103">この例では、[Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) メソッドを使用して、フォルダーを Outlook のフォルダー一覧に追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cccbe-103">This example shows how to use the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>

## <a name="example"></a><span data-ttu-id="cccbe-104">例</span><span class="sxs-lookup"><span data-stu-id="cccbe-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="cccbe-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="cccbe-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="cccbe-106">次のコード例の **AddMyNewFolder** は、[Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) コレクションの **Add** メソッドを呼び出して、フォルダー "My New Folder" を表す [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトを Outlook のフォルダー一覧の **[受信トレイ]** に追加します。</span><span class="sxs-lookup"><span data-stu-id="cccbe-106">In the following code example,  \*\*\*\* calls the **Add** method of the [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) collection to add a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that represents a folder called "My New Folder" to the **Inbox** in the Outlook folder list.</span></span> <span data-ttu-id="cccbe-107">"My New Folder" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cccbe-107">"My New Folder" is then displayed.</span></span>

<span data-ttu-id="cccbe-108">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cccbe-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="cccbe-109">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cccbe-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="cccbe-110">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cccbe-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="cccbe-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="cccbe-111">See also</span></span>

- [<span data-ttu-id="cccbe-112">フォルダー</span><span class="sxs-lookup"><span data-stu-id="cccbe-112">Folders</span></span>](folders.md)
