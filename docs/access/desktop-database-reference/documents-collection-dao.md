---
title: Documents コレクション (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f6edd02c316fdff3f64b8a09c1504c46c9812a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293750"
---
# <a name="documents-collection-dao"></a>Documents コレクション (DAO)


**適用先:** Access 2013、Office 2013

**Documents** コレクションには、特定の種類のオブジェクトのすべての **Document** オブジェクトが含まれます。

## <a name="remarks"></a>注釈

各 **Container** オブジェクトには、 **Container** が指定する種類の組み込みオブジェクトのインスタンスを説明する **Document** オブジェクトを含む、 **Documents** コレクションがあります。

コレクション内の **Document** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

  - **Documents**(0)

  - **ドキュメント**("*name*")

  - ****\!ドキュメント\[*名*\]

## <a name="example"></a>例

この例では、Tables コンテナーの **Documents** コレクションを列挙し、次にコレクションの最初の **Document** オブジェクトの **Properties** コレクションを列挙します。

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

