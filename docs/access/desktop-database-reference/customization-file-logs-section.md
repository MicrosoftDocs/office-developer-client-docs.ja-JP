---
title: カスタマイズ ファイルの Logs セクション
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28132ee681d941eda3f7c1a9b072135a2d47b12b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882834"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="14c3d-102">カスタマイズ ファイルの Logs セクション</span><span class="sxs-lookup"><span data-stu-id="14c3d-102">Customization File Logs Section</span></span>

<span data-ttu-id="14c3d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="14c3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14c3d-104">**logs** セクションには、 **DataFactory** の操作中に発生したエラーを記録するファイル名を指定する、ログ ファイル エントリを含めます。</span><span class="sxs-lookup"><span data-stu-id="14c3d-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c3d-105">構文</span><span class="sxs-lookup"><span data-stu-id="14c3d-105">Syntax</span></span>

<span data-ttu-id="14c3d-106">ログ ファイル エントリの形式は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="14c3d-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14c3d-107">引数</span><span class="sxs-lookup"><span data-stu-id="14c3d-107">Part</span></span></p></th>
<th><p><span data-ttu-id="14c3d-108">説明</span><span class="sxs-lookup"><span data-stu-id="14c3d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14c3d-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="14c3d-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="14c3d-110">これがログ ファイル エントリであることを示すリテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="14c3d-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14c3d-111"><em>Filename</em></span><span class="sxs-lookup"><span data-stu-id="14c3d-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="14c3d-p101">完全パスとファイル名。通常のファイル名は、<strong>c:\msdfmap.log</strong> です。</span><span class="sxs-lookup"><span data-stu-id="14c3d-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14c3d-114">ログ ファイルには、各エラーのユーザー名、HRESULT、および発生日時が含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c3d-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

