---
title: クラスター セーフ関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310977"
---
# <a name="cluster-safe-functions"></a><span data-ttu-id="1f7f3-103">クラスター セーフ関数</span><span class="sxs-lookup"><span data-stu-id="1f7f3-103">Cluster safe functions</span></span>

<span data-ttu-id="1f7f3-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f7f3-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1f7f3-p101">Excel 2013 では、Excel が専用のクラスター コネクタ インタ フェースを介して、高パフォーマンスのコンピューティング クラスターに対するユーザー定義関数 (UDF) 呼び出しをオフロードできます。計算クラスターのベンダーによりクラスター コネクタが提供されています。UDF の作成者は、作成する UDF をクラスター セーフとして宣言できます。クラスター コネクタが存在する場合、Excel はこれらの UDF の呼び出しをオフロードするためにクラスター コネクタに送信します。</span><span class="sxs-lookup"><span data-stu-id="1f7f3-p101">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface. Compute cluster vendors provide Cluster Connectors. UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="1f7f3-p102">Excel �́A�Čv�Z���ɃN���X�^�[ �Z�[�t UDF ����o����ƁA���ݎ��s���� XLL ���A�N���X�^�[ �Z�[�t UDF�A����єC�ӂ̃p�����[�^�[��N���X�^�[ �R�l�N�^�ɓn���܂��B�R�l�N�^�� UDF �Ăяo��������[�g�Ŏ��s���A���ʂ� Excel �ɕԂ��܂��B�ˑ����Ȃ��v�Z�����s����A�N���X�^�[ �R�l�N�^�� UDF �̎��s���������ƌ��ʂ� Excel �ɓn���āA�ˑ�����v�Z�𑱍s���܂��B���̔񓯊�����̃��J�j�Y���́A�񓯊��̓����Ǘ�����̂� UDF �쐬�҂ł͂Ȃ��N���X�^�[ �R�l�N�^�ł���Ƃ����_������΁A�񓯊� UDF �ɂ���Ďg�p����郁�J�j�Y���Ɠ����ł��B�ʏ�A�N���X�^�[ �R�l�N�^�� XLL shim ��������� XLL ��ǂݍ��݁A�v�Z�N���X�^�[ �m�[�h��� UDF ����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-p102">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector. The connector runs the UDF call remotely and returns the results to Excel. Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue. The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author. Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="1f7f3-p103">�N���X�^�[ �Z�[�t�Ƃ��� UDF ��錾���邵���݂́A�}���\` �X���b�h�̍Čv�Z�Ɋւ��� UDF ����S�Ƃ��Đ錾���邵���݂Ɏ��Ă��܂��B�������AUDF �͕K��������� Excel �Z�b�V�����̑��� UDF �Ɠ����R���s���[�^�[��Ŏ��s�����킯�ł͂Ȃ����߁A�N���X�^�[ �Z�[�t UDF ��L�q����ۂɂ́A���܂��܂ȍl�����������݂��܂��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-p103">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation. However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="1f7f3-p104">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface. For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md). Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span><span class="sxs-lookup"><span data-stu-id="1f7f3-p104">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface. For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md). Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="1f7f3-p105">�N���X�^�[ �Z�[�t�Ƃ��Ċ֐���o�^����ꍇ�́A�֐����N���X�^�[ �Z�[�t�ȕ��@�œ��삷�邱�Ƃ�m�F����K�v������܂��B�N���X�^�[ �R�l�N�^�̌����ȓ���͎����ɂ���ĈقȂ�܂����AUDF �́A���U�R���s���[�^�[ �V�X�e����Ŏ��s���A�܂����̂悤�ȓ�������悤�ɐ݌v����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-p105">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way. Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="1f7f3-p106">UDF �̓������̏�ԂɈˑ����Ȃ��B���Ƃ��΁AUDF �͊����̃�������L���b�V���ȂǂɈˑ����Ă��Ă͂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-p106">A UDF should not rely on any memory state. For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="1f7f3-122">UDF �̓N���X�^�[ �R�l�N�^ �v���o�C�_�[�ŃT�|�[�g����Ă��Ȃ� Excel �R�[���o�b�N����s���Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="1f7f3-123">�N���X�^�[ �Z�[�t UDF �ɂ́A�N���X�^�[ �Z�[�t�̓���̑��ɂ�A���̂悤�ȋZ�p�I�Ȑ���������܂��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="1f7f3-124">XLOPER ���� ('P' �^�A'R' �^) �͎g�p�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="1f7f3-125">�͈͎Q�Ƃ�T�|�[�g���� XLOPER12 ���� ('U' �^) �͎g�p�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="1f7f3-126">�}�N�� �V�[�g�̓����̊֐��ł����Ă͂Ȃ�܂��� ('#' �� '&amp;' ��g�ݍ��킹�邱�Ƃ͂ł��܂���)�B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="1f7f3-127">���s���Ԃ��Z�� UDF �̏ꍇ�́A�I�t���[�h�̃I�[�o�[�w�b�h�� UDF�̎��s�ɂ����鎞�Ԃ���傫���Ȃ��āA���̃C���t���X�g���N�\`����g�p���Ă�قƂ�ǃv���X�ɂȂ�Ȃ��\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f7f3-128">[!����] �N���X�^�[ �Z�[�t UDF �͔񓯊� UDF �Ƃ��Đ錾�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="1f7f3-129">UDF �́A[xlRunningOnCluster](xlrunningoncluster.md) �R�[���o�b�N�֐���Ăяo�����Ƃɂ���āA�N���X�^�[ �R�l�N�^��g�p���Ď��s����Ă��邩�ǂ����𔻕ʂł��܂��B</span><span class="sxs-lookup"><span data-stu-id="1f7f3-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

