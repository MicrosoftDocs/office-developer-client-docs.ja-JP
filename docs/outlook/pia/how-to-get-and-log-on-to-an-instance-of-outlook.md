---
title: Outlook のインスタンスを取得し、サインインする
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-and-log-on-to-an-instance-of-outlook?redirectedfrom=MSDN
ms:contentKeyID: 55119926
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bae79531e7d2be39610194e0b59477fcee28c15
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773702"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Outlook のインスタンスを取得し、サインインする

このトピックでは、ローカル コンピューターで Microsoft Outlook が実行されている場合には Outlook のアクティブ インスタンスを表す [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?redirectedfrom=MSDN&view=outlook-pia) オブジェクトを取得し、そうでない場合には Outlook の新しいインスタンスを作成し、既定のプロファイルにサインインし、Outlook のそのインスタンスを返す方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、Helmut Obertanner 氏が提供したものです。 Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。 

次のコード例には、Sample クラスの GetApplicationObject メソッドが含まれています。このメソッドは、Outlook アドイン プロジェクトの一部として実装されています。 それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?redirectedfrom=MSDN&view=outlook-pia) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。

GetApplicationObject メソッドは、.NET Framework クラス ライブラリのクラスを使用して、ローカル コンピューターで実行中の Outlook プロセスを確認および取得します。 まず、 [System.Diagnostics](https://docs.microsoft.com/dotnet/api/system.diagnostics.process.getprocessesbyname?redirectedfrom=MSDN&view=netframework-4.8#overloads) 名前空間内の [Process](https://docs.microsoft.com/dotnet/api/system.diagnostics.process?redirectedfrom=MSDN&view=netframework-4.8) クラスの [GetProcessesByName](https://docs.microsoft.com/dotnet/api/system.diagnostics?redirectedfrom=MSDN&view=netframework-4.8) メソッドを使用して、ローカル コンピューター上のプロセス名 "OUTLOOK" のプロセス コンポーネントの配列を取得します。 配列に少なくとも 1 つの Outlook プロセスが含まれているかどうかを確認するために、GetApplicationObject では Microsoft 統合言語クエリ (LINQ) を使用しています。 [System.Linq](https://msdn.microsoft.com/library/bb345746) 名前空間内の [Enumerable](https://msdn.microsoft.com/library/bb336768) クラスには、 \> ジェネリック インターフェイスを実装している各種メソッドがあり、 [Count](https://msdn.microsoft.com/library/9eekhta0) メソッドもその 1 つです。 [Array](https://msdn.microsoft.com/library/czz5hkty) クラスは **IEnumerable(T)** インターフェイスを実装しているため、**GetProcessesByName** から返された配列に **Count** メソッドを利用することで、実行中の Outlook プロセスが存在するかどうかを確認できます。 存在している場合、GetApplicationObject は [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) 名前空間の [Marshal](https://msdn.microsoft.com/library/asx0thw2) クラスに含まれる [GetActiveObject](https://msdn.microsoft.com/library/xt620x09) メソッドを使用して、その Outlook のインスタンスを取得し、そのオブジェクトを Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトにキャストします。

Outlook がローカル コンピューターで実行中ではない場合、GetApplicationObject では、Outlook の新しいインスタンスを作成し、[NameSpace](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.namespace?redirectedfrom=MSDN&view=outlook-pia) オブジェクトの [Logon(Object, Object, Object, Object)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._namespace.logon?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__NameSpace_Logon_System_Object_System_Object_System_Object_System_Object_) メソッドを使用して既定のプロファイルにサインインし、Outlook のその新しいインスタンスを返します。

次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>関連項目

- [セッション](sessions.md)

