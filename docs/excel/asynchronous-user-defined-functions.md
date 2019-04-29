---
title: 非同期のユーザー定義関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7fdf3bd09914981865c911fd65a78d044ad582f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412311"
---
# <a name="asynchronous-user-defined-functions"></a><span data-ttu-id="1cc1a-103">非同期のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="1cc1a-103">Asynchronous user-defined functions</span></span>

<span data-ttu-id="1cc1a-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1cc1a-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1cc1a-p101">Microsoft Excel 2013 can call user-defined functions asynchronously. Calling functions asynchronously can improve performance by allowing several calculations to run at the same time. When you run user-defined functions on a compute cluster, calling functions asynchronously enables several computers to be used to complete the calculations.</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p101">Microsoft Excel 2013 can call user-defined functions asynchronously. Calling functions asynchronously can improve performance by allowing several calculations to run at the same time. When you run user-defined functions on a compute cluster, calling functions asynchronously enables several computers to be used to complete the calculations.</span></span>
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a><span data-ttu-id="1cc1a-108">非同期のユーザー定義関数を使用する場合</span><span class="sxs-lookup"><span data-stu-id="1cc1a-108">When to use asynchronous user-defined functions</span></span>

<span data-ttu-id="1cc1a-p102">Some user-defined functions must wait for external resources. While they wait, the Excel calculation thread is blocked. In Excel 2013, user-defined functions can run asynchronously. This frees the calculation thread to run other calculations while the user-defined function waits.</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p102">Some user-defined functions must wait for external resources. While they wait, the Excel calculation thread is blocked. In Excel 2013, user-defined functions can run asynchronously. This frees the calculation thread to run other calculations while the user-defined function waits.</span></span>
  
<span data-ttu-id="1cc1a-p103">In Excel 2007, programmers could run multiple user-defined functions at the same time by increasing the number of threads used in multiple-thread recalculations. This method has drawbacks primarily because the number of threads is a setting scoped to an application and cannot be controlled at the level of a single function or an add-in.</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p103">In Excel 2007, programmers could run multiple user-defined functions at the same time by increasing the number of threads used in multiple-thread recalculations. This method has drawbacks primarily because the number of threads is a setting scoped to an application and cannot be controlled at the level of a single function or an add-in.</span></span>
  
<span data-ttu-id="1cc1a-p104">�֐����O�����\�[�X��҂K�v������ꍇ�A�v���O���}�[�͔񓯊��̃��[�U�[��\`�֐��̌Ăяo����g�p����K�v������܂��B���Ƃ��΁A�C���^�[�l�b�g��� SOAP �v���𑗐M����֐��́A�l�b�g���[�N�ŗv�����z�M����A�����[�g �T�[�o�[�ŗv�����������A�l�b�g���[�N�Ō��ʂ��Ԃ����̂�҂K�v������܂��B���̏ꍇ�A�d�v�ȃR���s���[�e�B���O�͔��������AExcel �ő��̌v�Z��p�����čs�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p104">Programmers should use asynchronous user-defined function calls when the function must wait for external resources. For example, a function that sends a SOAP request over the Internet must wait for the network to deliver the request, the remote server to complete the request, and the network to return the result. In this case, there is no significant computing occurring and Excel can continue with other calculations.</span></span>
  
<span data-ttu-id="1cc1a-p105">�֐����v�Z�N���X�^�[�ɗv���𑗐M���Ă���ꍇ�A�v���O���}�[�͔񓯊��̃��[�U�[��\`�֐���g�p���邱�Ƃ�ł��܂��B���̏ꍇ�A�l�b�g���[�N�̒x����҂����łȂ��A�N���X�^�[�͌X�̌Ăяo����ʁX�̃T�[�o�[�Ŏ��s�ł��܂��B�X�̌Ăяo������������܂ő҂��Ȃ����Ƃɂ��A�Ăяo����d�����邱�Ƃ��ł��邽�߃p�t�H�[�}���X�����P���܂��B�ꍇ�ɂ���ẮA�啝�ɉ��P���܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p105">Programmers can also use asynchronous user-defined functions when a function is sending requests to a compute cluster. In this case, there is not only network latency to wait for, but the cluster can execute separate calls on separate servers. By not waiting for each call to finish, the calls can be overlapped to improve performance. In some cases this improvement is significant.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1cc1a-122">[!����] ���[�U�[��\`�֐��́A�񓯊��ƃN���X�^�[ �Z�[�t�̗����Ƃ��ēo�^���邱�Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-122">User-defined functions cannot be registered as both asynchronous and cluster safe.</span></span> 
  
## <a name="writing-an-asynchronous-user-defined-function"></a><span data-ttu-id="1cc1a-123">非同期のユーザー定義関数を作成する</span><span class="sxs-lookup"><span data-stu-id="1cc1a-123">Writing an asynchronous user-defined function</span></span>

<span data-ttu-id="1cc1a-p106">Asynchronous user-defined functions must keep track of a handle and use that handle when informing Excel that the function call is finished. An asynchronous user-defined function is split into two pieces. The first piece is the standard UDF entry point, which will launch a second, separate asynchronous operation. Callbacks into Excel should be made during the UDF entry point. The first launching portion of the function will then return control of its calculation thread to Excel, which will continue calculation. When the second asynchronous operation is complete, it must call back into Excel and provide Excel with its result.</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p106">Asynchronous user-defined functions must keep track of a handle and use that handle when informing Excel that the function call is finished. An asynchronous user-defined function is split into two pieces. The first piece is the standard UDF entry point, which will launch a second, separate asynchronous operation. Callbacks into Excel should be made during the UDF entry point. The first launching portion of the function will then return control of its calculation thread to Excel, which will continue calculation. When the second asynchronous operation is complete, it must call back into Excel and provide Excel with its result.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1cc1a-130">[!����] �񓯊������ŕK�v�� UDF �ɓn���ꂽ���ׂĂ̈����ɂ��ẮAUDF �G���g�� �|�C���g���Ԃ��ꂽ�Ƃ��� Excel �������̈����������邽�߁A�֐��̏ڍׂ��R�s�[����Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-130">Any arguments passed into the UDF that are needed by the asynchronous portion the function must be deep copied because Excel frees these arguments when the UDF entry point returns.</span></span> 
  
<span data-ttu-id="1cc1a-p107">Excel �ł́A�񓯊��� UDF �Ăяo���̃��C�t �T�C�N����Ǘ����邽�߁AXLL �A�h�C�����g�����Ƃ̂ł���C�x���g�̃Z�b�g���񋟂���܂��B�����̃C�x���g�́AExcel �ł̌v�Z�������������A�v�Z���������ꂽ��������܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p107">Excel provides a set of events that an XLL add-in can use in order to manage the life cycle of asynchronous UDF calls. These events indicate that Excel is finished with calculations or that the calculation was canceled.</span></span>
  
### <a name="declaring-an-asynchronous-function"></a><span data-ttu-id="1cc1a-133">非同期関数を宣言する</span><span class="sxs-lookup"><span data-stu-id="1cc1a-133">Declaring an asynchronous function</span></span>

<span data-ttu-id="1cc1a-p108">�񓯊��̃��[�U�[��\`�֐��̓o�^���ɁA�����񓯊��Ƃ��Đ錾����K�v������܂��B����́AXLOPER12 �\�� (�o�^�^�C�v�̕������ "X" �ƕ\�������) ��|�C���g����p�����[�^�[�� UDF �p�����[�^�[�̈ꗗ�̔C�ӂ̏ꏊ�ɒǉ����邱�Ƃɂ���Ď��s����܂��BExcel �ł́A���̃p�����[�^�[��g�p���Ĕ񓯊��̌Ăяo���n���h����n���܂��BXLL �A�h�C���́A�񓯊��̌Ăяo���n���h���ƁA�֐��̌��ʂ̏������ł����炻�̌��ʂ� Excel �ɓn���K�v������܂��B����ɁAUDF �̖߂�l�̌^�́A������^�̍ŏ��̕����Ƃ��� ">" �ɂ���Ďw�肳��� **void** �łȂ���΂Ȃ�܂���BUDF �̓��������� Excel �ɒl��Ԃ��Ȃ����߁A�߂�l�̌^�� void �ł��B����ɁAXLL �A�h�C�����R�[���o�b�N�ɂ���Ēl��񓯊��ŕԂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p108">You must declare asynchronous user-defined functions as asynchronous when they are registered. This is performed by adding a parameter that points to a XLOPER12 structure, represented by "X" in the registration type string, anywhere in the list of UDF parameters. Excel uses this parameter to pass the asynchronous call handle. The XLL add-in must pass the asynchronous call handle and the result of the function back to Excel when the result is ready. In addition, the return type of the UDF should be **void**, designated by ">" as the first character in the type string. The return type is void because the synchronous part of the UDF does not return a value to Excel. Instead, the XLL add-in returns a value asynchronously through a callback.</span></span> 
  
<span data-ttu-id="1cc1a-141">�񓯊��̊֐���X���b�h �Z�[�t�Ƃ��Đ錾����ƁAUDF �̓����������}���\`�X���b�h�̍Čv�Z�Ŏg�p����܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-141">You can declare asynchronous functions as thread-safe and then the synchronous part of the UDF is used in a multi-threaded recalculation.</span></span> 
  
<span data-ttu-id="1cc1a-142">���̃R�[�h��́A"\>QX" ��o�^�^�C�v�̕�����Ƃ��Ďg�p���ēo�^���ꂽ�񓯊��̃��[�U�[��\`�֐�������܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-142">The following code example shows an asynchronous user-defined function registered by using "\>QX" as the registration type string:</span></span>
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a><span data-ttu-id="1cc1a-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="1cc1a-143">Returning values</span></span>

<span data-ttu-id="1cc1a-144">�񓯊��̌Ăяo���̌��ʂ̏������ł�����A�^ [xlAsyncReturn](xlasyncreturn.md) �̃R�[���o�b�N����s���邱�Ƃɂ���� XLL �A�h�C���͂��̌��ʂ� Excel �ɕԂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-144">When the result of the asynchronous call is ready, the XLL add-in returns the result to Excel by performing a callback of type [xlAsyncReturn](xlasyncreturn.md).</span></span>
  
<span data-ttu-id="1cc1a-p109">**xlAsyncReturn** �́A�Čv�Z���Ɍv�Z�ȊO�̃X���b�h�Ɏg�p�ł���B��̃R�[���o�b�N�ł��B���������āA�񓯊��� UDF �̔񓯊������ő��̃R�[���o�b�N�͎��s���Ȃ��ł��������B</span><span class="sxs-lookup"><span data-stu-id="1cc1a-p109">**xlAsyncReturn** is the only callback you can use on non-calculation threads during recalculation. Therefore, the asynchronous part of an asynchronous UDF should not perform any other callbacks.</span></span> 
  
### <a name="handling-events"></a><span data-ttu-id="1cc1a-147">イベントを処理する</span><span class="sxs-lookup"><span data-stu-id="1cc1a-147">Handling events</span></span>

<span data-ttu-id="1cc1a-148">Excel 2010 以降では、xlls は非同期関数のライフサイクルを管理するように設計されたイベントを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="1cc1a-148">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="1cc1a-149">詳しくは、「[イベントの処理](handling-events.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="1cc1a-149">For more information, see [Handling Events](handling-events.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1cc1a-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cc1a-150">See also</span></span>

- [<span data-ttu-id="1cc1a-151">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="1cc1a-151">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

