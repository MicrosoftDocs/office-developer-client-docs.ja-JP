---
title: 作成、取得、更新、およびプロジェクトのサーバーの JavaScript を使用してプロジェクトを削除します。
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: 現在の ProjectContext のインスタンスを取得します。取得し、サーバー上の発行済みプロジェクトのコレクションを反復処理します。作成、取得、チェック アウト、および、プロジェクトのサーバーの JavaScript オブジェクト モデルを使用してプロジェクトを削除します。プロジェクトのプロパティを変更してください。
ms.openlocfilehash: 966c1298d210cb608001e4ce2b390611a75bdb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804545"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>作成、取得、更新、およびプロジェクトのサーバーの JavaScript を使用してプロジェクトを削除します。

この資料のシナリオは、現在の**ProjectContext**のインスタンスを取得する方法を表示します。取得し、サーバー上の発行済みプロジェクトのコレクションを反復処理します。作成、取得、チェック アウト、および、プロジェクトのサーバーの JavaScript オブジェクト モデルを使用してプロジェクトを削除します。プロジェクトのプロパティを変更してください。 
  
> [!NOTE]
> これらのシナリオは SharePoint アプリケーション ページのマークアップでカスタム コードを定義しますが、ページの Visual Studio 2012 を作成する分離コード ファイルを使用しません。 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>JavaScript オブジェクト モデルでは、プロジェクトを Project Server 2013 を使用するための前提条件

この記事で説明するシナリオを実行するには、次の製品をインストールおよび構成する必要があります。
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Office Developer Tools for Visual Studio 2012
    
SharePoint Server 2013 に拡張機能を配置し、プロジェクトへの投稿のアクセス許可も必要です。
  
> [!NOTE]
> 次の手順では、Project Server 2013 を実行しているコンピューター上で開発することを前提としています。 
  
## <a name="create-the-visual-studio-solution"></a>Visual Studio ソリューションを作成する
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

次の手順では、SharePoint のプロジェクトとアプリケーション ページに含まれている Visual Studio 2012 のソリューションを作成します。 ページには、プロジェクトを操作するためのロジックが含まれています。
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Visual Studio で SharePoint を作成するには

1. Project Server 2013 を実行しているコンピューターに管理者として Visual Studio 2012 を実行します。
    
2. メニュー バーで、[ **ファイル**]、[ **新規作成**]、[ **プロジェクト**] の順に選択します。
    
3. [ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。 
    
4. **Office、SharePoint**テンプレートのカテゴリでは、 **SharePoint ソリューション**を選択し、 **SharePoint 2013 のプロジェクト**テンプレートを選択し、します。 
    
5. ProjectsJSOM、プロジェクトの名前し、 **[OK** ] ボタンをクリックします。 
    
6. [ **SharePoint カスタマイズ ウィザード**] ダイアログ ボックスで、[ **ファーム ソリューションとして配置する**] を選択して、[ **完了**] をクリックします。 
    
7. Project Web App インスタンスの URL と一致する**ProjectsJSOM**プロジェクトの**サイトの URL**プロパティの値を編集する (たとえば、 `http://ServerName/PWA`)。
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Visual Studio でアプリケーション ページを作成するには

1. **ソリューション エクスプ ローラー**で、 **ProjectsJSOM**プロジェクトのショートカット メニューを開くし、SharePoint を追加し、「レイアウト」フォルダーがマップされています。 
    
2. **レイアウト**フォルダーに**ProjectsJSOM**フォルダーのショートカット メニューを開くし、ProjectsList.aspx をという名前の新しい SharePoint アプリケーション ページを追加します。
    
3. **ProjectsList.aspx**ページのショートカット メニューを開き、**スタートアップ アイテムとして設定**] を選択します。
    
4. **ProjectsList.aspx**ページのマークアップでは、次のよう、"Main" **asp: コンテンツ**のタグ内のユーザー インターフェイス コントロールを定義します。 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > これらのコントロールは、すべてのシナリオでは使用できません。 たとえば、シナリオを作成するプロジェクト」では、**テキスト領域**と**ボタン**のコントロールは使用しません。 
  
5. **またがる**終了後にタグ付け、次のように**SharePoint:ScriptLink**タグや**SharePoint:FormDigest**タグでは、**スクリプト**タグを追加します。 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   **SharePoint:ScriptLink**タグは、Project Server 2013 の JavaScript オブジェクト モデルを定義する PS.js ファイルを参照します。 **SharePoint:FormDigest**タグは、サーバーのコンテンツを更新する操作が必要なときに、セキュリティ検証のメッセージ ダイジェストを生成します。 
    
6. プレースホルダー コメントを、次のいずれかの手順のコードで置換します。
    
   - [JavaScript オブジェクト モデルを使用して Project Server 2013 のプロジェクトを作成します。](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [JavaScript オブジェクト モデルを使用して Project Server 2013 のプロジェクトを更新します。](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [JavaScript オブジェクト モデルを使用して Project Server 2013 のプロジェクトを削除します。](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. メニュー バーの [アプリケーション] ページをテストするのには、**デバッグ**、**デバッグの開始**を選択します。 Web.config ファイルを変更するメッセージが表示されたら、 **[ok]** を選択します。
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>JavaScript オブジェクト モデルを使用して Project Server 2013 のプロジェクトを作成します。
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

このセクションの手順では、JavaScript オブジェクト モデルを使用してプロジェクトを作成します。 プロシージャには、次の大まかな手順が含まれています。
  
1. **ProjectContext**の現在のインスタンスを取得します。 
    
2. プロジェクトの初期のプロパティを指定するのには、 **ProjectCreationInformation**オブジェクトを作成します。 必要な**名前**のプロパティを指定するには、 **ProjectCreationInformation.set_name**関数を使用します。 
    
3. **ProjectContext.get_projects**関数を使用して、サーバーから発行されたプロジェクトを取得します。 **Get_projects**関数は、 **ProjectCollection**オブジェクトを返します。 
    
4. **ProjectCollection.add**関数を使用して、 **ProjectCreationInformation**オブジェクトを渡すことによって、コレクションに新しいプロジェクトを追加します。 
    
5. **ProjectCollection.update**関数および**ProjectContext.waitForQueueAsync**関数を使用してコレクションを更新します。 **更新**関数は、 **waitForQueueAsync**に渡された**QueueJob**オブジェクトを返します。 この呼び出しは、プロジェクトを発行します。
    
**Visual Studio でアプリケーション ページを作成する**手順で追加した**スクリプト**タグの間で次のコードを貼り付けます。 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>JavaScript オブジェクト モデルを使用して Project Server 2013 のプロジェクトを更新します。
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

このセクションの手順では、JavaScript オブジェクト モデルを使用して、プロジェクトの**開始日**のプロパティを更新します。 プロシージャには、次の大まかな手順が含まれています。 
  
1. **ProjectContext**の現在のインスタンスを取得します。 
    
2. **ProjectContext.get_projects**関数を使用して、サーバーから発行されたプロジェクトを取得します。 **Get_projects**関数は、 **ProjectCollection**オブジェクトを返します。 
    
3. **ProjectContext.load**関数および**ProjectContext.executeQueryAsync**関数を使用してサーバーに要求を実行します。 
    
4. **PublishedProject**オブジェクトを取得するには、 **ProjectContext.getById**関数を使用します。 
    
5. **Project.checkOut**関数を使用する対象となるプロジェクトをチェック_アウトします。 **チェック アウト**機能は、発行されたプロジェクトの下書きバージョンを返します。 
    
6. プロジェクトの開始日を変更するには、 **DraftProject.set_startDate**関数を使用します。 
    
7. **DraftProject.publish**関数および**ProjectContext.waitForQueueAsync**関数を使用してプロジェクトを発行します。 **発行**機能では、 **waitForQueueAsync**に渡すと、 **QueueJob**オブジェクトを返します。
    
**Visual Studio でアプリケーション ページを作成する**手順で追加した**スクリプト**タグの間で次のコードを貼り付けます。 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>JavaScript オブジェクト モデルを使用して Project Server 2013 のプロジェクトを削除します。
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

このセクションの手順では、JavaScript オブジェクト モデルを使用してプロジェクトを削除します。 プロシージャには、次の大まかな手順が含まれています。
  
1. **ProjectContext**の現在のインスタンスを取得します。 
    
2. **ProjectContext.get_projects**関数を使用して、サーバーから発行されたプロジェクトを取得します。 **Get_projects**関数は、 **ProjectCollection**オブジェクトを返します。 
    
3. **ProjectContext.load**関数および**ProjectContext.executeQueryAsync**関数を使用してサーバーに要求を実行します。 
    
4. **PublishedProject**オブジェクトを取得するには、 **ProjectCollection.getById**関数を使用します。 
    
5. **ProjectCollection.remove**関数に渡すことによって、プロジェクトを削除します。 
    
6. **ProjectCollection.update**関数および**ProjectContext.waitForQueueAsync**関数を使用してコレクションを更新します。 **更新**関数は、 **waitForQueueAsync**に渡された**QueueJob**オブジェクトを返します。
    
**Visual Studio でアプリケーション ページを作成する**手順で追加した**スクリプト**タグの間で次のコードを貼り付けます。 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>関連項目

- [プロジェクトのプログラミング タスク](project-programming-tasks.md)
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
    
