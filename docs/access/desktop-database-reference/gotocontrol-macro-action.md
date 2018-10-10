---
title: GoToControl マクロ アクション
TOCTitle: GoToControl Macro Action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2617544bf04aa0b26ccbb9d7ce8d7329d42ed1e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477725"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="28b87-102">GoToControl マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="28b87-102">GoToControl Macro Action</span></span>


<span data-ttu-id="28b87-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="28b87-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="28b87-p101">" **GoToControl/コントロールの移動** " アクションを使用すると、開いているフォーム、フォームのデータシート、テーブルのデータシート、またはクエリのデータシートのカレント レコードの、指定したフィールドまたはコントロールにフォーカスを移動できます。このアクションにより、特定のフィールドまたはコントロールにフォーカスを移動することができます。このフィールドまたはコントロールは、比較を行ったり " **FindRecord/レコードの検索** " アクションを実行したりするときに使用します。また、このアクションを使用して、フォーム内を一定の条件に従って移動することもできます。たとえば、"健康保険" フォームの [既婚] コントロールに [いいえ] が設定されると、自動的に [配偶者またはパートナーの名前] コントロールをスキップして、次のコントロールにフォーカスを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="28b87-p101">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet. You can use this action when you want a particular field or control to have the focus. This field or control can then be used for comparisons or **FindRecord** actions. You can also use this action to navigate in a form according to certain conditions. For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="28b87-109">設定</span><span class="sxs-lookup"><span data-stu-id="28b87-109">Setting</span></span>


> [!NOTE]
> <P><span data-ttu-id="28b87-110">[!メモ] このアクションは、データ アクセス ページでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="28b87-110">This action is not available for use with data access pages.</span></span></P>



<span data-ttu-id="28b87-111">" **GoToControl/コントロールの移動** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="28b87-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28b87-112">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="28b87-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="28b87-113">説明</span><span class="sxs-lookup"><span data-stu-id="28b87-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28b87-114"><strong>コントロール名</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-p102">フォーカスの移動先のフィールドまたはコントロールの名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>コントロール名</strong>] ボックスにフィールドまたはコントロールの名前を入力します。この引数は省略できません。  
 
</span><span class="sxs-lookup"><span data-stu-id="28b87-p102">The name of the field or control where you want the focus. Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="28b87-118">"<STRONG>Control Name/コントロール名</STRONG>" 引数には、完全な識別子 (<フォーム>!<製品>![製品 ID] など) ではなく、フィールドまたはコントロールの名前のみを入力してください。</span><span class="sxs-lookup"><span data-stu-id="28b87-118">Enter only the name of the field or control in the <STRONG>Control Name</STRONG> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="28b87-119">注釈</span><span class="sxs-lookup"><span data-stu-id="28b87-119">Remarks</span></span>

<span data-ttu-id="28b87-120">" **GoToControl/コントロールの移動** " アクションで、非表示のフォームのコントロールにフォーカスを移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="28b87-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>


> [!TIP]
> <P><span data-ttu-id="28b87-p103">[!ヒント] " <STRONG>GoToControl/コントロールの移動</STRONG> " アクションを使用すると、サブフォームに移動することもできます (サブフォームはコントロールの一種です)。移動後に、サブフォームの特定のレコードに移動するには、" <STRONG>GoToControl/コントロールの移動</STRONG> " アクションを使用します。" <STRONG>GoToControl/コントロールの移動</STRONG> " アクションを使って、サブフォームの特定のコントロールに移動することもできます。それには、サブフォームに移動してから、サブフォームのコントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="28b87-p103">You can use the <STRONG>GoToControl</STRONG> action to move to a subform, which is a type of control. You can then use the <STRONG>GoToRecord</STRONG> action to move to a particular record in the subform. You can also move to a control on a subform by using the <STRONG>GoToControl</STRONG> action to move first to the subform and then to the control on the subform.</span></span></P>



<span data-ttu-id="28b87-p104">Visual Basic for Applications (VBA) モジュールで " **GoToControl/コントロールの移動** " アクションを実行するには、 **DoCmd** オブジェクトの **GoToControl** メソッドを使用します。 **SetFocus** メソッドを使用して、フォームまたはフォームまたはそのサブフォームのコントロール、開いているテーブル、クエリ、またはフォーム データシートのフィールドにフォーカスを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="28b87-p104">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object. You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="28b87-126">例</span><span class="sxs-lookup"><span data-stu-id="28b87-126">Examples</span></span>

<span data-ttu-id="28b87-127">**マクロによるコントロールの値の設定**</span><span class="sxs-lookup"><span data-stu-id="28b87-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="28b87-p105">次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="28b87-p105">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28b87-133">アクション</span><span class="sxs-lookup"><span data-stu-id="28b87-133">Action</span></span></p></th>
<th><p><span data-ttu-id="28b87-134">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="28b87-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="28b87-135">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="28b87-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28b87-136"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-137"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-138">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="28b87-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b87-139"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-140"><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: 製品の一覧<strong>を保存</strong>:<strong>なし</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-141">[製品リスト] フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28b87-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b87-142"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-143"><strong>フォーム名</strong>: 製品の<strong>表示</strong>: <strong>FormData モード</strong>: <strong>AddWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-144">[製品] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="28b87-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b87-145"><strong>値の代入</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-146"><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="28b87-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="28b87-147">[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</span><span class="sxs-lookup"><span data-stu-id="28b87-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b87-148"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-149"><strong>Control Name/コントロール名</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="28b87-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="28b87-150">[カテゴリ ID] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="28b87-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28b87-151">**マクロによるデータの入力検査**</span><span class="sxs-lookup"><span data-stu-id="28b87-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="28b87-p106">次の入力検査マクロでは、"仕入先" フォームで入力された郵便番号を確認します。このマクロでは、" **StopMacro/マクロの中止** "、" **MessageBox/メッセージボックス** "、" **CancelEvent/イベントのキャンセル** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。条件式では、フォームのレコードに入力された都道府県と郵便番号を確認します。都道府県に対して郵便番号が正しく入力されていない場合、マクロはメッセージ ボックスを表示して、レコードの保存を取り消します。その後、PostalCode コントロールに戻り、エラーを修正することができます。このマクロは "仕入先" フォームの " **BeforeUpdate/更新前処理** " プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="28b87-p106">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. The macro then returns you to the Postal Code control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28b87-158">条件</span><span class="sxs-lookup"><span data-stu-id="28b87-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="28b87-159">アクション</span><span class="sxs-lookup"><span data-stu-id="28b87-159">Action</span></span></p></th>
<th><p><span data-ttu-id="28b87-160">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="28b87-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="28b87-161">コメント</span><span class="sxs-lookup"><span data-stu-id="28b87-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28b87-162">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="28b87-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="28b87-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="28b87-164">[都道府県] の値が <strong>Null</strong> の場合は、郵便番号を検証できません。</span><span class="sxs-lookup"><span data-stu-id="28b87-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b87-165">[都道府県](&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) と Len ([郵便番号]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="28b87-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="28b87-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-167"><strong>メッセージ</strong>: 郵便番号のコードは 5 文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="28b87-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="28b87-168"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</span><span class="sxs-lookup"><span data-stu-id="28b87-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="28b87-169">郵便番号が 7 文字でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="28b87-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b87-170">...</span><span class="sxs-lookup"><span data-stu-id="28b87-170"></span></span></p></td>
<td><p><span data-ttu-id="28b87-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="28b87-172">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="28b87-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="28b87-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-174"><strong>コントロール名</strong>: [郵便番号]</span><span class="sxs-lookup"><span data-stu-id="28b87-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b87-175">[都道府県](&quot;オーストラリア&quot;、&quot;シンガポール&quot;) と Len ([郵便番号]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="28b87-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="28b87-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-177">"Message/メッセージ": 郵便番号は 7 文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="28b87-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="28b87-178"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</span><span class="sxs-lookup"><span data-stu-id="28b87-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="28b87-179">郵便番号が 7 文字でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="28b87-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b87-180">...</span><span class="sxs-lookup"><span data-stu-id="28b87-180"></span></span></p></td>
<td><p><span data-ttu-id="28b87-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="28b87-182">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="28b87-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="28b87-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-184"><strong>コントロール名</strong>: [郵便番号]</span><span class="sxs-lookup"><span data-stu-id="28b87-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b87-185">([都道府県] =&quot;カナダ&quot;)([郵便番号] が気に入らない&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="28b87-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="28b87-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="28b87-187"><strong>メッセージ</strong>: 郵便番号のコードが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="28b87-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="28b87-188">カナダのコードの例: H1J 1C 3<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号コードのエラー</span><span class="sxs-lookup"><span data-stu-id="28b87-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="28b87-p110">[都道府県] が広島県で、郵便番号の上 3 桁が 720 ～ 739 でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="28b87-p110">If the postal code is not correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b87-191">...</span><span class="sxs-lookup"><span data-stu-id="28b87-191"></span></span></p></td>
<td><p><span data-ttu-id="28b87-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="28b87-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="28b87-193">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="28b87-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>
