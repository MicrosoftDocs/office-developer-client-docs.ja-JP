---
title: DCOM で DLL を実行できるようにする
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 26c83c9770ce7372338a054090025c67c32a9c36
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476776"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="788f9-102">DCOM で DLL を実行できるようにする</span><span class="sxs-lookup"><span data-stu-id="788f9-102">Enabling a DLL to Run on DCOM</span></span>


<span data-ttu-id="788f9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="788f9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="788f9-104">次の手順では、ビジネス オブジェクトのダイナミック リンク ライブラリが、コンポーネント サービスを介して DCOM と Microsoft® インターネット インフォメーション サービス (HTTP) の両方を使用できるようにする方法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="788f9-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft® Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="788f9-p101">コンポーネント サービス MMC スナップインに新しい空のパッケージを作成します。 コンポーネント サービス MMC スナップインを使ってパッケージを作成し、このパッケージに DLL を追加します。これにより、DCOM を介して .dll にアクセスできるようになりますが、IIS を介したアクセスはできなくなります (.dll のレジストリを確認すると、 **Inproc** キーが空になっているのがわかります。後で説明するようにアクティブ化属性を設定すると、 **Inproc** キーに値が追加されます)。</span><span class="sxs-lookup"><span data-stu-id="788f9-p101">Create a new empty package in the Component Services MMC snap-in. You will use the Component Services MMC snap-in to create a package and add the DLL into this package. This makes the .dll accessible through DCOM, but it removes the accessibility through IIS. (If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="788f9-p102">パッケージにビジネス オブジェクトをインストールします。 または[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトをパッケージにインポートします。</span><span class="sxs-lookup"><span data-stu-id="788f9-p102">Install a business object into the package. -or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="788f9-111">**作成者のプロセスで**[ライブラリ アプリケーションには、パッケージのアクティブ化属性を設定します。</span><span class="sxs-lookup"><span data-stu-id="788f9-111">Set the Activation attribute for the package to **In the creator's process** (Library application).</span></span> <span data-ttu-id="788f9-112">.Dll ファイルを同じコンピューターで DCOM と IIS を介してアクセスできるようにするためには、コンポーネント サービス MMC スナップインで、コンポーネントのアクティブ化属性を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="788f9-112">To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in.</span></span> <span data-ttu-id="788f9-113">**作成者のプロセス内**に属性を設定した後に、コンポーネント サービスへのポインターがアクティブ化する、**インプロセス**サーバーのレジストリ キーが追加されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="788f9-113">After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>
