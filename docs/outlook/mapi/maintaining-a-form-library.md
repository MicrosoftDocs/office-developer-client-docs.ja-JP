---
title: フォーム ライブラリを維持します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801292"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="58ebf-103">フォーム ライブラリを維持します。</span><span class="sxs-lookup"><span data-stu-id="58ebf-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="58ebf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58ebf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58ebf-105">フォーム ライブラリを保持するすべてのフォームに関する重要な情報: プロパティ、動詞、およびそのサーバーの実行可能ファイルです。</span><span class="sxs-lookup"><span data-stu-id="58ebf-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="58ebf-106">何人かのように、管理、インストール、またはフォームのサーバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="58ebf-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="58ebf-107">この機能をユーザーに提供する場合へのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="58ebf-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="58ebf-108">フォーム サーバーの構成ファイル、ファイルをします。CFG 拡張子を付けています。</span><span class="sxs-lookup"><span data-stu-id="58ebf-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="58ebf-109">フォーム ライブラリのコンテナーのオブジェクト、オブジェクトを実装する、 [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="58ebf-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="58ebf-110">構成ファイルまたはパス名を使用してアクセスするのにはなんらかの方法が便利です。</span><span class="sxs-lookup"><span data-stu-id="58ebf-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="58ebf-111">通常、クライアントのインストールと構成ファイルの場所をユーザーに確認するのにも使用できるフォームのサーバーを削除するためのダイアログ ボックスをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="58ebf-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="58ebf-112">フォーム ライブラリのコンテナーにアクセスするには、フォーム マネージャーの[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="58ebf-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="58ebf-113">開くには、フォーム ライブラリを指定する列挙値のパスと、必要に応じて、フォーム ライブラリを開くにフォーム マネージャーを使用する必要がありますオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="58ebf-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="58ebf-114">の[フォーム ライブラリのフォルダー](folder-form-libraries.md)を開いている場合を渡すなど、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)のポインター。</span><span class="sxs-lookup"><span data-stu-id="58ebf-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="58ebf-115">**IMAPIFormContainer**ポインターが返されると、 **OpenFormContainer**によっては、保守を実行する[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)または[IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)のいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="58ebf-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="58ebf-116">**InstallForm**フォームのサーバーをライブラリに追加します。**RemoveForm**は、フォームのサーバーをライブラリから削除します。</span><span class="sxs-lookup"><span data-stu-id="58ebf-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  
