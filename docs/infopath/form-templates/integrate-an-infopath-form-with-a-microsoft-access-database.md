---
title: InfoPath フォームと Microsoft Access データベースの統合
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ec9a9c0-b348-4a31-b377-e95db2f92455
description: Microsoft InfoPath では、Microsoft Access 2010 のデータベースをフォームのプライマリ データ ソースとして、あるいはフォームまたはコントロールのセカンダリ データ ソースとして使用できます。ここでは、Access 2010 データベースをデータ ソースとして使用する方法について説明します。
ms.openlocfilehash: 30aea15a5e9a8d19f64b3f089b71e859cff93e0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799166"
---
# <a name="integrate-an-infopath-form-with-a-microsoft-access-database"></a>InfoPath フォームと Microsoft Access データベースの統合

Microsoft InfoPath では、Microsoft Access 2010 のデータベースをフォームのプライマリ データ ソースとして、あるいはフォームまたはコントロールのセカンダリ データ ソースとして使用できます。ここでは、Access 2010 データベースをデータ ソースとして使用する方法について説明します。
  
## <a name="using-a-microsoft-access-database-as-a-data-source"></a>データ ソースとして Microsoft Access データベースを使用する

### <a name="setting-up-a-microsoft-access-database-as-a-forms-primary-data-source"></a>Microsoft Access データベースをフォームのプライマリ データ ソースとして設定する

InfoPath では **データ接続ウィザード**を使用してデータ接続を確立します。このウィザードを開くには、Microsoft Office Backstage の [ **新規作成**] タブにある [ **フォーム テンプレート (高度)**] セクションで [ **データベース**] を選択し、[ **Design This Form**] をクリックします。
  
[ **データベースの選択**] をクリックすると、既存のデータ ソースを選択するか、特定のデータベース ファイルに直接接続できます。
  
データベースを選択した後は、ウィザードに従って、フォームのデータ ソースとして使用するテーブルをそのデータベースから選択する必要があります。テーブルを追加していくと、テーブル相互のリレーションシップが確立され、[ **データ ソース構造**] ボックスの一覧に、各テーブルとそれらの階層関係が表示されます。[ **テーブルの列を表示する**] チェック ボックスをオンにすると、各テーブルのフィールドの名前が [データ ソース構造] ボックスの一覧に表示されます。各フィールド名の横にあるチェック ボックスを使用して、該当するフィールドをウィザードで作成する SQL ステートメントに含めるかどうかを指定できます。 
  
> [!NOTE]
> [!メモ] 各テーブルの主キー フィールドは必ず選択されます。選択を解除することはできません。 
  
**データ接続ウィザード**を使用してテーブル、リレーションシップ、およびフィールドを指定したら、[ **SQL の編集**] をクリックして、フォームのデータ ソースの作成に使用される SQL ステートメントを表示できます。[ **SQL の編集**] ダイアログ ボックスの [ **SQL ステートメントのテスト**] をクリックすると、指定した情報からデータ ソースを作成できるかどうかを確認できます。また、[ **SQL の編集**] ダイアログ ボックスでは、表示されている SQL ステートメントを編集して、より複雑なクエリを作成することもできます。 
  
> [!NOTE]
> [!メモ] InfoPath で使用される SQL ステートメントは、データ シェイプ クエリです。データ シェイプ クエリでは、クエリ内の複数の論理エンティティ間に階層関係を指定できます。SQL JOIN ステートメントを使用できますが、このステートメントを使用するとフォームの送信が無効になるため、お勧めできません。データ シェイプ クエリの詳細については、Microsoft Developer Network (MSDN) のドキュメントを参照してください。 
  
**データ接続ウィザード**の最後のページには、データ ソースの名前とファイルの場所、プライマリ親テーブルの名前、使用されるテーブルの数、送信状態など、データ ソースに関する概要が表示されます。送信状態によって、生成される SQL ステートメントでデータをデータ ソースに正しく送信できるかどうかがわかります。 
  
### <a name="setting-up-a-microsoft-access-database-as-a-secondary-data-source"></a>Microsoft Access データベースをセカンダリ データ ソースとして設定する

セカンダリ データ ソースは、リスト ボックスやドロップダウン リスト ボックスのエントリを提供する目的で使用できます。また、セカンダリ データ ソースのデータをフォームに追加するコードを記述することもできます。フォームでセカンダリ データ ソースを使用するには、フォームのデザイン時に [ **データ**] タブの [ **データ接続**] をクリックします。 
  
**データ接続ウィザード**を起動すると、フォームに使用するデータを受信するか、またはフォームのデータを送信するかを選択するように求められます。[ **データの受信**] を選択して [ **次へ**] をクリックします。データベースからセカンダリ データ ソースを作成するには、[ **データベース (Microsoft SQL Server または Microsoft Office Access のみ)**] を選択します。ウィザードの次のページで、[ **データベースの選択**] をクリックし、既存のデータ ソースを選択するか、特定のデータベース ファイルに直接接続します。 
  
データベースを選択した後は、ウィザードに従って、フォームのデータ ソースとして使用するテーブルまたはクエリをそのデータベースから選択する必要があります。最初にテーブルまたはクエリを 1 つ選択する必要がありますが、必要に応じて後から追加のテーブルを選択できます。テーブルまたはクエリを選択したら、使用するフィールドを [ **データ ソース構造**] ボックスの一覧で選択できます。既定では、テーブルのフィールドがすべて選択されていますが、フォームに不要なフィールドは選択を解除できます。また、テーブルから返されるレコードの並べ替え方法や、複数のレコードを扱えるかどうかも設定できます。設定する場合は、[ **テーブルの変更**] をクリックし、[ **並べ替え順序**] ダイアログ ボックスで並べ替えの条件を最大 3 つ選択します。設定が終了したら、[ **完了**] をクリックします。
  
> [!NOTE]
> [!メモ] 各テーブルの主キー フィールドは必ず選択されます。選択を解除することはできません。 
  
InfoPath では、複数のテーブルまたはクエリから同時にデータを取得することもできます。複数のテーブルまたはクエリからデータを取得するときは、 **データ接続ウィザード**で最初に選択したテーブルやクエリと関係のあるすべてのテーブルまたはクエリの間でリレーションシップを確立できる必要があります。たとえば、ノースウィンド データベースの得意先テーブルからデータを取得した場合は、受注テーブルを追加して、その顧客のすべての受注に関するデータを取得したり、受注明細テーブルを追加して、個々の注文の詳細を取得したりできます。
  
データ ソースにテーブルを追加するには、子テーブルの追加先のテーブルを [ **データ ソース構造**] ボックスの一覧で選択し、[ **テーブルの追加**] をクリックします。追加するテーブルまたはクエリを選択し、[ **次へ**] をクリックします。使用するリレーションシップ (複数可) を選択するように求められます。2 つのテーブルに同じ名前のフィールドがある場合は、それらのフィールドがリレーションシップとして自動的に追加されます。同じ名前のフィールドがない場合や、カスタムのリレーションシップを使用する場合は、[ **リレーションシップの追加**] をクリックして、親テーブルのどのフィールドを子テーブルのフィールドに対応付けるかを指定します。[ **リレーションシップの編集**] ダイアログボックスの [ **リレーションシップの削除**] をクリックして、既存のリレーションシップを削除することもできます。 
  
リレーションシップの設定が終了したら、[ **完了**] をクリックします。メイン テーブルの場合と同様に、子テーブルからどのフィールドを返すかを指定できます。ただし、[ **テーブルの変更**] ボタンを使用して、レコードを返す順序を編集することはできません。 
  
テーブル、リレーションシップ、およびフィールドを指定したら、[ **SQL の編集**] をクリックして、フォームのデータ ソースの作成に使用される SQL ステートメントを表示できます。[ **SQL の編集**] ダイアログ ボックスの [ **SQL ステートメントのテスト**] をクリックすると、指定した情報からデータ ソースを作成できるかどうかを確認できます。また、[ **SQL の編集**] ダイアログ ボックスでは、表示されている SQL ステートメントを編集して、より複雑なクエリを作成することもできます。 
  
> [!NOTE]
> [!メモ] InfoPath で使用される SQL ステートメントは、データ シェイプ クエリです。データ シェイプ クエリでは、クエリ内の複数の論理エンティティ間に階層関係を指定できます。SQL JOIN ステートメントを使用できますが、このステートメントを使用するとフォームの送信が無効になるため、お勧めできません。データ シェイプ クエリの詳細については、Microsoft Developer Network (MSDN) のドキュメントを参照してください。 
  
## <a name="enabling-form-submission"></a>フォームの送信を有効にする

InfoPath では、Access データベースからデータを受信するだけでなく、新しいデータや変更されたデータをデータベースに送り返すことができます。[ **ホーム**] タブまたは Microsoft Office Backstage の [ **送信**] コマンドを使用して、変更内容をデータベースに送信すると、ActiveX データ オブジェクト (ADO) を使用してデータベースのレコードが更新されます。フォームの送信は、次のすべての条件が満たされる場合に有効になります。 
  
- フォームのクエリで使用されるすべての列の基本列が存在する必要があります。
    
- テーブルの 1 つの列がクエリ全体で複数回使用されないようにします。
    
- フォームのクエリで使用される SELECT 句内のすべてのテーブルで、主キー、一意制約 (UNIQUE)、または一意なインデックスを利用できる必要があります。
    
- 1 つのテーブルをフォームのクエリに複数回含めることはできません。
    
- 親テーブルと子テーブルのリレーションシップには、親テーブルの主キー列をすべて含める必要があります。
    
- フォームのクエリに使用される SELECT 句内のすべての列について、ベース テーブルが 1 つであることが必要です。
    
フォームの変更内容を InfoPath でデータベースに送信できない状況がいくつかあります。たとえば、テーブルではなくクエリからデータを取得するフォームを作成した場合や、InfoPath で使用される SQL ステートメントをカスタマイズして JOIN ステートメントを挿入した場合は、InfoPath から変更内容を送信できません。親テーブルとの間に多対一のリレーションシップを持つテーブルをフォームに追加した場合も、変更内容の送信はできません。InfoPath からデータベースに変更内容を送信できない場合は、 **データ接続ウィザード**の最後のページの [ **送信状況**] フィールドに、その理由が表示されます。 
  
