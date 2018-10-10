---
title: ActiveX データ オブジェクト (ADO) エラー
TOCTitle: ADO Errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee87da91086a010066ba94b294955eebdff7b636
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476627"
---
# <a name="ado-errors"></a><span data-ttu-id="92e15-102">ADO エラー一覧</span><span class="sxs-lookup"><span data-stu-id="92e15-102">ADO Errors</span></span>


<span data-ttu-id="92e15-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="92e15-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92e15-104">ADO エラーは、実行時エラーとしてプログラムに報告されます。</span><span class="sxs-lookup"><span data-stu-id="92e15-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="92e15-105">使用しているプログラミング言語のエラー トラッピング機構を使用すると、これらのエラーをトラッピングして処理できます。</span><span class="sxs-lookup"><span data-stu-id="92e15-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="92e15-106">たとえば、Visual Basic では、 **On Error** ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="92e15-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="92e15-107">Visual J++ では、 **try-catch** ブロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="92e15-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="92e15-108">Visual C++ では、ADO ライブラリへのアクセス方法によって操作が異なります。</span><span class="sxs-lookup"><span data-stu-id="92e15-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="92e15-109">\#のインポートは、 **try-catch**ブロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="92e15-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="92e15-110">それ以外の場合は、 **GetErrorInfo** を呼び出すことによって、明示的にエラー オブジェクトを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92e15-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="92e15-111">次の Visual Basic の sub プロシージャでは、ADO エラーをトラッピングする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="92e15-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

<span data-ttu-id="92e15-112">これは、**フォーム\_ロード**イベント プロシージャが 2 回、同じ**接続**オブジェクトを開こうとしてエラーを意図的に作成します。</span><span class="sxs-lookup"><span data-stu-id="92e15-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="92e15-113">**Open** メソッドが 2 度目に呼び出されたときに、エラー ハンドラーが起動されます。</span><span class="sxs-lookup"><span data-stu-id="92e15-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="92e15-114">この場合、エラーの種類は **adErrObjectOpen** であるため、プログラムの実行が再開される前に、エラー ハンドラーによって次のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="92e15-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="92e15-p103">このエラー メッセージには、Visual Basic の **Err** オブジェクトによって提供される各種の情報が含まれています。ただし、 **LastDLLError** 値は、ここでは該当しないため、表示されません。エラー番号は、どのエラーが発生したのかを示します。説明は、エラーを自分で処理しない場合に便利です。この説明をユーザーにそのまま表示できるためです。通常はアプリケーション用にカスタマイズされたメッセージを使用する方がよいのですが、すべてのエラーを予測することはできません。説明は、どのような問題が発生したのかを知るための一定の手掛かりとなります。サンプル コードでは、 **Connection** オブジェクトによってエラーが報告されています。ここでは、変数名ではなく、オブジェクトの型またはプログラム識別子が示されます。</span><span class="sxs-lookup"><span data-stu-id="92e15-p103">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here. The error number tells you which error has occurred. The description is useful in cases in which you do not want to handle the error yourself. You can simply pass it along to the user. Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong. In the sample code, the error was reported by the **Connection** object. You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <P><span data-ttu-id="92e15-p104">[!メモ] Visual Basic の <STRONG>Err</STRONG> オブジェクトには、最新のエラーに関する情報のみが格納されます。 <STRONG>Connection</STRONG> オブジェクトの ADO の <STRONG>Errors</STRONG> コレクションには、直近の ADO 操作によって発生したエラー 1 つにつき 1 つの <STRONG>Error</STRONG> オブジェクトが含まれています。複数のエラーを処理するときは、 <STRONG>Err</STRONG> オブジェクトの代わりに <STRONG>Errors</STRONG> コレクションを使用します。 <STRONG>Errors</STRONG> コレクションの詳細については、「 <A href="provider-errors.md">プロバイダー エラー</A>」を参照してください。ただし、有効な <STRONG>Connection</STRONG> オブジェクトがない場合は、 <STRONG>Err</STRONG> オブジェクトが ADO エラーに関する唯一の情報源です。</span><span class="sxs-lookup"><span data-stu-id="92e15-p104">The Visual Basic <STRONG>Err</STRONG> object only contains information about the most recent error. The ADO <STRONG>Errors</STRONG> collection of the <STRONG>Connection</STRONG> object contains one <STRONG>Error</STRONG> object for each error raised by the most recent ADO operation. Use the <STRONG>Errors</STRONG> collection rather than the <STRONG>Err</STRONG> object to handle multiple errors. For more information about the <STRONG>Errors</STRONG> collection, see <A href="provider-errors.md">Provider Errors</A>. However, if there is no valid <STRONG>Connection</STRONG> object, the <STRONG>Err</STRONG> object is the only source for information about ADO errors.</span></span></P>



<span data-ttu-id="92e15-p105">ADO エラーを発生させる可能性が高い操作とはどのようなものでしょうか。よくある ADO エラーは、 **Connection** や **Recordset** などのオブジェクトを開いたときや、データを更新しようとしたとき、プロバイダーがサポートしていないメソッドまたはプロパティを呼び出したときに発生するものです。</span><span class="sxs-lookup"><span data-stu-id="92e15-p105">What kinds of operations are likely to cause ADO errors? Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="92e15-p106">OLE DB エラーも、 **Errors** コレクションで実行時エラーとしてアプリケーションに渡すことができます。OLE DB のエラー番号の詳細については、「OLE DB Programmer's ReferenceOLE DB Programmer's Reference」 (英語) の Chapter 16 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92e15-p106">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection. For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>
