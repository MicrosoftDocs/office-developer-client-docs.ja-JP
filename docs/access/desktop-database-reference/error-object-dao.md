---
title: エラー オブジェクトのデータ アクセス オブジェクトの (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62b195907d5acc05832c1feac45165aadd9e14d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477521"
---
# <a name="error-object-dao"></a><span data-ttu-id="3ee5e-102">Error オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ee5e-102">Error Object (DAO)</span></span>


<span data-ttu-id="3ee5e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ee5e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ee5e-104">**Error** オブジェクトにはデータ アクセス エラーに関する詳細が含まれ、各オブジェクトが DAO を扱う 1 回の操作に対応しています。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ee5e-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3ee5e-105">Remarks</span></span>

<span data-ttu-id="3ee5e-p101">DAO を扱うすべての操作では、1 つまたは複数のエラーが生成される可能性があります。たとえば、ODBC サーバーを呼び出すと、データベース サーバーのエラー、ODBC のエラー、および DAO エラーが発生する可能性があります。このようなエラーが発生するたびに、 **DBEngine** オブジェクトの **Errors** コレクションに 1 つの **Error** オブジェクトが追加されます。したがって、単一のイベントで **Errors** コレクションに複数の **Error** オブジェクトが格納される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-p101">Any operation involving DAO can generate one or more errors. For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error. As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object. A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="3ee5e-p102">後続の DAO 操作によってエラーが生成されると、 **Errors** コレクションがクリアされ、1 つ以上の新しい **Error** オブジェクトが **Errors** コレクションに追加されます。エラーを生成しない DAO 操作は、 **Errors** コレクションには影響しません。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-p102">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection. DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="3ee5e-p103">**Errors** コレクションの **Error** オブジェクトのセットにより、1 つのエラーが記述されます。最初の **Error** オブジェクトが最も低いレベルのエラー (作成元エラー)、2 番目が次に高いレベルのエラーで、以降同様です。たとえば、 **[Recordset](recordset-object-dao.md)** オブジェクトを開こうとしたときに ODBC エラーが発生した場合、最初の **Error** オブジェクト ( **Errors**(0)) には最も低いレベルの ODBC エラーが含まれ、後続のエラーには ODBC のさまざまなレイヤーによって返された ODBC エラーが含まれます。この場合、ODBC ドライバー マネージャー、さらに場合によってはドライバー自体が別々の **Error** オブジェクトを返します。最後の **Error** オブジェクト ( **Errors.Count-** 1) には、オブジェクトが開かれなかったことを示す DAO エラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-p103">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="3ee5e-p104">**Errors** コレクションの特定のエラーを列挙すると、エラー処理ルーチンでエラーの原因と発生源をより正確に特定し、適切な修復処理を実行できます。 **Error** オブジェクトのプロパティを参照すると、各エラーに関する次のような詳細を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-p104">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover. You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="3ee5e-119">エラーがトラップされない場合に画面に表示されるエラー メッセージのテキストを含む **[Description](error-description-property-dao.md)** プロパティ。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="3ee5e-120">エラー定数の長整数型 (Long integer) の値を含む **[Number](error-number-property-dao.md)** プロパティ。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="3ee5e-p105">エラーを発生させたオブジェクトを識別する **[Source](error-source-property-dao.md)** プロパティ。これは特に、ODBC データ ソースへの要求に対応する **Errors** コレクションに複数の **Error** オブジェクトがある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-p105">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="3ee5e-123">エラーが発生した場合に、そのエラーについて Microsoft Windows の適切なヘルプ ファイルを示す (ある場合) **HelpFile** プロパティおよび Microsoft Windows の適切なヘルプ トピックを示す (ある場合) **HelpContext** プロパティ。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="3ee5e-124">[!メモ] Microsoft Visual Basic for Applications (VBA) でプログラミングするときに、 <STRONG>New</STRONG> キーワードを使用して、オブジェクトがコレクションに追加される前にエラーが発生するオブジェクトを作成すると、新しいオブジェクトは <STRONG>DBEngine</STRONG> オブジェクトに関連付けられていないため、 <STRONG>DBEngine</STRONG> オブジェクトの <STRONG>Errors</STRONG> コレクションに、そのオブジェクト エラーのエントリが追加されません。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the <STRONG>New</STRONG> keyword to create an object that subsequently causes an error before that object has been appended to a collection, the <STRONG>DBEngine</STRONG> object's <STRONG>Errors</STRONG> collection won't contain an entry for that object's error, because the new object is not associated with the <STRONG>DBEngine</STRONG> object.</span></span> <span data-ttu-id="3ee5e-125">ただし、VBA の <STRONG>Err</STRONG> オブジェクトでエラー情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-125">However, the error information is available in the VBA <STRONG>Err</STRONG> object.</span></span> <span data-ttu-id="3ee5e-126">データ アクセス エラーが発生する可能性がある場合、VBA エラー処理コードで <STRONG>Errors</STRONG> コレクションを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-126">Your VBA error-handling code should examine the <STRONG>Errors</STRONG> collection whenever you anticipate a data access error.</span></span> <span data-ttu-id="3ee5e-127">集中化したエラー ハンドラーを記述している場合は、VBA の <STRONG>Err</STRONG> オブジェクトをテストして、 <STRONG>Errors</STRONG> コレクションのエラー情報が該当するかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-127">If you are writing a centralized error handler, test the VBA <STRONG>Err</STRONG> object to determine if the error information in the <STRONG>Errors</STRONG> collection is valid.</span></span> <span data-ttu-id="3ee5e-128">場合の<STRONG>Number</STRONG>プロパティ (DBEngine.Errors.Count - 1)<STRONG>エラー</STRONG>のコレクションの最後の要素の<STRONG>Err</STRONG>オブジェクトに一致する値をすることができますをクリックして一連の<STRONG>Select Case</STRONG>ステートメント特定の DAO エラーを識別するか、エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-128">If the <STRONG>Number</STRONG> property of the last element of the <STRONG>Errors</STRONG> collection (DBEngine.Errors.Count - 1) and the value of the <STRONG>Err</STRONG> object match, you can then use a series of <STRONG>Select Case</STRONG> statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="3ee5e-129">これらの値が一致しない場合は、 <A href="errors-refresh-method-dao.md">Errors</A> コレクションに対して <STRONG><STRONG>Refresh</STRONG></STRONG> メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-129">If they do not match, use the <STRONG><A href="errors-refresh-method-dao.md">Refresh</A></STRONG> method on the <STRONG>Errors</STRONG> collection.</span></span></P>



## <a name="example"></a><span data-ttu-id="3ee5e-130">例</span><span class="sxs-lookup"><span data-stu-id="3ee5e-130">Example</span></span>

<span data-ttu-id="3ee5e-131">この例では、エラーを発生させてトラップし、 **Error** オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="3ee5e-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
   Dim dbsTest As Database 
 
   On Error GoTo ErrorHandler 
 
   ' Intentionally trigger an error. 
   Set dbsTest = OpenDatabase("NoDatabase") 
 
   Exit Sub 
 
ErrorHandler: 
   Dim strError As String 
   Dim errLoop As Error 
 
   ' Enumerate Errors collection and display properties of  
   ' each Error object. 
   For Each errLoop In Errors 
      With errLoop 
         strError = _ 
            "Error #" & .Number & vbCr 
         strError = strError & _ 
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```
