---
nav_title: スケジュール配信
article_title: スケジュール配信
page_order: 0
page_type: reference
description: "この参考記事では、キャンペーン配信の時間ベースのスケジュール設定オプションの違いについて説明します。"
tool: Campaigns

---

# スケジュール配信

> 時間ベースのスケジュール配信を使用して送信されたキャンペーンは、指定された日に配信されます。

![][3]

## オプション 1: キャンペーン開​​始後すぐに送信

キャンペーン開始後すぐにメッセージを送信することを選択した場合、キャンペーンの作成が完了するとすぐにメッセージの送信が開始されます。

![][10]

このタイプのスケジュールは、現行のイベントに関するメッセージなど、すぐに送信したい 1 回限りのキャンペーン向けに設定されています。たとえば、スポーツアプリでは、このオプションを使用してスコア更新に関するプッシュ通知をスケジュールできます。また、自分自身または自分のチームだけに向けたテストメッセージを送信する場合にも、このオプションを使用すると、メッセージをすぐに配信できます。 

テストを確認した後にキャンペーンを編集して再度送信したい場合は、ユーザーを [再有効化][24] するチェックボックスを必ずオンにし、キャンペーンを受信できるようにします。デフォルトでは、そのボックスがオンになっていない限り、Braze からユーザーにキャンペーンが 1 度だけ送信されます。

## オプション 2: 指定した時刻に送信

指定した時間にキャンペーンをスケジュールする場合、キャンペーンを送信する曜日と時刻を指定できます。メッセージを 1 度、毎日、毎週、または毎月、特定の時間に送信したり、キャンペーンの開始日と終了日を指定したりできます。この終了日には、終了日として指定した日も含まれます。つまり、最後の送信は指定した終了日に行われます。 

**スケジュール配信**を選択し、ユーザーの現地時間で送信するように指定しなかった場合、キャンペーンは**会社の設定**ページで指定されたタイムゾーンに従って送信されます。

![][9]

### ローカルタイムゾーンでのキャンペーン

ユーザーのローカルタイムゾーンにあわせてメッセージを配信できるため、海外のオーディエンスに都合が良くない時間に通知が届くことがありません。ローカルタイムゾーンでのキャンペーンは、すべてのタイムゾーンの対象ユーザーがキャンペーンを受信できるように、24 時間前にスケジュールする必要があります。ローカルタイムゾーンでのキャンペーンの仕組みと関連する配信ルールに関しては、[キャンペーン FAQ][25] でご確認ください。

ローカルタイムゾーンでのキャンペーンの対象となるセグメントには、すべてのタイムゾーンのユーザーを組み込むため、少なくとも 2 日間の期間を設ける必要があります。たとえば、キャンペーンが夕方に送信されるようにスケジュールされているものの、期間が 1 日しかない場合、タイムゾーンに達したときに一部のユーザーがセグメントから外れてしまう可能性があります。2 日間の期間を作成するフィルタの例としては、「最後に使用したのが 1 日以上前」と「最後に使用したのが 3 日以内」の組み合わせや、「最初に購入したのが 7 日以上前」と「最初に購入したのが 9 日以内」の組み合わせなどです。 

### ユースケース

指定されたタイムスケジュールは、事前にスケジュールされたメッセージや、条件を満たしたユーザー全員に対して定期的に実行されるオンボーディングやリテンションなどの定期的なキャンペーンに最適です。

## オプション 3: インテリジェントタイミング

[インテリジェントタイミング][8] を使用すると、各ユーザーに異なる時間にキャンペーンを配信できます。Braze は、ユーザーがアプリと通知に通常アクセスする時間を基に、各個人の時間を計算します。オプションで、インテリジェントタイミングのキャンペーンが 1 日の特定の時間帯にのみに送信するように指定することもできます。たとえば、深夜に終了するプロモーションをユーザーに通知する場合、遅くとも午後 10 時までにメッセージの送信が必要になります。

![][14]

### 配信ルール

ユーザーにとって最適な時間は 24 時間の中の任意の時間になるため、インテリジェントタイミングのキャンペーンは 24 時間前にスケジュールする必要があります。さらに、1 日の期間を設けたメッセージでは、時間指定キャンペーンと同様に、タイムゾーンの最適な時間に達する前にセグメントから外れてしまったユーザーを見逃してしまいます。インテリジェントタイミングのキャンペーンのセグメントには、これを考慮して少なくとも 3 日間の期間を組み込む必要があります。

ユーザーのプロファイルに最適な時間を計算するのに十分なデータがない場合は、代わりに、全ユーザーの間でアプリが最もよく利用されている時間帯に送信するか、設定したカスタムフォールバック時間に送信するかを選択できます。 

### ユースケース

インテリジェントタイミングのキャンペーンは、ニュース速報や時間指定されたアナウンスに適していない場合など、配信時間に関して柔軟性がある 1 回限りの繰り返しメッセージに最適です。

[3]: {% image_buster /assets/img_archive/time_based.png %}
[8]: {{site.baseurl}}/user_guide/sage_ai/intelligence/intelligent_timing/
[9]: {% image_buster /assets/img_archive/schedule_designated.png %}
[10]: {% image_buster /assets/img_archive/schedule_immediately.png %}
[14]: {% image_buster /assets/img_archive/schedule_intelligent.png %}
[24]: {% image_buster /assets/img_archive/ReEligible.png %}
[25]: {{site.baseurl}}/user_guide/engagement_tools/campaigns/faq/#how-do-i-schedule-a-local-time-zone-campaign/
[34]: {% image_buster /assets/img_archive/customEventProperties.png %}