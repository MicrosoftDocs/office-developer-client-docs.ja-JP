---
title: ���b�Z�[�W�̑��M �g�����X�|�[�g �v���o�C�_�[�̃^�X�N
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 431e3d2f66616db2c586b76387a8521832ed985f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426549"
---
# <a name="sending-messages-transport-provider-tasks"></a>メッセージの送信: トランスポートプロバイダーのタスク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **�g�����X�|�[�g �v���o�C�_�[�A���b�Z�[�W�𑗐M����ɂ�**
  
- トランスポートプロバイダーがメッセージを送信したか、またはメッセージを送信しようとした後に、メッセージの**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定します。 If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. メッセージが正常に送信され、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティが TRUE に設定されている場合は、成功した受信者を含む[adrlist](adrlist.md)構造を作成します。**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) プロパティを各に設定し、 **StatusRecips**を呼び出して配信レポートを生成します。 For more information about creating delivery and non-delivery reports, see the following topics: [MAPI Report Messages](mapi-report-messages.md), [Required Report Message Properties](required-report-message-properties.md), [Optional Report Message Properties](optional-report-message-properties.md), and [Sending Message Delivery Reports](sending-message-delivery-reports.md).
    
- メッセージの**PR_SENDER**グループのプロパティを、ログオンしているユーザーの id に設定します。 このグループには、次のものが含まれます。 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))、 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))、 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))、および**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))。
    
- �\�ł���΁A���O�I�����Ă��郆�[�U�[�� id�A�܂��͑㗝�l���L���ȃ��[�U�[�ɂ́A���b�Z�[�W�� **PR_SENT_REPRESENTING**�̃v���p�e�B��ݒ肵�܂��B **PR_SENT_REPRESENTING**�v���p�e�B�́A���̃��[�U�[�̑㗝�Ƃ��āA���b�Z�[�W�̑��M���������A1 �̃��[�U�[���g�p����܂��B�����̃v���p�e�B��T�|�[�g���Ă��Ȃ��g�����X�|�[�g �v���o�C�_�[�𖳎����đ��M���b�Z�[�W�ɂ��܂��B 
    
- メッセージの**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティを設定して、クライアントが[IMessage:: submitmessage](imessage-submitmessage.md)を呼び出したことを示します。
    
- メッセージストアプロバイダーがメッセージを送信済みとしてマークした日時を示すように、メッセージの**PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) プロパティを設定します。 
    
���܂��܂ȃ��b�Z�[�W���O �V�X�e����������̎�M�҂Ƀ��b�Z�[�W�����M�����ƁA���M���ꂽ�e�R�s�[�ɂ́A���܂��܂ȑ��M�� id ������܂��B 
  
The transport provider or tightly coupled message store and transport is also responsible for setting originator and reply-to information. Originator information is stored in the **PR_ORIGINATOR** properties and reply-to information is stored in the PR_REPLY properties. The client can set these properties; however, the transport provider is allowed to ignore and overwrite the client's settings. 
  

