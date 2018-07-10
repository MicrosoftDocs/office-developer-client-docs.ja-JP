---
title: OneNote の開発者用リファレンス
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: このリファレンスには、概念の概要および OneNote 2013 デスクトップ クライアント アプリケーションのためのソリューションを開発するときにプログラムの参照が含まれています。
ms.openlocfilehash: 8af3f0b8623f0b457250ea11f185a25cadec7386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799291"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="1c411-103">OneNote の開発者用リファレンス</span><span class="sxs-lookup"><span data-stu-id="1c411-103">OneNote developer reference</span></span>

<span data-ttu-id="1c411-104">このリファレンスには、概念の概要および OneNote 2013 デスクトップ クライアント アプリケーションのためのソリューションを開発するときにプログラムの参照が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c411-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="1c411-105">すべての追加機能が含まれています、OneNote の 2013年のアプリケーション プログラミング インターフェイス (API) に変更され、OneNote の一部のタスクを実行する方法を表示する C# のコード サンプルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="1c411-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="1c411-106">OneNote 2013 API では、プログラムからアクセスし、OneNote のコンテンツを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="1c411-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="1c411-107">ユーザーは、OneNote ウィンドウのビューに変更をすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1c411-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="1c411-108">このドキュメントには次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1c411-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="1c411-109">[ウィンドウ インターフェイス](window-interfaces-onenote.md): OneNote ウィンドウの集合を列挙し、特定のウィンドウのプロパティを変更するユーザーを有効にする**ウィンドウ**と**ウィンドウ**インターフェイスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1c411-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="1c411-110">[クイック ファイリング ダイアログ ボックス インタ フェース](quick-filing-dialog-box-interfaces-onenote.md): プログラムを使用して OneNote 2013 で**クイック ファイリング**ダイアログ ボックスをカスタマイズするのに使用できるインターフェイスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1c411-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="1c411-111">[アプリケーション ・ インタ フェース](application-interface-onenote.md): メソッド、プロパティ、およびヘルプの取得、操作、および OneNote 2013 の情報とコンテンツを更新するイベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1c411-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="1c411-112">[列挙体](enumerations-onenote-developer-reference.md): OneNote 2013 オブジェクト モデルの列挙体について説明します。</span><span class="sxs-lookup"><span data-stu-id="1c411-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="1c411-113">[エラー コード](error-codes-onenote.md): OneNote 2013 オブジェクト モデル内のエラー コードを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="1c411-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1c411-p102">このドキュメントに記載する API は、未接続のシナリオにおける OneNote Win32 デスクトップ クライアント ソリューションのみを対象としています。接続のシナリオの場合は、推奨する OneNote サービス API を使用してください。詳細については、[dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="1c411-p102">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios. For connected scenarios, use the recommended OneNote service APIs. To learn more, visit [dev.onenote.com](http://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1c411-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c411-117">See also</span></span>

- [<span data-ttu-id="1c411-118">OneNote の開発者</span><span class="sxs-lookup"><span data-stu-id="1c411-118">OneNote for developers</span></span>](http://go.microsoft.com/fwlink/?LinkID=390615)
    
- <span data-ttu-id="1c411-119">[GitHub のサンプル](https://github.com/OneNoteDev/)(OneNote サービス Api)</span><span class="sxs-lookup"><span data-stu-id="1c411-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span> 
    
- [<span data-ttu-id="1c411-120">マイクロソフト製品のアクセシビリティ機能</span><span class="sxs-lookup"><span data-stu-id="1c411-120">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)
    
- [<span data-ttu-id="1c411-121">�h�L�������g�̂��߂̕\�L�K��</span><span class="sxs-lookup"><span data-stu-id="1c411-121">Document Conventions</span></span>](http://msdn.microsoft.com/ja-jp/office/aa905365.aspx)
    
- [<span data-ttu-id="1c411-122">OneNote の開発者リファレンスの著作権情報</span><span class="sxs-lookup"><span data-stu-id="1c411-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/ja-jp/library/office/jj680116.aspx)
    
- <span data-ttu-id="1c411-123">[Microsoft �v���C�o�V�[�Ɋւ��鐺��](http://privacy.microsoft.com/en-us/default.mspx)</span><span class="sxs-lookup"><span data-stu-id="1c411-123">[Microsoft Online Privacy Notice](http://privacy.microsoft.com/en-us/default.mspx)</span></span>
    
