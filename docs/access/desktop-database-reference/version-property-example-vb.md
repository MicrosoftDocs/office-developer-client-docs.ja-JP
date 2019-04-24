---
title: Version プロパティの使用例 (VB)
TOCTitle: Version property example (VB)
ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15)
ms:contentKeyID: 48548968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f76455c78c7c58b81a327d883cdd47821f42ac6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312076"
---
# <a name="version-property-example-vb"></a><span data-ttu-id="ed782-102">Version プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="ed782-102">Version property example (VB)</span></span>


<span data-ttu-id="ed782-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed782-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed782-p101">この例では、[Connection](version-property-ado.md) オブジェクトの [Version](connection-object-ado.md) プロパティを使用して、現在の ADO のバージョンを表示します。また、動的プロパティを使用して、次の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="ed782-p101">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version. It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="ed782-106">現在の DBMS の名前およびバージョン</span><span class="sxs-lookup"><span data-stu-id="ed782-106">the current DBMS name and version.</span></span>

  - <span data-ttu-id="ed782-107">OLE DB のバージョン</span><span class="sxs-lookup"><span data-stu-id="ed782-107">OLE DB version.</span></span>

  - <span data-ttu-id="ed782-108">プロバイダーの名前およびバージョン</span><span class="sxs-lookup"><span data-stu-id="ed782-108">provider name and version.</span></span>

  - <span data-ttu-id="ed782-109">ODBC のバージョン</span><span class="sxs-lookup"><span data-stu-id="ed782-109">ODBC version.</span></span>

  - <span data-ttu-id="ed782-110">ODBC ドライバーの名前およびバージョン</span><span class="sxs-lookup"><span data-stu-id="ed782-110">ODBC driver name and version.</span></span>

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

