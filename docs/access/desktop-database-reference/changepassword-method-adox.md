---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476546"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="02be2-102">ChangePassword メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="02be2-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="02be2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="02be2-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="02be2-104">ユーザー アカウントのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="02be2-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="02be2-105">構文</span><span class="sxs-lookup"><span data-stu-id="02be2-105">Syntax</span></span>

<span data-ttu-id="02be2-106">*ユーザー*です。パスワードの変更を*OldPassword*、 *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="02be2-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="02be2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="02be2-107">Parameters</span></span>

  - <span data-ttu-id="02be2-108">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="02be2-108">*OldPassword*</span></span>

  - <span data-ttu-id="02be2-p101">ユーザーの現在のパスワードを示す文字列型 (**String**) の値を指定します。ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。</span><span class="sxs-lookup"><span data-stu-id="02be2-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="02be2-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="02be2-111">*NewPassword*</span></span>

  - <span data-ttu-id="02be2-112">新しいパスワードを表す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="02be2-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="02be2-113">解説</span><span class="sxs-lookup"><span data-stu-id="02be2-113">Remarks</span></span>

<span data-ttu-id="02be2-114">セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02be2-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="02be2-115">プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="02be2-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>
