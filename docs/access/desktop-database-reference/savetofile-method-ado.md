---
title: SaveToFile メソッド (ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0bd915a4eb6405b7d5ddd4bfe42eb4a98f68b89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476818"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="d1e6b-102">SaveToFile メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="d1e6b-102">SaveToFile Method (ADO)</span></span>


<span data-ttu-id="d1e6b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1e6b-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="d1e6b-104">[Stream](stream-object-ado.md) のバイナリの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e6b-105">構文</span><span class="sxs-lookup"><span data-stu-id="d1e6b-105">Syntax</span></span>

<span data-ttu-id="d1e6b-106">*ストリーム*。SaveToFile*ファイル名*、 *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="d1e6b-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="d1e6b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1e6b-107">Parameters</span></span>

  - <span data-ttu-id="d1e6b-108">*Filename*</span><span class="sxs-lookup"><span data-stu-id="d1e6b-108">*FileName*</span></span>

  - <span data-ttu-id="d1e6b-p101">**Stream** の内容の保存先であるファイルの完全修飾名を含む文字列型 ( **String** ) の値を指定します。有効なローカルの場所、または UNC 値を介してアクセスできる場所への保存が可能です。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>

  - <span data-ttu-id="d1e6b-111">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="d1e6b-111">*SaveOptions*</span></span>

  - <span data-ttu-id="d1e6b-p102">保存するファイルがまだ存在しない場合に、 [SaveToFile](saveoptionsenum.md) メソッドで新しいファイルを作成するかどうかを **SaveOptionsEnum** 値で指定します。既定値は **adSaveCreateNotExists** です。これらのオプションでは、指定したファイルが存在しない場合にエラーが発生するように指定できます。また、 **SaveToFile** メソッドで既存ファイルの現在の内容を上書きするように指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d1e6b-116">[!メモ] <STRONG>adSaveCreateOverwrite</STRONG> を設定して既存ファイルを上書きすると、 <STRONG>SaveToFile</STRONG> メソッドによって、元の既存ファイルから、新しい <A href="eos-property-ado.md">EOS</A> 以降のバイトがすべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-116">If you overwrite an existing file (when <STRONG>adSaveCreateOverwrite</STRONG> is set), <STRONG>SaveToFile</STRONG> truncates any bytes from the original existing file that follow the new <A href="eos-property-ado.md">EOS</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="d1e6b-117">解説</span><span class="sxs-lookup"><span data-stu-id="d1e6b-117">Remarks</span></span>

<span data-ttu-id="d1e6b-p103">**SaveToFile** メソッドを使用すると、 **Stream** オブジェクトの内容をローカル ファイルにコピーできます。 **Stream** オブジェクトの内容やプロパティは変更されません。 **SaveToFile** メソッドを呼び出す前に、 **Stream** オブジェクトが開かれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="d1e6b-p104">このメソッドでは、 **Stream** オブジェクトと基になるソースの関連付けは変更されません。 **Stream** オブジェクトは、開かれたときのソースである元の URL または **Record** に関連付けられたままになります。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="d1e6b-123">**SaveToFile** メソッドの操作後、ストリーム内の現在の位置 ([Position](position-property-ado.md)) は、ストリームの先頭 (0) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d1e6b-123">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>
