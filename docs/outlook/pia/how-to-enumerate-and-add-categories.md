---
title: 分類項目を列挙および追加する
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 27fc8630c8e2eb0b491dbb5075f4c58aacec7f93
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406247"
---
# <a name="enumerate-and-add-categories"></a><span data-ttu-id="68456-102">分類項目を列挙および追加する</span><span class="sxs-lookup"><span data-stu-id="68456-102">Enumerate and add categories</span></span>

<span data-ttu-id="68456-103">この例では、分類項目を列挙し、メイン分類項目リストに分類項目を追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="68456-103">This example shows how to enumerate categories and add a category to the main category list.</span></span>

## <a name="example"></a><span data-ttu-id="68456-104">例</span><span class="sxs-lookup"><span data-stu-id="68456-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="68456-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="68456-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="68456-p101">Outlook のオブジェクト モデルは、ユーザーの受信トレイのアイテムを整理しやすくするための分類項目をサポートしています。高レベルな整理を維持するために、以下を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="68456-p101">The Outlook object model supports categories that help organize items in a user’s Inbox. To maintain a higher level of organization, you can do the following:</span></span>

- <span data-ttu-id="68456-108">Outlook アイテムを分類し、分類項目ごとに表示します。</span><span class="sxs-lookup"><span data-stu-id="68456-108">Categorize Outlook items and display them by category.</span></span>
- <span data-ttu-id="68456-109">単一の Outlook アイテムに複数の色の分類項目を適用します。</span><span class="sxs-lookup"><span data-stu-id="68456-109">Apply multiple color categories to a single Outlook item.</span></span>
- <span data-ttu-id="68456-110">色の分類項目により Outlook アイテムのグループ化と並べ替えを行います。</span><span class="sxs-lookup"><span data-stu-id="68456-110">Group and sort Outlook items by color category.</span></span>
- <span data-ttu-id="68456-111">色の分類項目のそれぞれにショートカット キーを割り当てて、ユーザーがアイテムを分類しやすくします。</span><span class="sxs-lookup"><span data-stu-id="68456-111">Assign shortcut keys to each color category, enabling users to more easily categorize items.</span></span>
- <span data-ttu-id="68456-112">プログラムにより、または Outlook のユーザー インターフェイスでのユーザー操作により、色の分類項目を作成、削除、および変更します。</span><span class="sxs-lookup"><span data-stu-id="68456-112">Create, delete, and change color categories either programmatically, or by user action within the Outlook user interface.</span></span>

<span data-ttu-id="68456-113">Outlook オブジェクト モデルでは、分類項目の機能が利用できるように、メイン分類項目リスト内の単一のユーザー定義の色の分類項目を表す [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) オブジェクトが提供されます。</span><span class="sxs-lookup"><span data-stu-id="68456-113">To expose the functionality of categories, the Outlook object model provides a [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object that represents a single user-defined color category in the main category list.</span></span> <span data-ttu-id="68456-114">メイン分類項目リストには、Outlook のユーザー インターフェイスに表示される色の分類項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="68456-114">The main category list contains color categories that are presented in the Outlook user interface.</span></span> <span data-ttu-id="68456-115">このリストは [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) コレクションで表されます。</span><span class="sxs-lookup"><span data-stu-id="68456-115">The list is represented by the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="68456-116">**Category** オブジェクトを作成するには、**Categories** コレクションの [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="68456-116">To create a **Category** object, use the [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) method of the **Categories** collection.</span></span> <span data-ttu-id="68456-117">**Category** オブジェクトを作成すると、変更をすることができないグローバル一意識別子 (GUID) が作成されます。</span><span class="sxs-lookup"><span data-stu-id="68456-117">When you create a **Category** object, a globally unique identifier (GUID) is created, and this identifier cannot be changed.</span></span> <span data-ttu-id="68456-118">GUID は、[CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) プロパティに表されます。</span><span class="sxs-lookup"><span data-stu-id="68456-118">It is represented by the [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) property.</span></span> <span data-ttu-id="68456-119">ただし、**Category** オブジェクトの [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\))、[Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\))、および [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) プロパティの設定をすることで、色の分類項目と関連付けらた名前、色、およびショートカット キーをそれぞれ変更することができます。</span><span class="sxs-lookup"><span data-stu-id="68456-119">You can, however, change the name, color, and shortcut key associated with a color category by setting the [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), and [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) properties, respectively, of the **Category** object.</span></span> <span data-ttu-id="68456-120">**Color** プロパティを変更するには、そのプロパティの [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\))定数の設定または取得をします。</span><span class="sxs-lookup"><span data-stu-id="68456-120">You can change the **Color** property by setting or getting its [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)) constant.</span></span> <span data-ttu-id="68456-121">カスタム コントロールで色を再現するは、以下の、**Category** オブジェクトの読み取り専用のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="68456-121">To reproduce the color in a custom control, use the following read-only properties of the **Category** object:</span></span>

  - <span data-ttu-id="68456-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="68456-122">[expression  . CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span></span>

  - <span data-ttu-id="68456-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="68456-123">[expression  . CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span></span>

  - <span data-ttu-id="68456-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="68456-124">[expression  . CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span></span>

<span data-ttu-id="68456-125">これらのプロパティは **OLE\_COLOR** 値を返します。この値は、**Category** オブジェクトの **Color** プロパティに依存します。</span><span class="sxs-lookup"><span data-stu-id="68456-125">These properties return an OLE_COLOR value, which is dependent on the Color property of the Category object.</span></span>

<span data-ttu-id="68456-126">Outlook アイテムは分類項目名に基づいて表示されます。</span><span class="sxs-lookup"><span data-stu-id="68456-126">Outlook items are displayed based on the category name stored in the Categories property of that Outlook item.</span></span> <span data-ttu-id="68456-127">各項目のオブジェクトには、分類項目名を表すコンマ区切り文字列を格納した **Categories** プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="68456-127">Each item object has a **Categories** property that stores a comma-delimited string that represents category names.</span></span> <span data-ttu-id="68456-128">(たとえば、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトでは、**MailItem** の [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) プロパティを使用します)。</span><span class="sxs-lookup"><span data-stu-id="68456-128">(For example, for the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object, you would use the **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) property).</span></span> <span data-ttu-id="68456-129">これにより、メインの分類項目リストにない分類項目もアイテムに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="68456-129">This enables you to add a category to the item, even if the category is not present in the main category list.</span></span>


> [!NOTE]
> <span data-ttu-id="68456-p104">[!メモ] アイテムの **Categories** プロパティに、 **NameSpace** オブジェクトの **Categories** コレクションにない分類項目名が含まれている場合、Outlook アイテムに関連付けられたその分類項目名は表示されますが、関連付けられた色はありません。 **Item** オブジェクトの **Categories** プロパティは **Categories** コレクションを返しません。</span><span class="sxs-lookup"><span data-stu-id="68456-p104">If the **Categories** property of an item contains a category name that is not in the **Categories** collection of the **NameSpace** object, the category name associated with that Outlook item is displayed, but without an associated color. The **Categories** property on an **Item** object does not return a **Categories** collection.</span></span>

<span data-ttu-id="68456-132">次のコード例で、最初のプロシージャである olCatlist では、**Categories** コレクションが表す現在のユーザーのメイン分類項目リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="68456-132">In the following code example, the first procedure,  , gets the current user's main list of categories, represented by the Categories collection.</span></span> <span data-ttu-id="68456-133">次に、そのコレクションの **Category** オブジェクトに対して順に処理を行い、 **Name** プロパティおよび **CategoryID** プロパティを [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="68456-133">It then enumerates the **Category** objects in that collection, and writes the **Name** and **CategoryID** properties to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="68456-134">2 番目のプロシージャの AddACategory では、現在のユーザーのメイン分類項目リストを取得し、CategoryExists メソッドを使用して "ISV" という名前の分類項目がコレクションに存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="68456-134">The second procedure,  , gets the current user's main list of categories and uses the   method to check whether a category named "ISV" exists in the collection.</span></span> <span data-ttu-id="68456-135">"ISV" という名前の分類項目が存在しない場合、AddACategory は、**Categories** コレクションの **Add** メソッドを使用して、分類項目のメイン リストに "ISV" という名前の分類項目を追加し、濃い青色を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="68456-135">If no category with the name "ISV" exists,   adds a category named "ISV" to the main category list and assigns it a dark blue color by using the Add method of the Categories collection.</span></span> <span data-ttu-id="68456-136">また、この分類項目のショートカット キーに Ctrl + F11 を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="68456-136">It also assigns CTRL+F11 as the shortcut key for the category.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a><span data-ttu-id="68456-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="68456-137">See also</span></span>

- [<span data-ttu-id="68456-138">色の分類項目</span><span class="sxs-lookup"><span data-stu-id="68456-138">Color Categories</span></span>](color-categories.md)
