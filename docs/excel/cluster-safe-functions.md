---
title: クラスター セーフ機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798760"
---
# <a name="cluster-safe-functions"></a>クラスター セーフ機能

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Excel 2013 �ł́AExcel ����p�̃N���X�^�[ �R�l�N�^ �C���^ �t�F�[�X���āA���p�t�H�[�}���X�̃R���s���[�e�B���O �N���X�^�[�ɑ΂��郆�[�U�[��`�֐� (UDF) �Ăяo����I�t���[�h�ł��܂��B�v�Z�N���X�^�[�̃x���_�[�ɂ��N���X�^�[ �R�l�N�^���񋟂���Ă��܂��BUDF �̍쐬�҂́A�쐬���� UDF ��N���X�^�[ �Z�[�t�Ƃ��Đ錾�ł��܂��B�N���X�^�[ �R�l�N�^�����݂���ꍇ�AExcel �͂����� UDF �̌Ăяo����I�t���[�h���邽�߂ɃN���X�^�[ �R�l�N�^�ɑ��M���܂��B
  
Excel �́A�Čv�Z���ɃN���X�^�[ �Z�[�t UDF ����o����ƁA���ݎ��s���� XLL ���A�N���X�^�[ �Z�[�t UDF�A����єC�ӂ̃p�����[�^�[��N���X�^�[ �R�l�N�^�ɓn���܂��B�R�l�N�^�� UDF �Ăяo��������[�g�Ŏ��s���A���ʂ� Excel �ɕԂ��܂��B�ˑ����Ȃ��v�Z�����s����A�N���X�^�[ �R�l�N�^�� UDF �̎��s���������ƌ��ʂ� Excel �ɓn���āA�ˑ�����v�Z�𑱍s���܂��B���̔񓯊�����̃��J�j�Y���́A�񓯊��̓����Ǘ�����̂� UDF �쐬�҂ł͂Ȃ��N���X�^�[ �R�l�N�^�ł���Ƃ����_������΁A�񓯊� UDF �ɂ���Ďg�p����郁�J�j�Y���Ɠ����ł��B�ʏ�A�N���X�^�[ �R�l�N�^�� XLL shim ��������� XLL ��ǂݍ��݁A�v�Z�N���X�^�[ �m�[�h��� UDF ����s���܂��B
  
�N���X�^�[ �Z�[�t�Ƃ��� UDF ��錾���邵���݂́A�}���` �X���b�h�̍Čv�Z�Ɋւ��� UDF ����S�Ƃ��Đ錾���邵���݂Ɏ��Ă��܂��B�������AUDF �͕K��������� Excel �Z�b�V�����̑��� UDF �Ɠ����R���s���[�^�[��Ŏ��s�����킯�ł͂Ȃ����߁A�N���X�^�[ �Z�[�t UDF ��L�q����ۂɂ́A���܂��܂ȍl�����������݂��܂��B
  
UDF をクラスター セーフとして登録するには、 **Excel12**または**Excel12v**のインターフェイスを使用[(フォーム 1) の xlfRegister](xlfregister-form-1.md)コールバック関数を呼び出す必要があります。 これらのインターフェイスの詳細については、 [Excel4/Excel12](excel4-excel12.md)と[Excel4v と Excel12v](excel4v-excel12v.md)を参照してください。 として UDF を登録するクラスター セーフ**Excel4**または**Excel4v**のインターフェイスではサポートされていません。 
  
�N���X�^�[ �Z�[�t�Ƃ��Ċ֐���o�^����ꍇ�́A�֐����N���X�^�[ �Z�[�t�ȕ��@�œ��삷�邱�Ƃ�m�F����K�v������܂��B�N���X�^�[ �R�l�N�^�̌����ȓ���͎����ɂ���ĈقȂ�܂����AUDF �́A���U�R���s���[�^�[ �V�X�e����Ŏ��s���A�܂����̂悤�ȓ�������悤�ɐ݌v����K�v������܂��B
  
- UDF �̓������̏�ԂɈˑ����Ȃ��B���Ƃ��΁AUDF �͊����̃�������L���b�V���ȂǂɈˑ����Ă��Ă͂Ȃ�܂���B
    
- UDF �̓N���X�^�[ �R�l�N�^ �v���o�C�_�[�ŃT�|�[�g����Ă��Ȃ� Excel �R�[���o�b�N����s���Ȃ��B
    
�N���X�^�[ �Z�[�t UDF �ɂ́A�N���X�^�[ �Z�[�t�̓���̑��ɂ�A���̂悤�ȋZ�p�I�Ȑ���������܂��B
  
1. XLOPER ���� ('P' �^�A'R' �^) �͎g�p�ł��܂���B
    
2. �͈͎Q�Ƃ�T�|�[�g���� XLOPER12 ���� ('U' �^) �͎g�p�ł��܂���B
    
3. �}�N�� �V�[�g�̓����̊֐��ł����Ă͂Ȃ�܂��� ('#' �� '&amp;' ��g�ݍ��킹�邱�Ƃ͂ł��܂���)�B
    
���s���Ԃ��Z�� UDF �̏ꍇ�́A�I�t���[�h�̃I�[�o�[�w�b�h�� UDF�̎��s�ɂ����鎞�Ԃ���傫���Ȃ��āA���̃C���t���X�g���N�`����g�p���Ă�قƂ�ǃv���X�ɂȂ�Ȃ��\��������܂��B
  
> [!NOTE]
> [!����] �N���X�^�[ �Z�[�t UDF �͔񓯊� UDF �Ƃ��Đ錾�ł��܂���B 
  
UDF �́A[xlRunningOnCluster](xlrunningoncluster.md) �R�[���o�b�N�֐���Ăяo�����Ƃɂ���āA�N���X�^�[ �R�l�N�^��g�p���Ď��s����Ă��邩�ǂ����𔻕ʂł��܂��B 
  

