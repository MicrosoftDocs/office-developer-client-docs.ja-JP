---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800434"
---
# <a name="iid"></a><span data-ttu-id="adca7-103">IID</span><span class="sxs-lookup"><span data-stu-id="adca7-103">IID</span></span>

  
  
<span data-ttu-id="adca7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="adca7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="adca7-105">MAPI インターフェイスの識別子を記述するために使用する[GUID](guid.md)構造体について説明します。</span><span class="sxs-lookup"><span data-stu-id="adca7-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="adca7-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="adca7-106">Members</span></span>

<span data-ttu-id="adca7-107">**GUID**構造体を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adca7-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="adca7-108">備考</span><span class="sxs-lookup"><span data-stu-id="adca7-108">Remarks</span></span>

<span data-ttu-id="adca7-109">MAPI インターフェイスを一意に識別して、特定のインターフェイスをオブジェクトに関連付けるには、 **IID**の構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="adca7-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="adca7-110">などの場合、クライアントへの呼び出し[IMAPISession::OpenEntry](imapisession-openentry.md)フォルダーを開き、クライアント パラメーターを設定_lpInterface_ **IID**を指すように、 [IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを表します。</span><span class="sxs-lookup"><span data-stu-id="adca7-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="adca7-111">MAPI では、IID_IMAPIFolder に**IMAPIFolderIID**を定義します。</span><span class="sxs-lookup"><span data-stu-id="adca7-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="adca7-112">**IID**の構造は、OLE インターフェイスを一意に識別するのにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="adca7-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="adca7-113">MAPI インターフェイスの特定の**IID**の構造体のすべては、Mapiguid.h ヘッダー ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="adca7-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adca7-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="adca7-114">See also</span></span>



[<span data-ttu-id="adca7-115">GUID</span><span class="sxs-lookup"><span data-stu-id="adca7-115">GUID</span></span>](guid.md)


[<span data-ttu-id="adca7-116">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="adca7-116">MAPI Structures</span></span>](mapi-structures.md)
