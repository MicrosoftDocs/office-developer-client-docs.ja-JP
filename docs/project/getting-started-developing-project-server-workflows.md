---
title: Project Server ワークフローの開発を開始する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Project Server 2013 の管理プロセスを支援するワークフローを含む要求は、プロジェクトの提案とポートフォリオ分析を管理します。 このセクションには、Project Server のワークフローを作成する方法を説明する記事が含まれています。
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804540"
---
# <a name="getting-started-developing-project-server-workflows"></a>Project Server ワークフローの開発を開始する

Project Server 2013 の管理プロセスを支援するワークフローを含む要求は、プロジェクトの提案とポートフォリオ分析を管理します。 このセクションには、Project Server のワークフローを作成する方法を説明する記事が含まれています。
  
Project Server 2013 のワークフローでは、Windows ワークフロー Foundation (WF4) のバージョン 4 の上に構築された、SharePoint Server 2013 ワークフロー プラットフォームを使用します。 WF4 ベースのワークフローは宣言的なワークフローのデザイン ツールで、実行時に解釈されますが、XAML コードをワークフロー ステージ、アクション、条件、およびその他の要素を保存します。 宣言型ワークフローを作成するのには、SharePoint Designer 2013 または Visual Studio 2012 のいずれかを使用できます。 ワークフローでは、オンプレミスのソリューションのローカル サーバー上またはオンライン プロジェクトのソリューション用のリモート サーバーには、ワークフロー マネージャーのクライアント 1.0 の実行エンジンが必要です。
  
SharePoint Designer 2013 を使用すると、比較的単純な宣言型ワークフローを作成します。 複雑なワークフローは、ワークフロー テンプレートを再利用できるを開発し、Project Web App のワークフローをデバッグするのに Visual Studio 2012 を使用できます。 詳細については、[プロジェクトのワークフローを作成する Visual Studio 2012 を使用して](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)参照してください。
  
> [!IMPORTANT]
> 作成し、ワークフローをテストするには、実稼働インストールではなく、Project Server のテスト環境を使用します。 Project Server 2013 のプレリリース バージョン用に開発されたワークフローでは、リリース バージョンでは、テストする必要があるし、再作成して再展開する必要があります。 
  
## <a name="in-this-section"></a>このセクションの内容

[需要管理に Project Server ワークフローを作成します。](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>関連項目



[更新プログラムのユーザー設定フィールドを一括して、オンラインのプロジェクトのワークフローからプロジェクト サイトを作成](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[SharePoint Designer 2013 と Visio 2013 でワークフローの開発](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[SharePoint ワークフローの新機能](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[Visual Studio を使用した SharePoint 2013 ワークフローの開発](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[Visual Studio 2012 を使用してプロジェクトのワークフローを作成します。](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows ワークフロー Foundation](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[Windows ワークフロー Foundation (WF) .NET 4 での開発者の概要](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[Hitchhiker のガイド需要管理 (ホワイト ペーパー)](http://msdn.microsoft.com/en-us/library/ff973112.aspx)
