---
title: 完全な信頼が必要なフォーム テンプレートをプレビューおよびデバッグする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: 既定では、完全な信頼が必要なオブジェクト モデルのメンバーを起動するコードを含むマネージ コード プロジェクト (ユーザーのログイン ドメインに関する情報へのアクセスを必要とする LoginName プロパティなど) をデバッグまたはプレビューしようとすると、Microsoft InfoPath では次のようになります。
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411261"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>完全な信頼が必要なフォーム テンプレートをプレビューおよびデバッグする

既定では、完全な信頼が必要なオブジェクト モデルのメンバーを起動するコードを含むマネージ コード プロジェクト (ユーザーのログイン ドメインに関する情報へのアクセスを必要とする **LoginName** プロパティなど) をデバッグまたはプレビューしようとすると、Microsoft InfoPath では次のようになります。 
  
プレビュー時 :
  
"ハンドルされていない例外がフォームのコードで発生しました" に続いて "フォームのコードにエラーが含まれるため、この操作を完了できませんでした" というエラー メッセージが表示されます。
  
デバッグ時 :
  
コード エディターで、完全な信頼が必要なメンバーを呼び出しているコード行にフォーカスが移動し、" **SecurityException** はユーザー コードによってハンドルされませんでした。要求が失敗しました" というエラー メッセージが表示されます。 
  
デバッグ時またはプレビュー時に、フォーム テンプレートのビジネス ロジックがこのメンバーを呼び出すことを許可するには、前の手順に示したように、フォーム テンプレートのセキュリティ レベルを [ **完全信頼**] に設定する必要があります。 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>完全な信頼が必要なマネージ コード フォーム テンプレートを構成する

### <a name="set-your-forms-security-level-to-full-trust"></a>フォームのセキュリティ レベルを完全信頼に設定する

1. InfoPath のデザイン モードでフォーム テンプレートを開きます。
    
2. [ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。 
    
3. [ **カテゴリ**] ボックスの一覧の [ **セキュリティと信頼**] をクリックします。
    
4. [ **セキュリティ レベル**] の [ **自動的にセキュリティ レベルを設定する**] をオフにします。
    
5. **[完全信頼]** を選択してから、**[OK]** をクリックします。
    
この手順を実行すると、「[コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-infopath-form-templates-with-code.md)」の説明に従ってプロジェクトをデバッグできるようになります。
  
> [!NOTE]
> 完全信頼を必要とするマネージ コード フォーム テンプレートを正しく展開するには、フォーム テンプレートのデジタル署名、インストールと登録などの追加の手順が必要です。 デバッグ後のマネージ コード フォーム テンプレートの展開方法については、「[コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)

