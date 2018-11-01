---
title: SkipLine メソッド (ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c1ab54402dac8f6721c4c12f55f07979c4adff4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885452"
---
# <a name="skipline-method-ado"></a>SkipLine メソッド (ADO)


**適用されます**Access 2013、Office 2013。

テキスト ストリームを読み取っているときに、1 行全体をスキップします。

## <a name="syntax"></a>構文

*ストリーム*。SkipLine

## <a name="remarks"></a>解説

次の行区切り文字までのすべての文字 (行区切り文字を含む) がスキップされます。既定では、[LineSeparator](lineseparator-property-ado.md) は **adCRLF** です。 [EOS](eos-property-ado.md) を越えてスキップしようとした場合は、 **EOS** が現在の位置になります。

**SkipLine** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText** のストリーム) で使用します。

