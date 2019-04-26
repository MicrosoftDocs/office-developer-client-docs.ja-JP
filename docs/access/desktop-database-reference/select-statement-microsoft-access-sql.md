---
title: SELECT ステートメント (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: 962e425c2c69511b6d7770fb03e954588249cf2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314638"
---
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="afbd8-102">SELECT ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="afbd8-102">SELECT Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="afbd8-103">**適用先**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="afbd8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="afbd8-104">Microsoft Access データベース エンジンにデータベースの情報をレコード セットとして返すように指示します。</span><span class="sxs-lookup"><span data-stu-id="afbd8-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="afbd8-105">構文</span><span class="sxs-lookup"><span data-stu-id="afbd8-105">Syntax</span></span>

<span data-ttu-id="afbd8-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span><span class="sxs-lookup"><span data-stu-id="afbd8-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="afbd8-107">\] \[GROUP BY…</span><span class="sxs-lookup"><span data-stu-id="afbd8-107">GROUP BY</span></span> <span data-ttu-id="afbd8-108">\] \[HAVING…</span><span class="sxs-lookup"><span data-stu-id="afbd8-108">HAVING</span></span> <span data-ttu-id="afbd8-109">\] \[ORDER BY…</span><span class="sxs-lookup"><span data-stu-id="afbd8-109">ORDER BY</span></span> <span data-ttu-id="afbd8-110">\] \[WITH OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="afbd8-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="afbd8-111">SELECT ステートメントでは次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="afbd8-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="afbd8-112">パーツ</span><span class="sxs-lookup"><span data-stu-id="afbd8-112">Part</span></span></p></th>
<th><p><span data-ttu-id="afbd8-113">説明</span><span class="sxs-lookup"><span data-stu-id="afbd8-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afbd8-114"><em>predicate</em></span><span class="sxs-lookup"><span data-stu-id="afbd8-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="afbd8-p102"><a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL、DISTINCT、DISTINCTROW、TOP</a> のいずれかの述語。これらの述語は、返されるレコードの数を制限するために使用します。指定がない場合は、ALL になります。  </span><span class="sxs-lookup"><span data-stu-id="afbd8-p102">One of the following predicates: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a>. You use the predicate to restrict the number of records returned. If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="afbd8-118">指定したテーブル (複数可) のすべてのフィールドを選択するよう指定します。</span><span class="sxs-lookup"><span data-stu-id="afbd8-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afbd8-119"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="afbd8-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="afbd8-120">レコードを選択するフィールドを含んだテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="afbd8-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afbd8-121"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="afbd8-121"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="afbd8-p103">取得するデータを含んだフィールドの名前。 複数のフィールドを含めた場合は、リストした順序で取得されます。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p103">The names of the fields containing the data you want to retrieve. If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afbd8-124"><em>alias1</em>、<em>alias2</em></span><span class="sxs-lookup"><span data-stu-id="afbd8-124"><em>alias1</em>  ,  <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="afbd8-125">
            <em>table</em> 内の元の列名の代わりに列見出しとして使用する名前。</span><span class="sxs-lookup"><span data-stu-id="afbd8-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afbd8-126"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="afbd8-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="afbd8-127">取得するデータを含んだテーブル (複数可) の名前。</span><span class="sxs-lookup"><span data-stu-id="afbd8-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afbd8-128"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="afbd8-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="afbd8-129">
            <em>tableexpression</em> のテーブルが現在のデータベースにない場合に、それを含むデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="afbd8-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="afbd8-130">注釈</span><span class="sxs-lookup"><span data-stu-id="afbd8-130">Remarks</span></span>

<span data-ttu-id="afbd8-131">この操作を実行するため、Microsoft Jet データベース エンジンは指定されたテーブル (複数可) を検索して、選択した列を抽出し、条件に一致する行を選択して、結果行を指定の順序に並べ替えたり、グループ化したりします。</span><span class="sxs-lookup"><span data-stu-id="afbd8-131">To perform this operation, the Microsoft® Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="afbd8-132">SELECT ステートメントはデータベース内のデータを変更することはありません。</span><span class="sxs-lookup"><span data-stu-id="afbd8-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="afbd8-p104">通常、SELECT は SQL ステートメントの先頭に記述します。ほとんどの SQL ステートメントは SELECT ステートメントまたは [SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p104">SELECT is usually the first word in an SQL statement. Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="afbd8-135">SELECT ステートメントの最小限の構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="afbd8-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="afbd8-136">SELECT *fields* FROM *table*</span><span class="sxs-lookup"><span data-stu-id="afbd8-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="afbd8-p105">アスタリスク (\*) を使用すると、テーブル内のすべてのフィールドが選択できます。次の例では、Employees テーブルにあるすべてのフィールドが選択されます。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p105">You can use an asterisk (\*) to select all fields in a table. The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="afbd8-p106">FROM 句で複数のテーブルに含まれるフィールドの場合は、その前にテーブル名と **.** (ドット) 演算子を付けます。 次の例では、Department フィールドが Employees テーブルと Supervisors テーブルの両方に含まれます。 この SQL ステートメントは、Employees テーブルから部署を選択し、Supervisors テーブルから監督者名を選択します。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p106">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.** (dot) operator. In the following example, the Department field is in both the Employees table and the Supervisors table. The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="afbd8-p107">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span><span class="sxs-lookup"><span data-stu-id="afbd8-p107">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="afbd8-p108">使用する集約関数やクエリで返される **Field** オブジェクト名があいまいな場合や重複する場合は、AS 句を使用して **Field** オブジェクトの代替名を指定する必要があります。 次の例では、タイトルに HeadCount を使用して、結果の **Recordset** オブジェクトで返された **Field** オブジェクトに名前を付けています。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p108">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object. The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="afbd8-p109">SELECT ステートメントではこの他にも、返されるデータを制限して整理する句を使用できます。 詳しくは、使用する句のヘルプ トピックをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p109">You can use the other clauses in a SELECT statement to further restrict and organize your returned data. For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="afbd8-150">[UtterAccess](https://www.utteraccess.com) コミュニティで**提供されるリンク**。</span><span class="sxs-lookup"><span data-stu-id="afbd8-150">**Links provided by:** Community Member Icon The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="afbd8-151">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="afbd8-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="afbd8-152">SQL to VBA Formatter</span><span class="sxs-lookup"><span data-stu-id="afbd8-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="afbd8-153">Viewing Records Within A Defined Range</span><span class="sxs-lookup"><span data-stu-id="afbd8-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="afbd8-154">例</span><span class="sxs-lookup"><span data-stu-id="afbd8-154">Example</span></span>

<span data-ttu-id="afbd8-p111">次に示す一部の使用例では、Employees テーブルに Salary フィールドが含まれていると仮定しています。実際には、ノースウィンド データベースの Employees テーブルにこのフィールドは含まれていないので注意してください。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p111">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table. Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="afbd8-p112">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span><span class="sxs-lookup"><span data-stu-id="afbd8-p112">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="afbd8-159">次の使用例では、PostalCode フィールドにエントリがあるレコードの数を調べ、その値が返されるフィールドとして Tally フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="afbd8-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="afbd8-160">次の使用例では、社員数と平均給与額および最高給与額を表示します。</span><span class="sxs-lookup"><span data-stu-id="afbd8-160">This example shows the number of employees and the average and maximum salaries.</span></span>

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="afbd8-p113">**Sub** プロシージャである EnumFields には、呼び出し元のプロシージャから **Recordset** オブジェクトが渡されます。次に **Recordset** のフィールドがフォーマットされ、 **Debug** ウィンドウに出力されます。変数は、必要な出力フィールド幅を示します。一部のフィールドが表示されない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="afbd8-p113">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure. The procedure then formats and prints the fields of the **Recordset** to the **Debug** window. The variable is the desired printed field width. Some fields may be truncated.</span></span>

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




