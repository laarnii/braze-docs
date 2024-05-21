---
nav_title: インテリジェント・チャンネル・フィルター
article_title: インテリジェント・チャンネル・フィルター
page_order: 0
description: "この記事では、インテリジェント チャネル フィルター (選択したメッセージング チャネルが最適なチャネルであるオーディエンスの部分を選択するフィルター) について説明します。この場合、ユーザーの履歴を考えると、最良の手段がエンゲージメントの可能性が最も高くなります。"
search_rank: 11
---

# [![Braze Learning course]({% image_buster /assets/img/bl_icon2.png %})](https://learning.braze.com/most-engaged-channel){: style="float:right;width:120px;border:0;" class="noimgborder"}インテリジェントチャンネルフィルター[せんじんとろーるふ�

> インテリジェントフィルターまたは `Most Engaged` チャネルフィルターは、選択したメッセージングチャネルが「最適な」チャネルであるオーディエンスの部分を選択します。 

この場合の「ベスト」とは、ユーザーの履歴からしてエンゲージメントの可能性が最も高いチャネルを意味します。チャネルとして、メール、SMS、Web プッシュ、またはモバイルプッシュ (使用可能なモバイル OS またはデバイスを含む) を選択できます。

![][1]{: style="float:right;max-width:40%;margin-left:10px;margin-top:10px;border:0"}

インテリジェント チャネルは、過去 6 か月間のアクティビティで受信したメッセージの数に対するメッセージの対話 (開封またはクリック) の比率を取ることで、3 つのチャネルのそれぞれの各ユーザーのエンゲージメント率を計算します。利用可能なチャネルは、それぞれのエンゲージメント率に応じてランク付けされ、比率が最も高いチャネルが、そのユーザーの「最もエンゲージメントが高い」チャネルになります。 

メッセージがユーザーに送信されるたびに、またはユーザーがメッセージと対話するたびに、エンゲージメント率は数秒以内に再計算されます。ユーザーは、メッセージを操作したと 1 回のみカウントできます (たとえば、同じメールを開いてクリックすると、そのメッセージは 2 回ではなく 1 回だけ関与したものとしてマークされます)。 

インテリジェントチャネルフィルターを有効にするには、メール、Web プッシュ、またはモバイルプッシュキャンペーンの作成時に [**ターゲットユーザー**] ページで [**インテリジェントチャネル**] フィルターを選択します。

{% alert important %}
SMS チャネルのエンゲージメント率を計算するには、高度なトラッキングとクリックトラッキングによる [SMS リンクの短縮]({{site.baseurl}}/user_guide/message_building_by_channel/sms/campaign/link_shortening/#overview/) を有効にします。
{% endalert %}

## 「データが足りない」オプション

Brazeがどのチャンネルが「最適」かを判断するには、十分なデータが必要です。つまり、ユーザーは、使用可能な 3 つのチャネルのうち少なくとも 2 つで、少なくとも 3 つ以上のメッセージを受信している必要があります。メッセージは、必ずしも開かれている必要はありません。 

ユーザーがチャネル全体で十分なメッセージを受信していない場合、それらのユーザーはこのフィルターの「データ不足」オプションに分類されます。これにより、使用可能な 3 つのメッセージング チャネルのいずれかを使用して、これらのユーザーをターゲットにすることができます。

例えば、プッシュメッセージを好むユーザーにはプッシュメッセージを受信し、データ量が足りないユーザーには同じプッシュメッセージを受け取るようにしたいとします。その場合は、インテリジェント チャネル フィルターを **[モバイル** ] に設定し、 **OR** を使用して 2 つ目のインテリジェント チャネル フィルターを **[データ不足**] に設定します。インテリジェント チャネル フィルターを電子メールに設定した別のキャンペーンは、電子メールを好むユーザーに対応できます。

![][2]

{% alert note %}
[フリークエンシー キャップ]({{site.baseurl}}/user_guide/engagement_tools/campaigns/testing_and_more/rate-limiting/#delivery-rules)を無視するキャンペーンとキャンバス ステップは、インテリジェント チャネルでは考慮されず、データ要件に寄与できません。
{% endalert %}

## 「モバイルプッシュ」オプション

モバイルプッシュには、Android、iOS、Kindle、およびBrazeで利用可能なその他のモバイルデバイスチャネルが組み込まれています。インテリジェントチャネルを計算する際、Brazeは各種類のモバイルデバイスを個別に調べ、メールやWebプッシュと比較した場合に「モバイルプッシュ」カテゴリを表すために、その中から最も高いエンゲージメント率を選択します。 

たとえば、ユーザーが複数のモバイルデバイスを持っている場合、そのユーザーのモバイルエンゲージメント率は、デバイス全体で最も高い割合で表されます。ただし、これにより、ユーザーはそのデバイスでのみプッシュ通知を受信するように強制されません。このレートは、メールやウェブプッシュとレートを比較する場合にのみ使用されます。

## ベストプラクティスと効果的な使用戦略

### タイブレーク

一部のユーザーは受信したメッセージの数が少ないため、特定のユーザーの利用可能なチャネル全体でエンゲージメント率に同点があることは珍しくありません(たとえば、1人のユーザーのメールとモバイルプッシュ **の両方で** エンゲージメント率が0.2)。このような場合、最新のオープンイベントがあるチャンネルを優先する(より高いランキングを与える)ことで、同点が解消されます。

### 到達不能なチャネル

ユーザーがランキングを決定するのに十分なデータを持っているのに、最もエンゲージメントの高いチャネルで到達できなくなった場合、ユーザーは「脱落」し、メッセージを受け取らなくなります。特定のチャネルでリーチできないユーザーは、個別にターゲットにする必要があります。

### オーディエンスのサイジング

インテリジェント チャネルを使用すると、他のオーディエンスよりもメッセージに関与する可能性がはるかに高いユーザーの割合を事前に選択的にターゲットにすることができます。これは、一般的なオーディエンスのユーザーの過半数を表す可能性は低いです。むしろ、このフィルターは、特定のチャンネルでのエンゲージメントの確立された記録を持つ通常の視聴者から5〜20%を見つけることが期待できます。


[1]: {% image_buster /assets/img/intelligent_channel_filter.png %} 「インテリジェント・チャンネル・フィルタ」
[2]: {% image_buster /assets/img/intelligent_example.png %}