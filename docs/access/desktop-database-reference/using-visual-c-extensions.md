---
title: Visual C++ Extensions を使用する
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0076eae8a930688219da413a31d73a376bc53a39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479079"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="3d1a4-102">Visual C++ Extensions を使用する</span><span class="sxs-lookup"><span data-stu-id="3d1a4-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="3d1a4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d1a4-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="3d1a4-104">IADORecordBinding インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3d1a4-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="3d1a4-p101">ADO 用 Microsoft Visual C++ Extensions は、[Recordset](recordset-object-ado.md) オブジェクトのフィールドを C/C++ の変数に関連付け (つまりバインドし) ます。バインドされた **Recordset** の現在の行が変更されると、 **Recordset** 内のバインドされたすべてのフィールドが C/C++ 変数にコピーされます。コピーされるデータは、必要に応じて、C/C++ 変数の宣言データ型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p101">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables. If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="3d1a4-p102">**IADORecordBinding** インターフェイスの **BindToRecordset** メソッドは、フィールドを C/C++ の変数にバインドします。 **AddNew** メソッドは、バインドされた **Recordset** に新しい行を追加します。 **Update** メソッドは、C/C++ 変数の値で、 **Recordset** の新しい行のフィールドを設定したり、既存の行のフィールドを更新したりします。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p102">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables. The **AddNew** method adds a new row to the bound **Recordset**. The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="3d1a4-p103">**IADORecordBinding** インターフェイスは、 **Recordset** オブジェクトによって実装されます。ユーザー自身が実装をコーディングする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p103">The **IADORecordBinding** interface is implemented by the **Recordset** object. You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="3d1a4-113">バインディング エントリ</span><span class="sxs-lookup"><span data-stu-id="3d1a4-113">Binding Entries</span></span>

<span data-ttu-id="3d1a4-114">ADO 用の Visual C++ の拡張機能では、C または C++ の変数に、[レコード セット](recordset-object-ado.md)オブジェクトのフィールドをマップします。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-114">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="3d1a4-115">フィールドと変数の間のマッピングの定義は、*バインディング エントリ*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-115">The definition of a mapping between a field and a variable is called a *binding entry*.</span></span> <span data-ttu-id="3d1a4-116">マクロでは、数値、固定長と可変長のデータのバインドのエントリを提供します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-116">Macros provide binding entries for numeric, fixed-length, and variable-length data.</span></span> <span data-ttu-id="3d1a4-117">Visual C++ の拡張機能のクラス、 **CADORecordBinding**から派生したクラスでは、バインディング エントリおよび C または C++ の変数が宣言されています。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-117">The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**.</span></span> <span data-ttu-id="3d1a4-118">**CADORecordBinding**クラスは、バインディング エントリ マクロによって内部的に定義されます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-118">The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="3d1a4-119">内部的に、ADO は、OLE DB の**DBBINDING**構造体にこれらのマクロにパラメーターをマップし、移動し、フィールドと変数間のデータの変換を管理する OLE DB**アクセサー**オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-119">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables.</span></span> <span data-ttu-id="3d1a4-120">OLE DB とで構成されるデータを定義する 3 つの部分:*バッファー*のデータが格納されます。*ステータス*を示すかどうか、フィールドが正常にバッファーに格納された、または、フィールドに変数を復元する方法データの*長さ*。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-120">OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data.</span></span> <span data-ttu-id="3d1a4-121">( *OLE DB プログラマ リファレンス*、第 6 章を参照してください: 詳細についてはデータの取得と設定します)。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-121">(See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="3d1a4-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3d1a4-122">Header File</span></span>

<span data-ttu-id="3d1a4-123">ADO 用 Visual C++ Extensions を使用するには、アプリケーションに次のファイルをインクルードします。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="3d1a4-124">Recordset のフィールドのバインド</span><span class="sxs-lookup"><span data-stu-id="3d1a4-124">Binding Recordset Fields</span></span>

<span data-ttu-id="3d1a4-125">**Recordset のフィールドを C/C++ の変数にバインドするには**</span><span class="sxs-lookup"><span data-stu-id="3d1a4-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="3d1a4-126">**CADORecordBinding** クラスから派生するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="3d1a4-127">バインディング エントリおよび対応する C/C++ 変数を派生クラスで指定します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="3d1a4-128">ブラケットの間でバインディング エントリ**を開始\_ADO\_バインド**と**エンド\_ADO\_バインド**マクロ。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="3d1a4-129">マクロの末尾にコンマまたはセミコロンを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="3d1a4-130">適切な区切り文字がマクロによって自動的に指定されます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="3d1a4-131">C/C++ 変数にマップするフィールドごとに、バインディング エントリを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="3d1a4-132">適切なメンバーを使用して、 **ADO\_固定\_長さ\_エントリ**、 **ADO\_数値\_エントリ**、または**ADO\_変数\_長さ\_エントリ**マクロのファミリです。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="3d1a4-p107">アプリケーションで、 **CADORecordBinding** から派生したクラスのインスタンスを作成します。 **Recordset** から **IADORecordBinding** インターフェイスを取得します。その後、 **BindToRecordset** メソッドを呼び出して、 **Recordset** のフィールドを C/C++ 変数にバインドします。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p107">In your application, create an instance of the class derived from **CADORecordBinding**. Get the **IADORecordBinding** interface from the **Recordset**. Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="3d1a4-136">詳細については、「[Visual C++ Extensions の例](visual-c-extensions-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="3d1a4-137">インターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="3d1a4-137">Interface Methods</span></span>

<span data-ttu-id="3d1a4-p108">**IADORecordBinding** インターフェイスには、3 つのメソッド **BindToRecordset** 、 **AddNew** 、および **Update** があります。各メソッドに対する唯一の引数は、 **CADORecordBinding** から派生したクラスのインスタンスへのポインターです。したがって、 **AddNew** メソッドおよび **Update** メソッドでは、同名の ADO メソッドのパラメーターは指定できません。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p108">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**. The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**. Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="3d1a4-141">**構文**</span><span class="sxs-lookup"><span data-stu-id="3d1a4-141">**Syntax**</span></span>

<span data-ttu-id="3d1a4-142">**BindToRecordset** メソッドは、 **Recordset** のフィールドを C/C++ の変数に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="3d1a4-143">**AddNew** メソッドは、ADO の同名の [AddNew](addnew-method-ado.md) メソッドを呼び出して、 **Recordset** に新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="3d1a4-144">**Update** メソッドは、ADO の同名の [Update](update-method-ado.md) メソッドを呼び出して、 **Recordset** を更新します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="3d1a4-145">バインディング エントリ マクロ</span><span class="sxs-lookup"><span data-stu-id="3d1a4-145">Binding Entry Macros</span></span>

<span data-ttu-id="3d1a4-p109">バインディング エントリ マクロは、 **Recordset** のフィールドと変数の関連付けを定義します。開始および終了のマクロで、バインディング エントリのセットを区切ります。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p109">Binding entry macros define the association of a **Recordset** field and a variable. A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="3d1a4-p110">**adDate** や **adBoolean** などの固定長データ、 **adTinyInt** 、 **adInteger** 、 **adDouble** などの数値データ、および **adChar** 、 **adVarChar** 、 **adVarBinary** などの可変長データに対し、マクロ ファミリが用意されています。 **adVarNumeric** を除くすべての数値型は、固定長型でもあります。各マクロ ファミリは、それぞれ異なるパラメーター セットを持っているので、必要のないバインディング情報を除外できます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p110">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**. All numeric types, except for **adVarNumeric**, are also fixed-length types. Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="3d1a4-151">詳細について*OLE DB プログラマ リファレンス」* の「付録 a データ型を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="3d1a4-152">_**バインディング エントリの開始**_</span><span class="sxs-lookup"><span data-stu-id="3d1a4-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="3d1a4-153">**開始\_ADO\_バインド**(*クラス*)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="3d1a4-154">_**固定長データ**_</span><span class="sxs-lookup"><span data-stu-id="3d1a4-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="3d1a4-155">**ADO\_固定\_長さ\_エントリ**(*、序数、データ型、バッファーの状態の変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="3d1a4-156">**ADO\_固定\_長さ\_ENTRY2**(*序数、データ型、バッファーの変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="3d1a4-157">_**数値データ**_</span><span class="sxs-lookup"><span data-stu-id="3d1a4-157">_**Numeric Data**_</span></span>

<span data-ttu-id="3d1a4-158">**ADO\_数値\_エントリ**(*序数、データ型、バッファー、精度、小数点部桁数、ステータス、変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="3d1a4-159">**ADO\_数値\_ENTRY2**(*序数、データ型、バッファー、精度、スケールの変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="3d1a4-160">_**可変長データ**_</span><span class="sxs-lookup"><span data-stu-id="3d1a4-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="3d1a4-161">**ADO\_変数\_長さ\_エントリ**(*序数、データ型、バッファー、サイズ、状態、長さ、変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="3d1a4-162">**ADO\_変数\_長さ\_ENTRY2**(*序数、データ型、バッファー、サイズ、状態の変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="3d1a4-163">**ADO\_変数\_長さ\_ENTRY3**(*序数、データ型、バッファー、サイズ、長さ、変更*を)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="3d1a4-164">**ADO\_変数\_長さ\_ENTRY4**(*、序数、データ型、バッファーのサイズを変更*)</span><span class="sxs-lookup"><span data-stu-id="3d1a4-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="3d1a4-165">_**バインディング エントリの終了**_</span><span class="sxs-lookup"><span data-stu-id="3d1a4-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="3d1a4-166">**エンド\_ADO\_バインド**()</span><span class="sxs-lookup"><span data-stu-id="3d1a4-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d1a4-167">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d1a4-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="3d1a4-168">説明</span><span class="sxs-lookup"><span data-stu-id="3d1a4-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-169"><em>Class</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-170">バインディング エントリおよび C/C++ 変数を定義するクラスです。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-172">C/C++ 変数に対応する <strong>Recordset</strong> フィールドの、1 から始まるインデックスです。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-p111">C/C++ 変数に対する ADO での等価のデータ型です (有効なデータ型の一覧については、<a href="datatypeenum.md">DataTypeEnum</a> のトピックを参照)。<strong>Recordset</strong> フィールドの値は、必要に応じてこのデータ型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p111">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types). The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-176"><em>Buffer</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-177"><strong>Recordset</strong> フィールドを格納する C/C++ 変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-178"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-p112">バイト数で示す <em>Buffer</em> の最大サイズです。<em>Buffer</em> に可変長文字列を格納する場合は、末尾のゼロを含んだサイズになります。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-p112">Maximum size in bytes of <em>Buffer</em>. If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-181"><em>Status</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-182"><em>Buffer</em> の内容が有効かどうか、および <em>DataType</em> へのフィールドの変換が成功したかどうかを示す変数の名前です。
</span><span class="sxs-lookup"><span data-stu-id="3d1a4-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="3d1a4-183">この変数で最も重要な 2 つの値は、変換が成功したことを示す <strong>adFldOK</strong> と、フィールドの値が VT_NULL 型の VARIANT であって単なる空ではないことを示す <strong>adFldNull</strong> です。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="3d1a4-184"><em>ステータス</em>の値が次の表に記載されている&quot;のステータス値。&quot;</span><span class="sxs-lookup"><span data-stu-id="3d1a4-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-185"><em>変更</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-186">ブール型のフラグです。TRUE の場合は、ADO が対応する <strong>Recordset</strong> フィールドを <em>Buffer</em> の値で更新できることを示します。
</span><span class="sxs-lookup"><span data-stu-id="3d1a4-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="3d1a4-187">バインドされたフィールドを ADO が更新できるようにするには、ブール型の <em>modify</em> パラメーターを TRUE に設定します。確認だけでフィールドを変更しない場合は FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-188"><em>Precision</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-189">数値変数で表すことのできる桁数です。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-190"><em>Scale</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-191">数値変数での小数点以下の桁数です。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="3d1a4-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-193"><em>Buffer</em> 内のデータの実際の長さを格納する 4 バイト変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="3d1a4-194">Status の値</span><span class="sxs-lookup"><span data-stu-id="3d1a4-194">Status Values</span></span>

<span data-ttu-id="3d1a4-195">*Status*変数の値は、フィールドが変数に正常にコピーされたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="3d1a4-196">データを設定するときは、*Status* を **adFldNull** に設定することで、**Recordset** フィールドを Null に設定する必要があることを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d1a4-197">定数</span><span class="sxs-lookup"><span data-stu-id="3d1a4-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="3d1a4-198">値</span><span class="sxs-lookup"><span data-stu-id="3d1a4-198">Value</span></span></p></th>
<th><p><span data-ttu-id="3d1a4-199">説明</span><span class="sxs-lookup"><span data-stu-id="3d1a4-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-201">0</span><span class="sxs-lookup"><span data-stu-id="3d1a4-201">0</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-202">Null ではないフィールド値が返されました。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-204">1</span><span class="sxs-lookup"><span data-stu-id="3d1a4-204">1</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-205">バインディングが無効です。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-207">2</span><span class="sxs-lookup"><span data-stu-id="3d1a4-207">2</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-208">符号の不一致またはデータのオーバーフロー以外の理由で、値を変換できませんでした。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-210">3</span><span class="sxs-lookup"><span data-stu-id="3d1a4-210">3</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-211">フィールドを取得するときは、Null 値が返されたことを示します。
</span><span class="sxs-lookup"><span data-stu-id="3d1a4-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="3d1a4-212">フィールドを設定するときは、フィールドが <strong>NULL</strong> そのものをエンコードできない場合 (文字配列または整数など)、フィールドを <strong>NULL</strong> に設定する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-214">4</span><span class="sxs-lookup"><span data-stu-id="3d1a4-214">4</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-215">可変長データまたは数値の桁が切り捨てられました。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-217">5</span><span class="sxs-lookup"><span data-stu-id="3d1a4-217">5</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-218">値は符号付きですが、変数のデータ型は符号なしです。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-220">6</span><span class="sxs-lookup"><span data-stu-id="3d1a4-220">6</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-221">変数のデータ型に格納できる値を超えています。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-223">7</span><span class="sxs-lookup"><span data-stu-id="3d1a4-223">7</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-224">未知の列の型であり、フィールドは既に開かれています。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-226">8</span><span class="sxs-lookup"><span data-stu-id="3d1a4-226">8</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-227">フィールド値を特定できませんでした。たとえば、新規の未割り当てフィールドで既定値が設定されていません。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-229">9</span><span class="sxs-lookup"><span data-stu-id="3d1a4-229">9</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-230">更新時に、データの書き込み権限が与えられていませんでした。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-232">10</span><span class="sxs-lookup"><span data-stu-id="3d1a4-232">10</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-233">更新時に、フィールド値が列の整合性に違反していました。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-235">11</span><span class="sxs-lookup"><span data-stu-id="3d1a4-235">11</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-236">更新時に、フィールド値が列のスキーマに違反していました。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1a4-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-238">12</span><span class="sxs-lookup"><span data-stu-id="3d1a4-238">12</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-239">更新時に、無効なステータス パラメーターがありました。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1a4-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="3d1a4-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1a4-241">13</span><span class="sxs-lookup"><span data-stu-id="3d1a4-241">13</span></span></p></td>
<td><p><span data-ttu-id="3d1a4-242">更新時に、既定値が使用されました。</span><span class="sxs-lookup"><span data-stu-id="3d1a4-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>
