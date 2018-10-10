---
title: AbsolutePage プロパティ、PageCount プロパティ、および PageSize プロパティの使用例 (VJ++)
TOCTitle: AbsolutePage, PageCount, and PageSize Properties Example (VJ++)
ms:assetid: 6cdf3880-1d77-5826-1d7b-7bf61a886d1b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249431(v=office.15)
ms:contentKeyID: 48545480
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 776129bcd3adfedbe25aa6df6a30a5c0d8339263
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478575"
---
# <a name="absolutepage-pagecount-and-pagesize-properties-example-vj"></a><span data-ttu-id="97dd2-102">AbsolutePage プロパティ、PageCount プロパティ、および PageSize プロパティの使用例 (VJ++)</span><span class="sxs-lookup"><span data-stu-id="97dd2-102">AbsolutePage, PageCount, and PageSize Properties Example (VJ++)</span></span>


<span data-ttu-id="97dd2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="97dd2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="97dd2-104">次の例では、[AbsolutePage](absolutepage-property-ado.md) プロパティ、[PageCount](pagecount-property-ado.md) プロパティ、および [PageSize](pagesize-property-ado.md) プロパティを使用して、***Employee*** テーブルから取得した名前と雇用年月日を一度に 5 レコードずつ表示します。</span><span class="sxs-lookup"><span data-stu-id="97dd2-104">This example uses the [AbsolutePage](absolutepage-property-ado.md), [PageCount](pagecount-property-ado.md), and [PageSize](pagesize-property-ado.md) properties to display names and hire dates from the ***Employees*** table, five records at a time.</span></span>

```java 
 
// BeginAbsolutePageJ 
// The WFC class includes the ADO objects. 
 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class AbsolutePageX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 AbsolutePageX(); 
 System.exit(0); 
 } 
 
 // AbsolutePageX function 
 
 static void AbsolutePageX() 
 { 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = new BufferedReader (new 
 InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 String strName; 
 String strFName; 
 String strLName; 
 String strHDate; 
 int intPage; 
 int intRecord; 
 
 try 
 { 
 rstEmployees = new Recordset(); 
 
 // Use client cursor to enable AbsolutePosition property. 
 rstEmployees.setCursorLocation( AdoEnums.CursorLocation.CLIENT); 
 
 // Open a recordset using client cursor for the Employees table. 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Display names and hire dates, five records at a time. 
 
 rstEmployees.setPageSize(5); 
 int intPageCount = rstEmployees.getPageCount(); 
 for ( intPage = 1; intPage <= intPageCount; intPage++) 
 { 
 strName = ""; 
 rstEmployees.setAbsolutePage(intPage); 
 for ( intRecord = 1; intRecord <= rstEmployees.getPageSize(); 
 intRecord++) 
 { 
 strFName = rstEmployees.getField("fname").getString(); 
 strLName = rstEmployees.getField("lname").getString(); 
 strHDate = rstEmployees.getField("hire_date").getString(); 
 
 strHDate = strHDate.substring(5,7) + "/" + 
 strHDate.substring(8,10) + 
 "/" + strHDate.substring(2,4); 
 
 strName = strName + "\n" + strFName + " " + strLName + 
 " " + strHDate; 
 rstEmployees.moveNext(); 
 if ( rstEmployees.getEOF()) 
 break; 
 } 
 System.out.println(strName); 
 // Get user input to display next records. 
 
 System.out.println("\n\nPress <Enter> key to Continue."); 
 line = in.readLine(); 
 } 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstEmployees.getActiveConnection()==null) 
 System.out.println("Exception: " + ae.getMessage()); 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
 } 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 //.PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndAbsolutePageJ 
```
