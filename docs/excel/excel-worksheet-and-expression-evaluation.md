---
title: Excel ���[�N�V�[�g�Ǝ��̕]��
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 543ff7fcbc88253dafd7fc6e7000bf9657d8c258
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798854"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Excel ���[�N�V�[�g�Ǝ��̕]��

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ���[�N�V�[�g�̃Z���̓�e�́A���� 4 �̊�{�I�ȃf�[�^�^�̂����ꂩ�ɕ]������܂��B
  
- **Numbers**
    
- **Boolean TRUE** �܂��� **FALSE**
    
- **Strings**
    
- **エラー**
    
�֐��̈����Ƃ��āA�܂��͔z�񐔎���̕����̃Z���ɂ܂�����l�Ƃ��āA�����̃f�[�^�^�̍����z��𐔎��ɓ��͂��邱�Ƃ�ł��܂��B
  
���[�U�[ (�܂��̓R�}���h �}�N��) ���Z���ɕ��������͂���ƁAExcel �͓��͂̉�߂���݁A��߂ł��Ȃ��ꍇ�ɂ̓G���[ ���b�Z�[�W��\�����܂��B���͒l��������̃v���t�B�b�N�X (�P����p��) �Ŏn�܂��Ă���ꍇ�́AExcel �́A���ׂĂ̓��͕�������̂܂ܕύX�����ɃZ���ɔz�u���܂��B(������̃v���t�B�b�N�X�͕\������܂���B)���͒l���A **=** �A **+** �A **-** �̂����ꂩ�Ŏn�܂�ꍇ�AExcel �͓��͒l�𐔎��Ƃ��ĉ�߂��悤�Ƃ��܂��B�\�����������Ȃ��ꍇ��]������~�����ꍇ�́A�G���[���\������A�Z���͕ҏW���[�h�ɂȂ�܂��B����ȊO�̏ꍇ�AExcel �͉��Z�q����ъ֐����Ƃ��̈����̎��ʁA�ϊ��A�]������݂܂��B 
  
���Z�q���K�p�����O�ɁA�I�y�����h�͍�����E�ɕ]������܂��B�֐��́A�D�揇�ʂ̍������Z�q�Ɠ���q�̈�ԓ���̉��Z�q����]������܂��B�֐��̈�����I�y�����h���A�\�������f�[�^�^�ɕϊ��ł��Ȃ��ꍇ�A�]���͎��s���A **#VALUE!** �G���[�ɂȂ�܂��B�g�[�N�� (���e�����l�ł͂Ȃ�) ���֐������`���A���x���Ƃ��ĔF������Ȃ��ꍇ�A�]���͎��s���A **#NAME?** �G���[�ɂȂ�܂��B 
  
���͒l����L�̂�����ł�n�܂��Ă��Ȃ��ꍇ�́A���t�A�����A�ʉ݁A�p�[�Z���e�[�W�A���l�ȂǁA���m�̓��̓p�^�[���ɏƂ炵�ă`�F�b�N���A�����ɉ����ĉ�߂���܂��B����́A���P�[���ŗL�̕��@�ōs���܂��B��L�̂�����̕��@�ł��߂ł��Ȃ��ꍇ�́A������Ƃ��ĔF����������A�Z���̓�e�͕ύX����܂���B
  
Excel �͑��̃f�[�^�^��T�|�[�g���Ă���A���̒��ōł�悭�m���Ă���̂́A�͈͎Q�Ƃł��B�Q�ƈ�����Ƃ�Ȃ����Z�q��֐��̈�����]��������A�܂��̓Z���̐�����ɂ��鎮��Q�Ƃɏk�߂��肷��ƁA�Q�Ƃ͎Q�Ɛ�Z���̒l�ɕϊ�����܂��B
  
Excel �ł́AXLM �֐� **EVALUATE** �܂��͂���ɑ������� C API�֐� **xlfEvaluate** ��g���āA�L���ȕ������A���[�N�V�[�g�p�̊�{�I�� 4 �̃f�[�^�^�̂����ꂩ�ɏk�߂�@�\�����J����Ă��܂��B���ł���̊֐���g�p����ƁADLL �R�[�h��̖��O�t���͈͂�ȒP�ɕ]�����邱�Ƃ��ł��܂��B���̊֐��́A�G���[���b�Z�[�W��\��������A�Z���̕ҏW��\�ɂ����肷��̂ł͂Ȃ��A���̕]�����ł��Ȃ��ꍇ�� **#VALUE!** �G���[��Ԃ��Ƃ����_�ŁA�O�q�̓���Ƃ͈قȂ�܂��B 
  
## <a name="numbers"></a>���l

Excel �̃��[�N�V�[�g�ԍ��͂��ׂāA8 �o�C�g�̔{���x���������_ (���ׂĂ̐�����܂�) �œ���I�ɕ\����܂��B�������AExcel �ɂ����邱���̐��l�̎����́A�ȉ��̕\�Ɏ����悤�ɁAIEEE �K�i�Ɋ��S�ɂ͏������Ă��܂���B
  
|**�^**|**�ő�**|**�ŏ�**|
|:-----|:-----|:-----|
|IEEE 8 �o�C�g�̔{���x���������_�^  <br/> |1.7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|���[�N�V�[�g (�֐��܂��͓\��t���l�ɂ���ĕԂ����)  <br/> |1.7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|���[�N�V�[�g (�葀�����)  <br/> |9.99999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
IEEE �񐳋K���� ( 2.2250738585072009E?308 ���� 4.9406564584124654E?324 �͈̔͂̐��l) �́AExcel ���[�N�V�[�g�ł̓T�|�[�g����Ă��܂��񂪁AVBA �̔{���x���������_�^�ł̓T�|�[�g����Ă��܂��B
  
DLL 関数では、無限大、または、無効な二重の +/-IEEE が返された場合 Excel 変換する **#NUM!** です。 Subnormal すべて Excel で最小の正の標準よりも小さい数値が正の 0 に変換されます。 IEEE 負の 0 がサポートされている、つまり、DLL 関数によって返されることができ、として表示されます **-0**です。 (、**\<** 演算子が負のゼロをチェックしませんので **= A1\<0** A1 には、負のゼロが含まれている場合に**TRUE**に評価された)。 
  
���t�Ǝ����Ȃǂ̈ꕔ�̐��l�����́A��L��������͈͂ɐ�������Ă��邱�Ƃɒ��ӂ��Ă��������B�������Z�͎��ۂɂ͕��������_���Z�ł���A�ɒ[�ȏꍇ�́A���m�ɂ͐����̌��ʂɂȂ�ꍇ�ɔ񐮐��̌��ʂ����炷�ꍇ������܂��B
  
## <a name="long-unicode-strings"></a>���� Unicode ������

���݁AExcel ��ɕ\������Ă��镶����͂��ׂāA�����̃o�[�W�����ɂ����āA����I�� Unicode ������Ƃ��Ċi�[����܂��B���[�N�V�[�g�Ŏg�p���� Unicode ������ł́A�C�ӂ̗L���� Unicode ������ő� 32,767 (2<sup>15</sup>?- 1) �����܂ނ��Ƃ��ł��܂��B 
  
C API ���ŏ��ɓ������ꂽ�Ƃ��A���[�N�V�[�g�̕�����́A���� 255 �����̃o�C�g��ɐ�������Ă��܂������AC API �ł�A�����̐��������f����܂��BExcel 2007 �ł́AC API �́A���� Unicode �����������ł���悤�ɍX�V����Ă��܂��B�܂�ADLL �֐����K�؂ȕ��@�œo�^����Ă���΁AUnicode �̈�����󂯎������AUnicode �������Ԃ����肷�邱�Ƃ��ł��܂��B
  
> [!NOTE]
> [!����] �o�C�g��́A���ʌ݊����̂��߂� C API �Ŋ��S�ɃT�|�[�g����Ă��܂����A����܂łǂ��� 255 �����ɐ�������Ă��܂��B 
  
## <a name="returning-errors"></a>�G���[

�֐��܂��͉��Z�q�̈�����K�؂Ȍ^�ɕϊ��ł��Ȃ��ꍇ�A���邢�͊֐��܂��͒�`�ς݂̖��O���F������Ȃ��ꍇ�AExcel �̓Z����G���[�ɕ]�����܂��B�����̃V�i���I�͂�������L�Ő�����Ă��܂��B�g�ݍ��݃��[�N�V�[�g�֐��Ɖ��Z�q�����s�����ꍇ�A���[�U�[�ɃG���[�̎�ނ�ʒm����G���[��\������܂��B����̃A�h�C���֐��� Excel �̓���Ɛ�������G���[��Ԃ��悤�ɂ��Ă��������B
  
### <a name="null"></a>#NULL!

**#NULL!** �G���[�́A�������� XLM ���֐��ɂ���ĕԂ���܂��B���Ƃ��΁A�v�����^�[���C���X�g�[������Ă��Ȃ��ꍇ�ɁA **GET.DOCUMENT(78)** ��Ăяo�����A�܂��͈��� 78 �œ����� C API �֐� **xlfGetDocument** ��Ăяo���ƁA���̃G���[���Ԃ���邱�ƂɂȂ�܂��B�܂��A��L�G���[�͋�̕����񂪕]�������ꍇ�Ȃǂɂ�A�ꕔ�̊֐��ŕԂ����\��������܂��B 
  
���̂�����̃G���[��K�؂ł͂Ȃ��Ɗ�����ꍇ��A�A�h�C���֐����炱�̃G���[��Ԃ��Ƃ悢�ł��傤�B
  
### <a name="div0"></a>#DIV/0!

���ꂪ 0 �ɕ]������邩�A�܂��͐��l�������� 0 �ȊO�̐��l�ŕ\���Ȃ��ꍇ�ɂ́AExcel �̏��Z���Z�q�� **#DIV/0!** �G���[��Ԃ��܂��B��`��A���Z���֌W����ꕔ�̊֐��ł���̃G���[���Ԃ����ꍇ������܂��B���Ƃ��΁A���͒l�̂��������l�ɕϊ��ł��Ȃ��ꍇ�́A **AVERAGE** �ɂ�肱�̃G���[���Ԃ���܂��B 
  
0 �ɂ�鏜�Z�����o���ꂽ���Ƃ�����ꍇ�ɂ̂݁A�A�h�C���֐����炱�̃G���[���Ԃ����悤�ɂ��Ă��������B
  
### <a name="value"></a>#VALUE!

**#VALUE!** �G���[�́A�֐��܂��͉��Z�q�̈������K�v�Ȍ^�ɕϊ��ł��Ȃ��ꍇ�ɕԂ���܂��B�ϊ��ł��Ȃ��֐��̈��� (��F  `=LN("X")`) �̏ꍇ �A�֐��R�[�h�͌Ăяo����܂���B����́A�Ǝ��̃A�h�C���֐��̍쐬��f�o�b�O��s���ۂɏd�v�ȃ|�C���g�ł��B 
  
�������̊֐��ł́A�֐��R�[�h��ň�����ϊ��ł��Ȃ��ꍇ�ɂ��̃G���[���Ԃ���܂��B���Ƃ��΁A `DATEVALUE("30-Feb-2007")` �͐������^�̈����ł���ɂ������炸�A���̃G���[�𔺂��Ď��s���܂��B���̏ꍇ�A���̊֐��ɂ���Ċ֐��R�[�h�����G���[���Ԃ���܂��B�l�̌^��͈͂����e�͈͂ł����Ă�A�֐��ɂ���Ă͂��̃G���[���Ԃ���܂��B���Ƃ��΁A  `FIND("a","xyz")` �͂��̃G���[��Ԃ��܂��B 
  
������������^�ł��邱�Ƃ�A�������^�ɕϊ��ł��Ȃ��������ƁA�͈͊O�ł��邱�Ƃ�������߂ɁA�A�h�C���֐�����G���[��Ԃ��悤�ɂ��Ă��������B�������A���l�̈������͈͊O�̏ꍇ�� **#NUM!** ��Ԃ��悤�������Ă��������B�͈͂�z������̃T�C�Y��`���قȂ�ꍇ�ɂ�A���̃G���[��Ԃ��悤�������Ă��������B 
  
### <a name="ref"></a>#REF!

���ʓI�ɑ��ΎQ�Ƃ͈̔͊O�̏ꏊ�ɃR�s�[�����ƁA����� **#REF!** �G���[����������܂��B���Ƃ��΁AB2 �Z���ɐ���  `=A1` �������Ă���ꍇ�AB1 �Z���ɂ��̐�����R�s�[����ƁA���ʂ͐��� **=#REF!** �ɂȂ�܂��B���̃G���[�́A�؂���/�\��t������ŏ㏑�����ꂽ�Q�Ƃ�A���s�A���[�N�V�[�g���ƍ폜���ꂽ�Q�Ƃ������Ɋ܂܂��ꍇ�ɂ��������܂��B  `OFFSET(A1,-1,-1)` �ȂǁA�Q�Ƃ�Ԃ��������̊֐��͂��̃G���[��Ԃ��\��������܂��B���[�N�V�[�g���̒�`�ɁA�����ƂȂ�Q�Ƃ��܂܂�Ă���ꍇ�́A���̃G���[�ɕ]������܂��B
  
�A�h�C���֐����Q�ƈ��������Ă��āA�Q�Ƃ������ł��邩�A�܂��͎Q�ƃG���[��ʂ����ꍇ�́A���̃G���[��Ԃ��悤�������Ă��������B[Excel �̃������Ǘ�](memory-management-in-excel.md)�� XLOPER/XLOPER12 �Z�N�V�����ł́A�Q�ƈ�����󂯎��A�Ԃ����Ƃ��ł���֐���쐬������@�ɂ��Đ�����Ă��܂��B 
  
### <a name="name"></a>#NAME?

Excel が生成されます、 **#NAME?** 式には、関数として認識されませんまたは名前を定義するトークンが含まれているとエラーが発生します。 アドインの関数が定義された名前にアクセスしようし、してが定義されていない、このエラーを返すことを検討してください。 
  
### <a name="num"></a>#NUM!

**** �ȂǁA���l���͂����e�͈͊O�̏ꍇ�AExcel �̑g�ݍ��ݐ��l�֐��Ɛ��w�I�֐��̑����� `LN(0)` �G���[��Ԃ��܂��B���l���͂������܂��͔͈͊O�ł��邱�Ƃ�������߁A�A�h�C���֐����炱�̃G���[��Ԃ��悤�������Ă��������B
  
### <a name="na"></a>#N/A

�����̏ꍇ **#N/A** �G���[�́A����Ȍ��ʂ܂��͗L���Ȍ��ʂ����p�ł��Ȃ����Ƃ�\���܂��B���Ƃ��΁A���S��v��������Ȃ������ꍇ�ɂ́A�� 3 ������ 0 �� MATCH �֐���肱�̃G���[���Ԃ���܂��B�܂��A���̃G���[�́A�֐� **NA** ��g�p���A�֐� **ISNA** �ŌʂɌ��o���āA�������邱�Ƃ�ł��܂��B���̂��߁A���̃G���[�́A�A�v���P�[�V�����ŗL�̏���͈͂�������߂Ƀ��[�N�V�[�g�ň�ʓI�Ɏg�p����Ă��܂��B
  
## <a name="see-also"></a>�֘A����



[Excel �v���O���~���O�̊T�O](excel-programming-concepts.md)
  
[Excel �ł� C API ��g�p�����v���O���~���O](programming-with-the-c-api-in-excel.md)
  
[���O�Ƒ��̃��[�N�V�[�g�̎���]������](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK API �֐����t�@�����X](excel-xll-sdk-api-function-reference.md)
