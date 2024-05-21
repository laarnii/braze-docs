---
nav_title: 5月
page_order: 8
noindex: true
page_type: update
description: "この記事には、2019 年 5 月のリリース ノートが含まれています。"
---

# 2019年5月

## コンテンツカード

コンテンツ カードは、顧客のアプリおよび Web エクスペリエンス内に表示される永続的なコンテンツです。

コンテンツ カードを使用すると、顧客の体験を中断することなく、顧客が愛用しているアプリ内で、ターゲットを絞った動的なリッチ コンテンツ ストリームを顧客に送信できます。または、コンテンツ カードを電子メールやプッシュ通知などの他のチャネルと組み合わせて、一貫性のあるマーケティング戦略を実現することもできます。

![Content Cards Feed]({% image_buster /assets/img/cc-feed.png %}){: height="50%" width="50%"}

さらに、コンテンツ カードは、カードのピン留め、カードの削除、API ベースの配信、カスタム カードの有効期限、カード分析など、よりパーソナライズされた機能をサポートします。

通知センター、ホームページ フィード、プロモーション フィードを作成するために使用します。

サポートされている Braze SDK バージョンに更新する必要があります。
\- iOS:3.8.0以降
\- アンドロイド:2.6.0以降
\- ウェブ:2.2.0以降

[コンテンツ カードの詳細については、こちらをご覧ください。]({{site.baseurl}}/user_guide/message_building_by_channel/content_cards/overview/)

{% alert update %}
Currents のコンテンツ カードとコンテンツ カードの API ドキュメントは、今週後半にリリースされる予定です。しばらくお待ちください。
{% endalert %}

## Roku プラットフォームの追加

Braze の機能に新しいチャネルが追加されました。新しいチャネルに拡大することで、お客様は視聴行動を理解してデータを充実させたり、関連するすべてのチャネルを通じて消費者に有意義な体験を提供したりできるようになります。

データの拡充とカスタム イベントの追跡のために [、Roku デバイスからデータを取得できる]({{site.baseurl}}/developer_guide/platform_integration_guides/roku/initial_sdk_setup/) ようになりました。

## キャンバスまたはキャンペーンの更新に関する通知設定

この [新しい通知は]({{site.baseurl}}/user_guide/administrative/company_settings/notification_preferences/#notification-preferences) 、キャンペーンまたはキャンバスがアクティブ化、更新、再アクティブ化、または非アクティブ化されたときに電子メールで通知します。Braze アカウントの **通知設定** でこれを有効にします。

## Jampp テクノロジー パートナー ドキュメント

Jampp は、モバイル カスタマーの獲得とリターゲティングを行うパフォーマンス マーケティング プラットフォームです。行動データと予測およびプログラマティック技術を組み合わせ、消費者の初回購入や複数回の購入を促すパーソナライズされた関連性の高い広告を表示することで、広告主に収益をもたらします。

Braze のお客様は、Braze Webhook チャネルを構成してイベントを Jampp にストリーミングすることで、[Jampp と統合]({{site.baseurl}}/partners/advertising_technologies/retargeting/jampp/) できます。その結果、顧客はモバイル広告エコシステム内で Jampp を活用し、リターゲティング イニシアチブにさらに豊富なデータ セットを追加できるようになります。

## アプリ内メッセージのプラットフォーム選択

キャンペーン作成プロセスのこのステップを強調するプラットフォーム ピッカーを使用すると、アプリ内メッセージの送信先と対象プラットフォームの選択が簡単になります。

![プラットフォームピッカー][1]

## 電子メールのディスパッチID Currentsフィールド

{% alert update %}
行動 `dispatch_id` Braze は、Canvas ステップ (スケジュール可能なエントリ ステップを除く) を、たとえ「スケジュール」されている場合でもトリガーされたイベントとして扱うため、Canvas とキャンペーンでは異なります。詳細はこちら [`dispatch_id`]({{site.baseurl}}/help/help_articles/data/dispatch_id/) キャンバスとキャンペーンでの動作。

_2019 年 8 月に更新が記録されました。_
{% endalert %}

Currentsの機能強化を継続するために、 `dispatch_id` すべてのコネクタ タイプにわたる Currents メール イベントへのフィールドとして。

の `dispatch_id` Braze プラットフォームから送信される各送信またはディスパッチに対して生成される一意の ID です。

スケジュールされたメッセージを受信したすべての顧客には、同じメッセージが送信されます。 `dispatch_id`アクションベースまたはAPIトリガーメッセージを受信した顧客には、固有の `dispatch_id` メッセージごとに。の `dispatch_id` このフィールドを使用すると、定期的なキャンペーンのどのインスタンスがコンバージョンに寄与しているかを特定できるため、どのタイプのキャンペーンがビジネス目標の達成に役立っているかについて、より多くの洞察と情報が得られます。

## 「自分のものだけを表示」キャンペーン並べ替え機能

ユーザーが `Only Show Mine` キャンペーン グリッドのチェックボックスをオンにすると、結果はログインしたユーザーが作成したキャンペーンのみにフィルターされます。さらに、ユーザーは検索バーに入力して `created_by_me:true`。

また、キャンペーン グリッド サイドバーのサイズも変更できるようになりました。

## エイリアスでユーザーを削除する

これで、 `users/delete`[エイリアスでユーザーを削除する]({{site.baseurl}}/api/endpoints/user_data/#user-delete-request)エンドポイント!

## メールのクリックと開封の独自の計算

メールのユニーククリック数とユニーク開封数は、ユーザーごとに7日間の期間で記録され、その7日間の期間内に1回ずつカウントされます。 `dispatch_id`。

使用 `dispatch_id` 繰り返しメッセージで、各メッセージの実際のユニーク開封数またはユニーククリック数を反映できます。顧客がこのデータを照合するのは簡単になります。 `dispatch_id`Currents でご利用いただけます。

Mailjet も使用しているユーザーは、以前の一意性の期間が 30 日を超えていたため、これらの数値が急増することがわかります。この変更については 3 週間前にお知らせしているはずです。 SendGrid のお客様には違いは見られません。

これらの更新された用語は [、レポート メトリックの用語集]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/)で検索できます。

{% alert update %}
行動 `dispatch_id` キャンバスとキャンペーンでは異なります。Braze は、キャンバスのステップ (スケジュール可能なエントリ ステップを除く) を、たとえ「スケジュール」されていてもトリガーされたイベントとして扱うためです。[詳細を見る [`dispatch_id`]({{site.baseurl}}/help/help_articles/data/dispatch_id/) キャンバスとキャンペーンでの動作。

_2019 年 8 月に更新が記録されました。_
{% endalert %}


## 最もエンゲージメントの高いチャンネル

{% alert update %}
[2019 年 11 月の製品リリース]({{site.baseurl}}/help/release_notes/2019/november/#intelligence-suite)以降、「最もエンゲージメントの高いチャネル」は [「インテリジェント チャネル」]({{site.baseurl}}/user_guide/intelligence/intelligent_channel/)に名前が変更されました。
{% endalert %}

最もエンゲージメントの高いチャネル フィルターは、選択したメッセージング チャネルが「最適な」チャネルであるオーディエンスの部分を選択します。この場合、「最適」とは、「ユーザーの履歴を考慮すると、エンゲージメントの可能性が最も高い」ことを意味します。チャネルとして、電子メール、Web プッシュ、またはモバイル プッシュ (利用可能なモバイル OS またはデバイスを含む) を選択できます。

この新しいフィルターを[セグメンテーションフィルターライブラリ\]({{site.baseurl }})でチェックしてください。/user_guide/engagement_tools/segments/segmentation_filters/).

[1]: {% image_buster /assets/img/iam_platforms.gif %}