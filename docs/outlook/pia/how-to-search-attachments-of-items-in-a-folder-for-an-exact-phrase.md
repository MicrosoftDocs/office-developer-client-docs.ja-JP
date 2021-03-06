---
title: フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3d14da44731810308d57ba0e70f9651f3105aad0
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773716"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a>フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する

この例では、受信トレイ内のアイテムへの添付ファイルで、文字列 "office" を完全一致で検索します。

## <a name="example"></a>例

このコード例では、DAV Searching and Locating (DASL) 構文を使用してクエリを指定します。 フィルターを作成するために、まずクイック検索が既定のストアで有効になっているかどうかをチェックし、添付ファイル内で "office" を完全一致で検索する **ci\_phrasematch** キーワードを使用するかどうかを決定します。 その後で、この例では、受信トレイの [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) メソッドにフィルターを適用して、[Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia) オブジェクトで結果を取得します。 さらに、このコード例では、**Table** で返された各アイテムの件名を表示します。

このコード例では、アイテムの **Attachments** プロパティを指定するために、名前空間の表現として https://schemas.microsoft.com/mapi/proptag/0x0EA5001E を使用しています。 **ci\_phrasematch** キーワードの構文は次のとおりです。

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```


```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

