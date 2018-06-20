---
title: イベント通知をサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 45bfe9f9314a154bd5f096ac20f76f6bf4f259c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804020"
---
# <a name="supporting-event-notification"></a>イベント通知をサポートしています。

  
  
**適用されます**: Outlook 
  
イベント通知をサポートできますが、複雑なために、MAPI には、プロセスの最も困難な部分を実装する 3 つのサポート オブジェクトのメソッドが用意されています。 これらのメソッドは、ユニットとして動作し、3 つのすべてまたはどれも、プロバイダーを使用する必要があります。
  
MAPI サポートされている方法では、通知のキーを使用して、通知を生成するオブジェクトとアドバイズ シンクの接続を管理します。 通知キーは、プロセス間でオブジェクトを識別するバイナリ データを格納する[NOTIFKEY](notifkey.md)構造です。 通知キーは通常、長期的なエントリのアドバイズ ソース オブジェクトの id からコピーされます。 クライアントには、**アドバイス**の呼び出しのエントリ id が指定されている場合は、通知のキーを使用できます。 **アドバイズ**する_lpEntryID_パラメーターが NULL の場合は、メッセージ ・ ストアなど、可能な最も外側のコンテナー オブジェクトのエントリ id を使用します。 
  
サポート メソッドを使用するには、クライアントが**通知を登録するのには、メソッド**を呼び出すたびに、 [IMAPISupport::Subscribe](imapisupport-subscribe.md)を呼び出します。 [NOTIFKEY](notifkey.md)構造体を割り当てるし、アドバイスのソース オブジェクトの通知の一意なキーを作成します。 などの特定のフォルダーにメッセージを受信したときにクライアントに通知するように要求するメッセージ ストア プロバイダーはそのフォルダーの通知キーを作成します。 クライアントへのポインターとは、**購読**への呼び出しに**NOTIFKEY**構造体へのポインターを渡すには、シンクが案内します。 **Subscribe**メソッドを呼び出してアドバイズ シンクの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)その参照カウントをインクリメントし、MAPI では、登録をキャンセルするまで、ポインターが保持されます。 
  
渡すことができます NOTIFY_SYNC フラグ**購読**の**通知**が動作することを要求する同期していない戻り値の[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドへのすべての呼び出しを行ったことになるまで登録されているアドバイズ シンクします。 独自の内部の使用のためにのみ、このフラグを設定します。 クライアントの**アドバイス**の呼び出しに応答する場合は設定しません。 クライアントとプロバイダー間でのイベント通知は、常に非同期です。 MAPI を保証する呼び出しを実行中にイベントが発生した**OnNotify**呼び出しのいずれかが行われる前にクライアントに戻ります。 
  
NOTIFY_SYNC フラグを設定する場合、アドバイズ シンク オブジェクトのいずれかに、変更しないでくださいし、**購読**する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)によって作成されたラッパーのアドバイズ シンクを渡さないでください。 **HrThisThreadAdviseSink**は、スレッド セーフでないバージョンの非同期通知のみに使用するアドバイズ シンクを作成します。 
  
同期通知用に登録されているアドバイズ シンクは、CALLBACK_DISCONTINUE フラグを設定して**OnNotify**から返された場合、 [IMAPISupport::Notify](imapisupport-notify.md)は NOTIFY_CANCELED フラグを設定し、 **OnNotify**への呼び出しを作成せずに返します。 
  
コピーを保持する必要がする必要がない**購読**が返されると、クライアントのシンクをアドバイスします。 [リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を解放するメソッドを呼び出します。 **購読**をクライアントに返す必要がありますは 0 以外の接続数を返します。 接続数は、ソース アドバイズとアドバイズ シンク間のリンクを表します。 それまで有効のままクライアント**に**正常な呼び出しを行います。 
  
クライアントの登録をキャンセルする準備ができたら、 **Unadvise**メソッドを呼び出します。 [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) **Unadvise**の呼び出しからの接続数を渡します。 **購読の取り消し**では、アドバイズ シンクの**リ ス**のメソッドを呼び出します。 **アドバイズ**、 **Unadvise**の**購読**および**購読解除**する呼び出しを組み合わせる必要があります。 **購読****購読**に対して行ったすべての呼び出しに対して 1 回の呼び出しを行う必要があります。 ただし、 **Subscribe**を呼び出して **、メソッド**が呼び出されるたびにする必要はありません。 逆に、内部通知を設定するために呼び出すことができます。 
  
イベントが発生してイベントの適切な型の 1 つまたは複数の[通知](notification.md)構造体を割り当てる[IMAPISupport::Notify](imapisupport-notify.md)を呼び出します。 **通知**は、各登録されているアドバイズ シンクに通知を生成します。 未使用のすべてのメンバー、[通知](notification.md)の構造体をゼロを設定する必要があります。 **通知**の構造体を初期化するためには、この手法は、クライアントが高速で、エラーが発生しやすい**OnNotify**実装のサイズを小さくすると、作成に役立ちます。 
  
個別**通知**の構造体が同じ型の複数のイベントであっても、イベントごとに必要なことに注意してください。 たとえば、3 つのクライアントが特定のテーブルにテーブルの通知用に登録されている 5 つの行がテーブルに追加される場合は、作成する必要が 5 つの**OBJECT_NOTIFICATION**構造体の**通知**呼び出しの。 このバッチ通知は、**通知**5 回の呼び出しよりもパフォーマンスの向上になります。 各**通知**の呼び出しには、MAPI は、すべての登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 ある場合は no が登録されているアドバイズ シンクでは、MAPI の呼び出しは無視されます。 
  
バッチ通知を送信するサービス プロバイダーで必要があります順序を最後の最初の通知から解釈できるようにします。 通知バッチには、一連の同じバッチ内の別のイベントに追加された前の行を参照する 1 つのイベントと TABLE_ROW_ADDED などのイベントが含まれている場合は、この順序付けすると特に必要があります。
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)
