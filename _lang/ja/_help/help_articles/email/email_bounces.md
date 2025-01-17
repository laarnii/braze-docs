---
nav_title: メールバウンス
article_title: メールバウンス
page_order: 0
page_type: solution
description: "このヘルプ記事では、ハードバウンスとソフトバウンスの違いを明確にしている。"
channel: email
---

# メールのバウンス

メールキャンペーンからのメッセージがユーザーのメールアドレスからバウンスバックしてきた場合、どうすればいいのだろうか？まず、メールのバウンスにはハードバウンスとソフトバウンスの2種類がある。 

## ハードバウンド

メールメッセージがハードバウンスした場合、メールアドレスが無効であるか、存在しないかのどちらかである。この場合、Brazeはメールアドレスを無効としてマークするが、ユーザーのサブスクリプションステータスは更新しない[。][1]この時点で、Brazeは、無効とマークされたこれらのメールアドレスにメッセージを送信しようとしない。

## ソフトバウンド

ソフトバウンスは、受信者のメールアドレスが有効な場合や、受信者のメールサーバーには届いたが、一時的な問題でメッセージが拒否された場合に発生する。このような一時的な問題は、以下のような場合に発生する可能性がある：
- 受信トレイが一杯になっている
- メッセージが大きすぎて受信トレイに入らない。  
- メールサーバーがダウンした

メールがソフトバウンスした場合、通常72時間以内に再試行するが、再試行回数は受信者によって異なる。

ソフトバウンスはキャンペーン分析ではトラッキングされないが、[メッセージアクティビティログで][3]ソフトバウンスを監視することができる。ソフトバウンスの理由や、メールキャンペーンの「送信」と「配信」の不一致を把握することもできる。

メールサブスクリプションとキャンペーンの管理については、[メールのベストプラクティスを][2]参照。

まだ助けが必要か？[サポートチケットを]({{site.baseurl}}/braze_support/)開封する。

_最終更新日：2024年5月2日_

[1]: {{site.baseurl}}/user_guide/message_building_by_channel/email/managing_user_subscriptions
[2]: {{site.baseurl}}/user_guide/message_building_by_channel/email/best_practices
[3]: {{site.baseurl}}/user_guide/administrative/app_settings/message_activity_log_tab/
