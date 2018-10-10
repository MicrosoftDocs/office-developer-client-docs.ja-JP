---
title: DataControl エラー コード
TOCTitle: DataControl Error Codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef139e545fafedd67ca788ebfdc8a8ae86c659e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477105"
---
# <a name="datacontrol-error-codes"></a><span data-ttu-id="e3437-102">DataControl エラー コード</span><span class="sxs-lookup"><span data-stu-id="e3437-102">DataControl Error Codes</span></span>


<span data-ttu-id="e3437-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3437-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e3437-p101">次の表は、[RDS.DataControl](datacontrol-object-rds.md) オブジェクトのエラー コードの一覧です。下位 2 バイトを正の 10 進数に変換した値、エラー コード全体を負の 10 進数に変換した値、および 16 進数値を示します。</span><span class="sxs-lookup"><span data-stu-id="e3437-p101">The following table lists the [RDS.DataControl](datacontrol-object-rds.md) object error codes. The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3437-106">RDS.DataControl エラー コード</span><span class="sxs-lookup"><span data-stu-id="e3437-106">RDS.DataControl error codes</span></span></p></th>
<th><p><span data-ttu-id="e3437-107">番号</span><span class="sxs-lookup"><span data-stu-id="e3437-107">Number</span></span></p></th>
<th><p><span data-ttu-id="e3437-108">説明</span><span class="sxs-lookup"><span data-stu-id="e3437-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3437-109"><strong>IDS_AsyncPending</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-109"><strong>IDS_AsyncPending</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-110">4107</span><span class="sxs-lookup"><span data-stu-id="e3437-110">4107</span></span><br />
<span data-ttu-id="e3437-111">-2146824175</span><span class="sxs-lookup"><span data-stu-id="e3437-111">-2146824175</span></span><br />
<span data-ttu-id="e3437-112">0x800A1011</span><span class="sxs-lookup"><span data-stu-id="e3437-112">0x800A1011</span></span></p></td>
<td><p><span data-ttu-id="e3437-113">非同期操作の保留中に、操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="e3437-113">Operation cannot be performed while async operation is pending.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-114"><strong>IDS_BadInlineTablegram</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-114"><strong>IDS_BadInlineTablegram</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-115">4105</span><span class="sxs-lookup"><span data-stu-id="e3437-115">4105</span></span><br />
<span data-ttu-id="e3437-116">-2146824183</span><span class="sxs-lookup"><span data-stu-id="e3437-116">-2146824183</span></span><br />
<span data-ttu-id="e3437-117">0x800A1009</span><span class="sxs-lookup"><span data-stu-id="e3437-117">0x800A1009</span></span></p></td>
<td><p><span data-ttu-id="e3437-118">インライン テーブルグラムが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="e3437-118">Bad inline tablegram.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-119"><strong>IDS_CantConnect</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-119"><strong>IDS_CantConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-120">4099</span><span class="sxs-lookup"><span data-stu-id="e3437-120">4099</span></span><br />
<span data-ttu-id="e3437-121">-2146824189</span><span class="sxs-lookup"><span data-stu-id="e3437-121">-2146824189</span></span><br />
<span data-ttu-id="e3437-122">0x800A1003</span><span class="sxs-lookup"><span data-stu-id="e3437-122">0x800A1003</span></span></p></td>
<td><p><span data-ttu-id="e3437-123">サーバーに接続できません。</span><span class="sxs-lookup"><span data-stu-id="e3437-123">Cannot connect to server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-124"><strong>IDS_CantCreateObject</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-124"><strong>IDS_CantCreateObject</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-125">4100</span><span class="sxs-lookup"><span data-stu-id="e3437-125">4100</span></span><br />
<span data-ttu-id="e3437-126">-2146824188</span><span class="sxs-lookup"><span data-stu-id="e3437-126">-2146824188</span></span><br />
<span data-ttu-id="e3437-127">0x800A1004</span><span class="sxs-lookup"><span data-stu-id="e3437-127">0x800A1004</span></span></p></td>
<td><p><span data-ttu-id="e3437-128">ビジネス オブジェクトは作成できません。</span><span class="sxs-lookup"><span data-stu-id="e3437-128">Business object cannot be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-129"><strong>IDS_CantFindDataspace</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-129"><strong>IDS_CantFindDataspace</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-130">4102</span><span class="sxs-lookup"><span data-stu-id="e3437-130">4102</span></span><br />
<span data-ttu-id="e3437-131">-2146824186</span><span class="sxs-lookup"><span data-stu-id="e3437-131">-2146824186</span></span><br />
<span data-ttu-id="e3437-132">0x800A1006</span><span class="sxs-lookup"><span data-stu-id="e3437-132">0x800A1006</span></span></p></td>
<td><p><span data-ttu-id="e3437-133">Dataspace プロパティは無効です。</span><span class="sxs-lookup"><span data-stu-id="e3437-133">Dataspace property is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-134"><strong>IDS_CantInvokeMethod</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-134"><strong>IDS_CantInvokeMethod</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-135">4101</span><span class="sxs-lookup"><span data-stu-id="e3437-135">4101</span></span><br />
<span data-ttu-id="e3437-136">-2146824187</span><span class="sxs-lookup"><span data-stu-id="e3437-136">-2146824187</span></span><br />
<span data-ttu-id="e3437-137">0x800A1005</span><span class="sxs-lookup"><span data-stu-id="e3437-137">0x800A1005</span></span></p></td>
<td><p><span data-ttu-id="e3437-138">ビジネス オブジェクトのメソッドを呼び出せません。</span><span class="sxs-lookup"><span data-stu-id="e3437-138">Method cannot be invoked on business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-139"><strong>IDS_CrossDomainWarning</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-139"><strong>IDS_CrossDomainWarning</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-140">4112</span><span class="sxs-lookup"><span data-stu-id="e3437-140">4112</span></span><br />
<span data-ttu-id="e3437-141">-2146824170</span><span class="sxs-lookup"><span data-stu-id="e3437-141">-2146824170</span></span><br />
<span data-ttu-id="e3437-142">0x800A1016</span><span class="sxs-lookup"><span data-stu-id="e3437-142">0x800A1016</span></span></p></td>
<td><p><span data-ttu-id="e3437-143">このページでは、別のドメイン上のデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e3437-143">This page accesses data on another domain.</span></span> <span data-ttu-id="e3437-144">これを許可しますか。</span><span class="sxs-lookup"><span data-stu-id="e3437-144">Do you want to allow this?</span></span> <span data-ttu-id="e3437-145">Internet Explorer でこのメッセージを回避するには、[<strong>セキュリティ</strong>] タブ、[<strong>インターネット オプション</strong>] ダイアログ ボックスの [信頼済みサイト ゾーンにセキュリティで保護された web サイトを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e3437-145">To avoid this message in Internet Explorer, you can add a secure website to your Trusted Sites zone on the <strong>Security</strong> tab of the <strong>Internet Options</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-146"><strong>IDS_InvalidADCClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-146"><strong>IDS_InvalidADCClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-147">4106</span><span class="sxs-lookup"><span data-stu-id="e3437-147">4106</span></span><br />
<span data-ttu-id="e3437-148">-2146824176</span><span class="sxs-lookup"><span data-stu-id="e3437-148">-2146824176</span></span><br />
<span data-ttu-id="e3437-149">0x800A1010</span><span class="sxs-lookup"><span data-stu-id="e3437-149">0x800A1010</span></span></p></td>
<td><p><span data-ttu-id="e3437-150">無効な RDS クライアント バージョン-クライアントは、サーバーよりも新しいです。</span><span class="sxs-lookup"><span data-stu-id="e3437-150">Invalid RDS Client Version — Client is newer than server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-151"><strong>IDS_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-151"><strong>IDS_INVALIDARG</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-152">サイズは 5376</span><span class="sxs-lookup"><span data-stu-id="e3437-152">5376</span></span><br />
<span data-ttu-id="e3437-153">-2147019520</span><span class="sxs-lookup"><span data-stu-id="e3437-153">-2147019520</span></span><br />
<span data-ttu-id="e3437-154">0x80071500</span><span class="sxs-lookup"><span data-stu-id="e3437-154">0x80071500</span></span></p></td>
<td><p><span data-ttu-id="e3437-155">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="e3437-155">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-156"><strong>IDS_InvalidBindings</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-156"><strong>IDS_InvalidBindings</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-157">4097</span><span class="sxs-lookup"><span data-stu-id="e3437-157">4097</span></span><br />
<span data-ttu-id="e3437-158">-2146824191</span><span class="sxs-lookup"><span data-stu-id="e3437-158">-2146824191</span></span><br />
<span data-ttu-id="e3437-159">0x800A1001</span><span class="sxs-lookup"><span data-stu-id="e3437-159">0x800A1001</span></span></p></td>
<td><p><span data-ttu-id="e3437-160">プロパティのバインド エラーです。</span><span class="sxs-lookup"><span data-stu-id="e3437-160">Error in bindings property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-161"><strong>IDS_InvalidParam</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-161"><strong>IDS_InvalidParam</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-162">4110</span><span class="sxs-lookup"><span data-stu-id="e3437-162">4110</span></span><br />
<span data-ttu-id="e3437-163">-2146824172</span><span class="sxs-lookup"><span data-stu-id="e3437-163">-2146824172</span></span><br />
<span data-ttu-id="e3437-164">0x800A1014</span><span class="sxs-lookup"><span data-stu-id="e3437-164">0x800A1014</span></span></p></td>
<td><p><span data-ttu-id="e3437-165">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="e3437-165">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-166"><strong>IDS_NOINTERFACE</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-166"><strong>IDS_NOINTERFACE</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-167">5377</span><span class="sxs-lookup"><span data-stu-id="e3437-167">5377</span></span><br />
<span data-ttu-id="e3437-168">-2147019519</span><span class="sxs-lookup"><span data-stu-id="e3437-168">-2147019519</span></span><br />
<span data-ttu-id="e3437-169">0x80071501</span><span class="sxs-lookup"><span data-stu-id="e3437-169">0x80071501</span></span></p></td>
<td><p><span data-ttu-id="e3437-170">そのインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e3437-170">No such interface is supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-171"><strong>IDS_NotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-171"><strong>IDS_NotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-172">4111</span><span class="sxs-lookup"><span data-stu-id="e3437-172">4111</span></span><br />
<span data-ttu-id="e3437-173">-2146824171</span><span class="sxs-lookup"><span data-stu-id="e3437-173">-2146824171</span></span><br />
<span data-ttu-id="e3437-174">0x800A1015</span><span class="sxs-lookup"><span data-stu-id="e3437-174">0x800A1015</span></span></p></td>
<td><p><span data-ttu-id="e3437-175">イベント ハンドラーの処理中に要求を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="e3437-175">Request cannot be executed while the event handler is still processing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-176"><strong>IDS_ObjectNotSafe</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-176"><strong>IDS_ObjectNotSafe</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-177">4103</span><span class="sxs-lookup"><span data-stu-id="e3437-177">4103</span></span><br />
<span data-ttu-id="e3437-178">-2146824185</span><span class="sxs-lookup"><span data-stu-id="e3437-178">-2146824185</span></span><br />
<span data-ttu-id="e3437-179">0x800A1007</span><span class="sxs-lookup"><span data-stu-id="e3437-179">0x800A1007</span></span></p></td>
<td><p><span data-ttu-id="e3437-180">このコンピューターの安全性の設定により、ビジネス オブジェクトの作成が禁止されています。</span><span class="sxs-lookup"><span data-stu-id="e3437-180">Safety settings on this computer prohibit creation of business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-181"><strong>IDS_RecordsetNotOpen</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-181"><strong>IDS_RecordsetNotOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-182">4109</span><span class="sxs-lookup"><span data-stu-id="e3437-182">4109</span></span><br />
<span data-ttu-id="e3437-183">-2146824173</span><span class="sxs-lookup"><span data-stu-id="e3437-183">-2146824173</span></span><br />
<span data-ttu-id="e3437-184">0x800A1013</span><span class="sxs-lookup"><span data-stu-id="e3437-184">0x800A1013</span></span></p></td>
<td><p><span data-ttu-id="e3437-185">レコードセット (<strong>Recordset</strong>) が開かれていません。</span><span class="sxs-lookup"><span data-stu-id="e3437-185"><strong>Recordset</strong> is not open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-186"><strong>IDS_ResetInvalidField</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-186"><strong>IDS_ResetInvalidField</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-187">4108</span><span class="sxs-lookup"><span data-stu-id="e3437-187">4108</span></span><br />
<span data-ttu-id="e3437-188">-2146824174</span><span class="sxs-lookup"><span data-stu-id="e3437-188">-2146824174</span></span><br />
<span data-ttu-id="e3437-189">0x800A1012</span><span class="sxs-lookup"><span data-stu-id="e3437-189">0x800A1012</span></span></p></td>
<td><p><span data-ttu-id="e3437-190"><strong>SortColumn</strong> または <strong>FilterColumn</strong> に指定された列は存在しません。</span><span class="sxs-lookup"><span data-stu-id="e3437-190">Column specified in <strong>SortColumn</strong> or <strong>FilterColumn</strong> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-191"><strong>IDS_RowsetNotUpdateable</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-191"><strong>IDS_RowsetNotUpdateable</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-192">4104</span><span class="sxs-lookup"><span data-stu-id="e3437-192">4104</span></span><br />
<span data-ttu-id="e3437-193">-2146824184</span><span class="sxs-lookup"><span data-stu-id="e3437-193">-2146824184</span></span><br />
<span data-ttu-id="e3437-194">0x800A1008</span><span class="sxs-lookup"><span data-stu-id="e3437-194">0x800A1008</span></span></p></td>
<td><p><span data-ttu-id="e3437-195">行セットは更新できません。</span><span class="sxs-lookup"><span data-stu-id="e3437-195">Rowset not updateable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-196"><strong>IDS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-196"><strong>IDS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-197">4351</span><span class="sxs-lookup"><span data-stu-id="e3437-197">4351</span></span><br />
<span data-ttu-id="e3437-198">-2146823937</span><span class="sxs-lookup"><span data-stu-id="e3437-198">-2146823937</span></span><br />
<span data-ttu-id="e3437-199">0x800A10FF</span><span class="sxs-lookup"><span data-stu-id="e3437-199">0x800A10FF</span></span></p></td>
<td><p><span data-ttu-id="e3437-200">予期しないエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="e3437-200">Unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3437-201"><strong>IDS_UpdatesFailed</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-201"><strong>IDS_UpdatesFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-202">4098</span><span class="sxs-lookup"><span data-stu-id="e3437-202">4098</span></span><br />
<span data-ttu-id="e3437-203">-2146824190</span><span class="sxs-lookup"><span data-stu-id="e3437-203">-2146824190</span></span><br />
<span data-ttu-id="e3437-204">0x800A1002</span><span class="sxs-lookup"><span data-stu-id="e3437-204">0x800A1002</span></span></p></td>
<td><p><span data-ttu-id="e3437-205">データベースを更新できません。</span><span class="sxs-lookup"><span data-stu-id="e3437-205">Unable to update database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3437-206"><strong>IDS_URLMONNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="e3437-206"><strong>IDS_URLMONNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="e3437-207">4119</span><span class="sxs-lookup"><span data-stu-id="e3437-207">4119</span></span><br />
<span data-ttu-id="e3437-208">-2146824169</span><span class="sxs-lookup"><span data-stu-id="e3437-208">-2146824169</span></span><br />
<span data-ttu-id="e3437-209">0x800A1017</span><span class="sxs-lookup"><span data-stu-id="e3437-209">0x800A1017</span></span></p></td>
<td><p><span data-ttu-id="e3437-210">DataControl <strong>URL</strong> プロパティにはシステム ファイル Urlmon.dll が必要ですが、ファイルが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="e3437-210">DataControl <strong>URL</strong> property requires the system file Urlmon.dll, which cannot be found.</span></span></p></td>
</tr>
</tbody>
</table>

