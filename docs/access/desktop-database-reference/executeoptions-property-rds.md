---
title: ExecuteOptions プロパティ (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 641e7942f5336f230d396db7e06b9d0601645cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476678"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="68464-102">ExecuteOptions プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="68464-102">ExecuteOptions Property (RDS)</span></span>


<span data-ttu-id="68464-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="68464-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="68464-104">非同期実行が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="68464-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="68464-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="68464-105">Settings and Return Values</span></span>

<span data-ttu-id="68464-106">次のいずれかの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="68464-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68464-107">定数</span><span class="sxs-lookup"><span data-stu-id="68464-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="68464-108">説明</span><span class="sxs-lookup"><span data-stu-id="68464-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68464-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="68464-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="68464-110">次回の <a href="recordset-object-ado.md">Recordset</a> の更新を同期的に実行します。</span><span class="sxs-lookup"><span data-stu-id="68464-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68464-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="68464-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="68464-p101">既定値です。次回の <strong>Recordset</strong> の更新を非同期的に実行します。</span><span class="sxs-lookup"><span data-stu-id="68464-p101">Default. Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="68464-p102">[!メモ] これらの定数を使うクライアント側の各実行可能ファイルは、その定数を宣言する必要があります。C:\Program Files\Common Files\System\MSADC フォルダーの Adcvbs.inc ファイルから、定数の宣言を切り取って貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="68464-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="68464-116">解説</span><span class="sxs-lookup"><span data-stu-id="68464-116">Remarks</span></span>

<span data-ttu-id="68464-117">**ExecuteOptions** が **adcExecAsync** に設定されている場合、 **RDS.DataControl** オブジェクトの [Recordset](datacontrol-object-rds.md) における次の **Refresh** 呼び出しは非同期的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="68464-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="68464-118">[RDS.DataControl](reset-method-rds.md) オブジェクトの [Recordset](refresh-method-rds.md) に変更を行う可能性のある別の非同期操作の実行中に [Reset](submitchanges-method-rds.md)、[Refresh](cancelupdate-method-ado.md)、[SubmitChanges](recordset-sourcerecordset-properties-rds.md)、[CancelUpdate](datacontrol-object-rds.md)、または **Recordset** を呼び出そうとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="68464-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="68464-119">非同期操作中にエラーが発生した場合、**RDS.DataControl** オブジェクトの [ReadyState](readystate-property-rds.md) 値が **adcReadyStateLoaded** から **adcReadyStateComplete** に変更され、**Recordset** プロパティ値は *Nothing* のまま維持されます。</span><span class="sxs-lookup"><span data-stu-id="68464-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>
