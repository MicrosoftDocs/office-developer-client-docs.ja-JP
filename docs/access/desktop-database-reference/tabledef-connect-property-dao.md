---
title: TableDef.Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eaedb53c8cb70746229e3f311ba5925e3b30ddef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478050"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="f7e4e-102">TableDef.Connect プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7e4e-102">TableDef.Connect Property (DAO)</span></span>


<span data-ttu-id="f7e4e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7e4e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7e4e-p101">リンク テーブルに関する情報を提供する値を設定します。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e4e-106">構文</span><span class="sxs-lookup"><span data-stu-id="f7e4e-106">Syntax</span></span>

<span data-ttu-id="f7e4e-107">*式*です。接続</span><span class="sxs-lookup"><span data-stu-id="f7e4e-107">*expression* .Connect</span></span>

<span data-ttu-id="f7e4e-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e4e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="f7e4e-109">Remarks</span></span>

<span data-ttu-id="f7e4e-p102">**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="f7e4e-112">リンク テーブルを表す **TableDef** オブジェクトの場合、 **Connect** プロパティの設定値は、1 つまたは 2 つの部分 (データベースの種類の識別子とそのデータベースへのパス) で構成され、それぞれの末尾にセミコロンが付けられています。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="f7e4e-p103">次の表のパスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="f7e4e-115">次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7e4e-116">データベースの種類</span><span class="sxs-lookup"><span data-stu-id="f7e4e-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="f7e4e-117">識別子</span><span class="sxs-lookup"><span data-stu-id="f7e4e-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="f7e4e-118">例</span><span class="sxs-lookup"><span data-stu-id="f7e4e-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-119">Microsoft Access データベース</span><span class="sxs-lookup"><span data-stu-id="f7e4e-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-120">[database];</span><span class="sxs-lookup"><span data-stu-id="f7e4e-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-121"><ドライブ>:\<パス>\<ファイル名>.wk1</span><span class="sxs-lookup"><span data-stu-id="f7e4e-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="f7e4e-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-124"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="f7e4e-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-127"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="f7e4e-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-130"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="f7e4e-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-133"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="f7e4e-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-136"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="f7e4e-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-139"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="f7e4e-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-142"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="f7e4e-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="f7e4e-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-145"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="f7e4e-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-146">Microsoft Excel 5.0 または Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="f7e4e-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-148"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="f7e4e-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="f7e4e-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-151"><ドライブ>:\<パス>\<ファイル名.xls></span><span class="sxs-lookup"><span data-stu-id="f7e4e-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-152">Lotus 1-2-3 WKS および WK1</span><span class="sxs-lookup"><span data-stu-id="f7e4e-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-154"><ドライブ>:\<パス>\<ファイル名.wk1></span><span class="sxs-lookup"><span data-stu-id="f7e4e-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="f7e4e-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-157"><ドライブ>:\<パス>\<ファイル名.wk3></span><span class="sxs-lookup"><span data-stu-id="f7e4e-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="f7e4e-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-160"><ドライブ>:\<パス>\<ファイル名.wk4></span><span class="sxs-lookup"><span data-stu-id="f7e4e-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-161">HTML インポート</span><span class="sxs-lookup"><span data-stu-id="f7e4e-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-163"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="f7e4e-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-164">HTML エクスポート</span><span class="sxs-lookup"><span data-stu-id="f7e4e-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-166"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="f7e4e-167">Text</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-168">Text;</span><span class="sxs-lookup"><span data-stu-id="f7e4e-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-169"><ドライブ>:\<パス></span><span class="sxs-lookup"><span data-stu-id="f7e4e-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e4e-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="f7e4e-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-171">ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</span><span class="sxs-lookup"><span data-stu-id="f7e4e-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-172">なし</span><span class="sxs-lookup"><span data-stu-id="f7e4e-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e4e-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="f7e4e-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-174">Exchange 4.0 です。MAPILEVEL = folderpath です。[TABLETYPE = {0 | 1}]。[プロファイル = プロファイル][PWD = パスワード][データベース = データベース]</span><span class="sxs-lookup"><span data-stu-id="f7e4e-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="f7e4e-175"><ドライブ>:\<パス>\<ファイル名></span><span class="sxs-lookup"><span data-stu-id="f7e4e-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f7e4e-176">必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="f7e4e-177">Microsoft Exchange のデータを完全に解決済みのフォルダーのパス (たとえば、「メールボックス-Pat SmithIAlpha/今日」) に必要な MAPILEVEL キーを設定してください。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="f7e4e-178">パスでは、テーブルとして表示するフォルダーの名前は含まれません**CreateTable**メソッドの引数名としてそのフォルダーの名前を指定する必要があります代わりに。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="f7e4e-179">TABLETYPE キーは、フォルダー (既定値) またはアドレス帳を開くには、「1」を開く「0」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="f7e4e-180">プロファイルにプロファイル キーの既定値が使用されています。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="f7e4e-181">Micorosoft Access データベースのベース テーブルの場合、 **Connect** プロパティ設定は長さ 0 の文字列 ("") です。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="f7e4e-182">[!メモ] <STRONG>ReturnsRecords</STRONG> プロパティを設定する前に、 <STRONG>Connect</STRONG> プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-182">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="f7e4e-183">アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e4e-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>

