---
title: XML の保存形式
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9db8da66ab2c7bae1f28271ae37573f06ca222d7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477995"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="2d019-102">XML の保存形式</span><span class="sxs-lookup"><span data-stu-id="2d019-102">XML Persistence Format</span></span>

<span data-ttu-id="2d019-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d019-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="2d019-104">XML の保存形式</span><span class="sxs-lookup"><span data-stu-id="2d019-104">XML Persistence Format</span></span>

<span data-ttu-id="2d019-105">ADO では、保存する XML ストリームに UTF-8 エンコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d019-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="2d019-p101">ADO XML 形式は、スキーマ セクションと、その後に続くデータ セクションの 2 つのセクションに分けられます。Northwind データベースの Shippers テーブルの XML ファイルの例を次に示します。XML のさまざまな部分について、例に続いて解説しています。</span><span class="sxs-lookup"><span data-stu-id="2d019-p101">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="2d019-p102">このスキーマには、名前空間の宣言、スキーマ セクション、およびデータ セクションが示されています。スキーマ セクションに、行、ShipperID、CompanyName、および Phone の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d019-p102">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="2d019-p103">スキーマ定義は XML-Data の仕様に準拠し、すべて検証できます (ただし、検証は Internet Explorer 5 では行われません)。この仕様については、[W3C XML-Data ノート (英語)](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)で確認できます。XML-Data は、現在、 **Recordset** の保存をサポートしている唯一のスキーマ形式です。</span><span class="sxs-lookup"><span data-stu-id="2d019-p103">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="2d019-114">データ セクションには、荷主 (Shipper) に関する情報を含む 3 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="2d019-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="2d019-115">空の行セットのデータ セクションは空である可能性がありますが、`<rs:data>`タグが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d019-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="2d019-116">データがない可能性がありますを記述するタグの簡単なだけで`<rs:data>`です。</span><span class="sxs-lookup"><span data-stu-id="2d019-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="2d019-117">プレフィックスが "rs" のタグは、urn:schemas-microsoft-com:rowset によって定義された名前空間にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="2d019-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="2d019-118">このスキーマの完全な定義については、このドキュメントの付録を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d019-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="2d019-119">XML の保存形式</span><span class="sxs-lookup"><span data-stu-id="2d019-119">XML Persistence Format</span></span>

<span data-ttu-id="2d019-120">ADO では、保存する XML ストリームに UTF-8 エンコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d019-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="2d019-p105">ADO XML 形式は、スキーマ セクションと、その後に続くデータ セクションの 2 つのセクションに分けられます。Northwind データベースの Shippers テーブルの XML ファイルの例を次に示します。XML のさまざまな部分について、例に続いて解説しています。</span><span class="sxs-lookup"><span data-stu-id="2d019-p105">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="2d019-p106">このスキーマには、名前空間の宣言、スキーマ セクション、およびデータ セクションが示されています。スキーマ セクションに、行、ShipperID、CompanyName、および Phone の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d019-p106">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="2d019-p107">スキーマ定義は XML-Data の仕様に準拠し、すべて検証できます (ただし、検証は Internet Explorer 5 では行われません)。この仕様については、[W3C XML-Data ノート (英語)](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)で確認できます。XML-Data は、現在、 **Recordset** の保存をサポートしている唯一のスキーマ形式です。</span><span class="sxs-lookup"><span data-stu-id="2d019-p107">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="2d019-129">データ セクションには、荷主 (Shipper) に関する情報を含む 3 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="2d019-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="2d019-130">空の行セットのデータ セクションは空である可能性がありますが、`<rs:data>`タグが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d019-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="2d019-131">データがない可能性がありますを記述するタグの簡単なだけで`<rs:data>`です。</span><span class="sxs-lookup"><span data-stu-id="2d019-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="2d019-132">プレフィックスが "rs" のタグは、urn:schemas-microsoft-com:rowset によって定義された名前空間にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="2d019-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="2d019-133">このスキーマの完全な定義については、このドキュメントの付録を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d019-133">The full definition of this schema is defined in the appendix to this document.</span></span>
