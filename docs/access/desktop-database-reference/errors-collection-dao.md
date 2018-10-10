---
title: Errors コレクション (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f118bab1a73d29858776e33149c54aab39ef5cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476550"
---
# <a name="errors-collection-dao"></a><span data-ttu-id="ef606-102">Errors コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef606-102">Errors Collection (DAO)</span></span>


<span data-ttu-id="ef606-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef606-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ef606-104">**Errors** コレクションには、格納されているすべての **Error** オブジェクトが含まれ、それぞれが DAO に関する単一の操作に対応しています。</span><span class="sxs-lookup"><span data-stu-id="ef606-104">An **Errors** collection contains all stored **Error** objects, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef606-105">注釈</span><span class="sxs-lookup"><span data-stu-id="ef606-105">Remarks</span></span>

<span data-ttu-id="ef606-p101">DAO オブジェクトに関係するすべての操作では、1 つ以上のエラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **DBEngine** オブジェクトの **Errors** コレクションに追加されます。別の DAO 操作によってエラーが発生すると、**Errors** コレクションがクリアされ、**Errors** コレクションに **Error** オブジェクトの新しいセットが配置されます。**Errors** コレクションの最高値のオブジェクト (DBEngine.Errors.Count - 1) は、Microsoft Visual Basic for Applications (VBA) の **Err** オブジェクトがレポートするエラーに対応します。</span><span class="sxs-lookup"><span data-stu-id="ef606-p101">Any operation involving DAO objects can generate one or more errors. As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **DBEngine** object. When another DAO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection. The highest-numbered object in the **Errors** collection (DBEngine.Errors.Count - 1) corresponds to the error reported by the Microsoft Visual Basic for Applications (VBA) **Err** object.</span></span>

<span data-ttu-id="ef606-110">エラーを生成しない DAO 操作が **Errors** コレクションに影響を及ぼすことはありません。</span><span class="sxs-lookup"><span data-stu-id="ef606-110">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="ef606-111">**Errors** コレクションの要素は、一般に他のコレクション内にあるので、追加されません。したがって、 **Errors** コレクションでは、 **Append** メソッドと **Delete** メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ef606-111">Elements of the **Errors** collection aren't appended as they typically are with other collections, so the **Errors** collection doesn't support the **Append** and **Delete** methods.</span></span>

<span data-ttu-id="ef606-p102">**Errors** コレクションの **Error** オブジェクトのセットは、単一のエラーを表します。最初の **Error** オブジェクトが最低レベルのエラーで、2 番目のエラーが次に高いレベルのエラーになり、その後も同様です。たとえば、 **[Recordset](recordset-object-dao.md)** オブジェクトを開く際に ODBC エラーが発生すると、最初のエラー オブジェクトに最低レベルの ODBC エラーが含まれ、その後のエラーに ODBC のさまざまなレイヤーが返す ODBC エラーが含まれます。この場合、ODBC ドライバー マネージャーおよびドライバー自体も個別の **Error** オブジェクトを返します。最後の **Error** オブジェクトには、オブジェクトを開くことができなかったことを示す DAO エラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ef606-p102">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error, the second the next higher level, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first error object contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="ef606-117">**Errors** コレクションの特定のエラーを列挙することにより、エラー処理ルーチンは、エラーの原因、発生源、および適切な回復手順をより正確に特定できます。</span><span class="sxs-lookup"><span data-stu-id="ef606-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ef606-p103">[!メモ] <STRONG>New</STRONG> キーワードを使用してオブジェクトを作成し、 <STRONG>Errors</STRONG> コレクションに追加される前またはその最中にエラーが発生した場合、新しいオブジェクトは <STRONG>DBEngine</STRONG> オブジェクトに関連付けられていないので、このオブジェクトに関するエラー情報はコレクションに追加されません。ただし、このエラー情報は、VBA の <STRONG>Err</STRONG> オブジェクトで参照できます。</span><span class="sxs-lookup"><span data-stu-id="ef606-p103">If you use the <STRONG>New</STRONG> keyword to create an object that causes an error either before or while being placed into the <STRONG>Errors</STRONG> collection, the collection doesn't contain error information about that object, because the new object is not associated with the <STRONG>DBEngine</STRONG> object. However, the error information is available in the VBA <STRONG>Err</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="ef606-120">例</span><span class="sxs-lookup"><span data-stu-id="ef606-120">Example</span></span>

<span data-ttu-id="ef606-121">この例では、エラーを発生させてトラップし、 **Error** オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="ef606-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```
