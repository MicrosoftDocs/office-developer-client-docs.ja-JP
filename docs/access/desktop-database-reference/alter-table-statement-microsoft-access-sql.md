---
title: ALTER TABLE ステートメント (Microsoft Access SQL)
TOCTitle: ALTER TABLE Statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8fc826d438973b4d079e9b90d3663ab755821cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479190"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="408b6-102">ALTER TABLE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="408b6-102">ALTER TABLE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="408b6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="408b6-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="408b6-104">[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントで作成されたテーブルのデザインを変更します。</span><span class="sxs-lookup"><span data-stu-id="408b6-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>


> [!NOTE]
> <span data-ttu-id="408b6-p101">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース以外のデータベースの ALTER TABLE または DDL (データ定義言語) ステートメントをサポートしません。代わりに、DAO の Create メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="408b6-p101">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases. Use the DAO Create methods instead.</span></span>



## <a name="syntax"></a><span data-ttu-id="408b6-107">構文</span><span class="sxs-lookup"><span data-stu-id="408b6-107">Syntax</span></span>

<span data-ttu-id="408b6-108">*テーブル*の ALTER TABLE {追加 {*フィールド型*の列の\[(*サイズ*)\] \[NOT NULL\] \[制約*インデックス*\] |ALTER COLUMN*フィールド型*\[(*サイズ*)\] |制約*multifieldindex*} |ドロップ {列の*フィールド*に制約*indexname*}}</span><span class="sxs-lookup"><span data-stu-id="408b6-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="408b6-109">ALTER TABLE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="408b6-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="408b6-110">指定項目</span><span class="sxs-lookup"><span data-stu-id="408b6-110">Part</span></span></p></th>
<th><p><span data-ttu-id="408b6-111">説明</span><span class="sxs-lookup"><span data-stu-id="408b6-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="408b6-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="408b6-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-113">変更するテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="408b6-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408b6-114"><em>field</em></span><span class="sxs-lookup"><span data-stu-id="408b6-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-p102">引数 table に追加、または引数 table から削除するフィールドの名前。または、table で変更するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="408b6-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="408b6-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="408b6-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-118">引数 <em>field</em> のデータ型。</span><span class="sxs-lookup"><span data-stu-id="408b6-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408b6-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="408b6-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-120">バイト数で表したフィールド サイズ。テキスト型 (Text) およびバイナリ型 (Binary) フィールドのみ指定します。</span><span class="sxs-lookup"><span data-stu-id="408b6-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="408b6-121"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="408b6-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-p103">引数 <em>field</em> のインデックス。このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="408b6-p103">The index for <em>field</em>. For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408b6-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="408b6-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-p104">引数 <em>table</em> に追加する複数フィールド インデックスの定義。このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="408b6-p104">The definition of a multiple-field index to be added to <em>table</em>. For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="408b6-127"><em>indexname</em></span><span class="sxs-lookup"><span data-stu-id="408b6-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="408b6-128">削除する複数フィールド インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="408b6-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="408b6-129">解説</span><span class="sxs-lookup"><span data-stu-id="408b6-129">Remarks</span></span>

<span data-ttu-id="408b6-p105">ALTER TABLE ステートメントを使用すると、次の方法で既存のテーブルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="408b6-p105">Using the ALTER TABLE statement you can alter an existing table in several ways. You can:</span></span>

  - <span data-ttu-id="408b6-p106">テーブルに新しいフィールドを追加するには、ADD COLUMN 句を使用します。フィールド名およびデータ型を指定し、テキスト型フィールドとバイナリ型フィールドの場合はサイズ (省略可) も指定します。たとえば、次のステートメントにより、"Notes" という名前の 25 バイトのテキスト型フィールドが Employees テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="408b6-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
    ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
    ```
    
    <span data-ttu-id="408b6-p107">また、追加したフィールドにインデックスを定義することもできます。単一フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="408b6-p107">You can also define an index on that field. For more information on single-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
    <span data-ttu-id="408b6-137">フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。</span><span class="sxs-lookup"><span data-stu-id="408b6-137">If you specify NOT NULL for a field then new records are required to have valid data in that field.</span></span>

  - <span data-ttu-id="408b6-p108">既存のフィールドのデータ型を変更するには、ALTER COLUMN 句を使用します。フィールド名および新しいデータ型を指定し、テキスト型フィールドとバイナリ型フィールドの場合はサイズ (省略可) も指定します。たとえば、次のステートメントでは、Employees テーブルにある "ZipCode" という名前のフィールドのデータ型を整数型から 10 バイトのテキスト型に変更します。</span><span class="sxs-lookup"><span data-stu-id="408b6-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
    ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
    ```

  - <span data-ttu-id="408b6-p109">複数フィールド インデックスを追加するには、ADD CONSTRAINT 句を使用します。複数フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="408b6-p109">Use ADD CONSTRAINT to add a multiple-field index. For more information on multiple-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>

  - <span data-ttu-id="408b6-p110">フィールドを削除するには、DROP COLUMN 句を使用します。フィールド名のみを指定します。</span><span class="sxs-lookup"><span data-stu-id="408b6-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

  - <span data-ttu-id="408b6-p111">複数フィールド インデックスを削除するには、DROP CONSTRAINT 句を使用します。予約語 CONSTRAINT の後にインデックス名のみを指定します。</span><span class="sxs-lookup"><span data-stu-id="408b6-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="408b6-147">一度に複数のフィールドおよびインデックスを追加または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="408b6-147">You cannot add or delete more than one field or index at a time.</span></span></P>
> <LI>
> <P><span data-ttu-id="408b6-148"><A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> ステートメントを使用すると、単一フィールド インデックスまたは複数フィールド インデックスをテーブルに追加できます。また、ALTER TABLE ステートメントや CREATE INDEX ステートメントで作成したインデックスは、ALTER TABLE ステートメントまたは <A href="drop-statement-microsoft-access-sql.md">DROP</A> ステートメントを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="408b6-148">You can use the <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the <A href="drop-statement-microsoft-access-sql.md">DROP</A> statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span></P>
> <LI>
> <P><span data-ttu-id="408b6-p112">NOT NULL は、単一フィールド、または名前付き CONSTRAINT 句の内部で使用できます。名前付き CONSTRAINT 句は、単一フィールドまたは複数フィールドのどちらかの名前付き CONSTRAINT 句に適用されます。ただし、NOT NULL の制約を適用できるのはフィールドに対して一度のみです。再度適用しようとした場合は実行時エラーになります。 
</span><span class="sxs-lookup"><span data-stu-id="408b6-p112">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once restuls in a run-time error.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="408b6-152">使用例</span><span class="sxs-lookup"><span data-stu-id="408b6-152">Example</span></span>

<span data-ttu-id="408b6-153">次の使用例では、データ型が通貨型 ( **Money** ) である Salary フィールドを Employees テーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="408b6-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="408b6-154">次の使用例では、Salary フィールドのデータ型を通貨型 ( **Money** ) から文字型 ( **Char** ) に変更します。</span><span class="sxs-lookup"><span data-stu-id="408b6-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="408b6-155">次の使用例では、Salary フィールドを Employees テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="408b6-155">This example removes the Salary field from the Employees table.</span></span>

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="408b6-p113">次の使用例では、外部キーを Orders テーブルに追加します。外部キーは、EmployeeID フィールドに基づき、Employees テーブルの EmployeeID フィールドを参照します。この例では、REFERENCES 句の Employees テーブルの後に EmployeeID フィールドをリストする必要はありません。EmployeeID が Employees テーブルの主キーだからです。</span><span class="sxs-lookup"><span data-stu-id="408b6-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="408b6-159">次の使用例では、外部キーを Orders テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="408b6-159">This example removes the foreign key from the Orders table.</span></span>

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```