---
nav_title: 概要
article_title: ドラッグ&ドロップメールの作成
alias: "/dnd/overview/"
channel: email
page_order: 0
description: "この記事では、電子メール メッセージのドラッグ アンド ドロップ エディターを設定して適切に使用する方法について説明します。"
tool:
- Campaigns
- Canvas
---

# ドラッグ&ドロップメールの作成

> メール用のドラッグ&ドロップエディターを使用すると、HTMLを使用してメール本文を作成することなく、キャンペーンまたはキャンバス用に完全にカスタム化されたパーソナライズされたメールメッセージを作成できます。

メールメッセージをキャンペーンとキャンバスのどちらで送信すべきか迷っていますか?キャンペーンは単一のシンプルなメッセージングキャンペーンに適しており、キャンバスは複数ステップのユーザージャーニーに適しています。 

メッセージを作成する場所を選択したら、ドラッグ&ドロップメールを作成する手順を詳しく見ていきましょう。

## ステップ 1:テンプレートを選択する

編集エクスペリエンスとしてドラッグ アンド ドロップ エディターを選択した後、次のことを選択できます。
\- 空白のテンプレートから始めます。
\- Brazeのドラッグ&ドロップメールテンプレートを使用します。
\- 保存したドラッグ&ドロップのメールテンプレートを使用します。

{% alert note %}
既存のカスタム HTML テンプレートまたはサードパーティが作成したテンプレートを使用するには、[ **テンプレート** ] > **[メールテンプレート** ] に移動し、編集エクスペリエンスとして [ **ドラッグ アンド ドロップ エディター** ] を選択して、テンプレートを再作成する必要があります。
{% endalert %}

[ **テンプレート]** セクションからすべてのテンプレートにアクセスすることもできます。

{% alert note %}
[古いナビゲーション]({{site.baseurl}}/navigation)を使用している場合、テンプレートは **[テンプレートとメディア**] の下にあります。
{% endalert %}

テンプレートを選択すると、[ **メールバリアント** ]に送信情報とメール本文を含むメールの概要が表示されます。「 **メール本文を編集** 」をクリックして、ドラッグ&ドロップエディターでメール構造のデザインを開始します。 

![][8]

## ステップ 2:メールを作成する

ドラッグ アンド ドロップ編集エクスペリエンスは、次の 3 つのセクションに分かれています。**送信設定**、 **コンテンツ**、 **プレビューとテスト**。メール本文を作成する魔法は、[ **コンテンツ** ] セクションで行われます。メールを作成する前に、メール作成エクスペリエンスの指針となる主要なコンポーネントを理解することが重要です。

### ドラッグ&ドロップによるメールコンポーネント

ドラッグ アンド ドロップ エディターでは、 **コンテンツ** と **行** を 2 つの主要コンポーネントとして使用して、HTML を追加で使用することなくワークフローを簡素化します。

![][10]{: style="float:right;max-width:30%;margin-left:10px;"}
![][9]{: style="float:right;max-width:30%;margin-left:10px;"}

#### コンテンツ

**コンテンツ** には、メッセージで使用できるさまざまな種類のコンテンツを表す一連のタイルが含まれます。これらは、基本、メディア、高度な 3 つのカテゴリに分類されます。 

##### 基本ブロック

基本ブロックはメールの基本です。これらのブロックを使用して、次の要素のいずれかをメール本文に追加できます。
\- タイトル
\- 段落
-リスト
\- ボタン
\- 区切り線
\- 余白

##### メディアブロック

メディアブロックを使用すると、画像、動画、ソーシャルメディアのアイコンやリンク、カスタマイズ可能なアイコンなど、さまざまなビジュアルコンテンツを追加できます。

##### 高度なブロック

ドラッグ&ドロップエディターはこれらのブロックでワークフローを簡素化しますが、高度なブロックを使用してHTMLを挿入したり、メール本文にメニューを追加したりすることもできます。独自の HTML を使用すると、メッセージの表示方法に影響を与える可能性があることに注意してください。

#### \- 行

**行** は、列を使用してメッセージのセクションの水平方向の構成を定義する構造単位です。行または [コンテンツブロック]({{site.baseurl}}/user_guide/message_building_by_channel/email/drag_and_drop/dnd_content_blocks/)を空にすることができます。

複数の列を使用すると、異なるコンテンツ要素を並べて配置できます。これにより、開始時に選択したテンプレートに関係なく、必要なすべての構造要素をメッセージに追加できます。

これらの主要コンポーネントを確認したので、これらのブロックを使用してドラッグ&ドロップメールを作成しましょう。

1. [ **行** ] パネルを選択します。行の設定をメインエディタにドラッグ&ドロップします。これにより、メールコンテンツのレイアウトがマッピングされます。新しい構成は、既存のセクションの上部または下部にドラッグする必要があることに注意してください。
- 行構成を選択すると、[ **行のプロパティ** ] 設定が表示され、行の背景色、画像、およびカスタム列サイズをさらにカスタマイズできます。
2. [ **コンテンツ** ] パネルを選択します。目的のコンテンツタイルを行コンポーネントにドラッグ&ドロップします。
- また、任意の **コンテンツ** タイルをメインエディターにドラッグすることもできます。これにより、タイルの行が作成されます。
- タイルを選択し、[**コンテンツ プロパティ****] と [ブロック オプション**] のフィールドを調整することで、タイルをさらに絞り込むことができます。これには、文字の間隔、パディング、行の高さなどの編集が含まれます。

ドラッグ&ドロップメールをさらにカスタマイズする他の方法については、 [クリエイティブの詳細](#creative-details) をご覧ください。

Eメールを作成する際に、デスクトップビューとモバイルビューを切り替えて、Eメールメッセージがユーザーグループでどのように表示されるかをプレビューできます。これにより、コンテンツがレスポンシブであることが確認され、途中で必要な調整を行うことができます。

{% alert tip %}
素晴らしいコピーの作成にサポートが必要ですか?[AIコピーライティングアシスタント]({{site.baseurl}}/user_guide/intelligence/ai_copywriting/)を使ってみてください。製品名または説明を入力すると、AIがメッセージングで使用するための人間のようなマーケティングコピーを生成します。

![Copywriter button, located in the Content panel next to Style Settings in the drag-and-drop editor.]({% image_buster /assets/img/ai_copywriter/ai_copywriter_dnd.png %})
{% endalert %}

## ステップ 3:送信情報を追加する

メールメッセージのデザインと作成が完了したら、[ **送信設定** ]セクションに送信情報を追加します。

1. [ **送信情報**] で、[ **差出人表示名 + アドレス**] としてメールを選択します。また、[ **表示名 + アドレスからカスタマイズ**] を選択して、これをカスタマイズすることもできます。
2. **返信先アドレス**としてメールを選択します。また、「 **返信先アドレスのカスタマイズ**」を選択して、これをカスタマイズすることもできます。
3. 次に、 **BCCアドレス** としてメールを選択して、このアドレスにメールが表示されるようにします。
4. メールに件名を追加します。必要に応じて、プリヘッダーとプリヘッダーの後に空白を追加することもできます。

右側のパネルのプレビューに、追加した送信情報が入力されます。この情報は、[ **設定** ] > **[電子メール設定** ] > **[送信設定**] に移動して更新することもできます。

### 上級者 

**[送信設定**]で、メールヘッダーとメールエクストラのパーソナライゼーションを追加して、他のメールサービスプロバイダーに追加データを送り返すことができます。受信者の名前を含めるなど、メールヘッダーをパーソナライズすることも、メールが開封される可能性を高める可能性があります。

{% alert note %}
高度な機能は、キャンペーンまたはキャンバスコンポーザーに表示されます。高度な機能では、インライン CSS 設定を変更し、ヘッダーまたは追加のキーと値のペア(設定されている場合)を入力できます。
{% endalert %}

## ステップ 4: メールをテストする

送信情報を追加したら、いよいよメールをテストします。 

**[プレビューとテスト**] セクションに移動します。ここでは、ユーザーとしてメールをプレビューするか、テストメッセージを送信するかを選択できます。このセクションには [Inbox Vision]({{site.baseurl}}/user_guide/message_building_by_channel/email/inbox_vision/) も含まれており、さまざまなモバイルクライアントや Web クライアントで E メールが正しくレンダリングされたことを確認できます。

{% alert tip %}
また、プレビューパネルの **ダークモードプレビュー** トグルを使用して、メール本文をダークモードで表示し、必要に応じてメールを調整することもできます。
{% endalert %}

同じメールの 3 つの異なるバージョンを実際のエディター、Inbox Vision、および実際のテストメールとして表示できるため、すべてのプラットフォームで詳細を揃えることが重要です。

#### プレビューとテスト送信
 
[ **ユーザーとしてプレビュー]** タブでは、次のユーザー タイプを選択してメッセージをプレビューできます。

- **ランダムユーザー:**Brazeはデータベースからユーザーをランダムに選択し、その属性やイベント情報に基づいてメールをプレビューします。
- **ユーザーの選択:**メールアドレスまたは外部 ID に基づいて特定のユーザーを選択できます。メールは、そのユーザーの属性とイベント情報に基づいてプレビューされます
- **カスタムユーザー:**ユーザーをカスタマイズできます。Brazeは、利用可能なすべての属性とイベントの入力を提供します。プレビューメールに表示したい情報を入力できます。

{% alert note %}
ランダムなユーザーは、セグメンテーション条件に含まれる場合と含まれない場合があります。セグメンテーションは後から選択されるため、Brazeはこの時点ではターゲットオーディエンスを認識していません。
{% endalert %}

### Inbox Vision を使用する

Inbox Visionでは、メールクライアントとモバイルデバイスの観点からメールキャンペーンを表示できます。Inbox Vision を使用して電子メール メッセージをテストするには、[**Preview & Test**] セクションで **[Inbox Vision**] を選択し、[**Run Inbox Vision**] をクリックします。

{% alert tip %}
メールメッセージの背景画像は、画像間に白い線や断絶が表示される場合があるため、メールメッセージの詳細をテストして確認することが重要です。
{% endalert %}

ドラッグ&ドロップエディタを使用してメールメッセージをデザインして作成したら、キャンペーンまたはキャンバスの残りの部分を[ビルド][12]に進みます。

{% details About the updated HTML engine %}
ドラッグ アンド ドロップ エディターから HTML を生成する基盤となるエンジンが最適化および更新され、HTML ファイルの圧縮とレンダリングに関連する利点がもたらされました。

エクスポートされる HTML データの平均フットプリント サイズが削減され、読み込みとレンダリングが高速化され、モバイル クリッピングが削減され、帯域幅の消費が削減されました。

HTML レンダリングは、条件付きコメントと CSS メディアクエリの数を最小限に抑える次の更新に基づいて改善されました。その結果、HTML ファイルはサイズが小さくなり、より効率的にコーディングされます。
\- 要素ベースの設計から `<div>` 標準 `<table>` フォーマットのコードベースへの移行
\- [エディタブロック][7] は簡潔にするために再コーディングされました
\- 最終的なHTMLコードは、タグ間の空白を削除するために圧縮されます
\- 透明な仕切りは、自動的にコンテンツのパディングに変換されます
{% enddetails %}

## よりクリエイティブな詳細 {#creative-details}

ドラッグ&ドロップメールの作成を続けながら、これらのクリエイティブな詳細を組み合わせて使用することで、各メール本文をさらにカスタマイズし、メッセージに対するオーディエンスの注意と関心を引くことができます。

{% alert tip %}
ドラッグ&ドロップエディタのカスタムテーマは、 [グローバルスタイル設定]({{site.baseurl}}/user_guide/message_building_by_channel/email/drag_and_drop/dnd_email_style_settings/)を使用して作成できます。
{% endalert %}

### 画像の幅を自動調整

メールに追加された画像は、自動的に **[自動幅**] に設定されます。この設定を調整するには、[ **自動幅** ] をオフに切り替えて、必要に応じて幅のパーセンテージを調整します。

![ドラッグ&ドロップエディタの[コンテンツ]タブの[自動幅]オプション。[2]

### カラーレイヤリング

カラーレイヤーを使用すると、電子メールの背景、コンテンツ領域、およびさまざまなコンテンツコンポーネントの色を変更できます。前から後ろに色順は、コンテンツコンポーネントの色、コンテンツ領域の背景色、背景色です。

![ドラッグ&ドロップエディターでのカラーレイヤーの例][3]

### コンテンツのパディング

![ドラッグ&ドロップエディタのブロックオプション][4]{: style="float:right;max-width:25%;margin-left:15px;"}

パディングを調整するには、[ **ブロック オプション** ] まで下にスクロールし、[ **その他のオプション**] を選択します。パディングを微調整して、メールの見栄えを良くすることができます。

### コンテンツの背景

行設定に背景画像を追加して、より多くのデザインとビジュアルコンテンツをメールキャンペーンに組み込むことができます。

### 個人用設定を追加

![ドラッグ アンド ドロップ エディターの個人用設定を追加するためのオプション。[5]{: style="float:right;max-width:25%;margin-left:15px;"}

Basic Liquidは、ドラッグ&ドロップ式のメールエディターでサポートされています。Eメールにパーソナライゼーションを追加するには:

1. [**コンテンツ**] セクションの **[個人用設定**] を選択します。 
2. パーソナライゼーションの種類を選択します。これには、デフォルト(標準)属性、デバイス属性、カスタム属性などが含まれます。 
3. 追加する属性を検索します。
4. 生成されたLiquidスニペットをコピーして、メール本文のコンテンツブロックに貼り付けます。

リキッドパーソナライゼーションは、画像ブロックとボタンリンクタイプのフィールドではサポートされていません。 

#### ダイナミック イメージ

画像ソース属性に Liquid を含めることで、メール メッセージに動的画像を含めることができます。たとえば、静止画像の代わりに、画像 URL として挿入 {% raw %} `https://example.com/images/?imageBanner={{first_name}}` {% endraw %} して、画像にユーザーの名を含めることができます。これにより、各ユーザーに合わせてメールをパーソナライズできます。

### リンクに HTML 属性を追加する

![][6]{: style="float:right;max-width:35%;margin-left:15px;"}

ドラッグ&ドロップエディターでリンク、ボタン、画像、動画を使用する場合は、「**コンテンツ**」セクションの**「属性**」で**「新しい属性を追加**」を選択して、メールのHTMLタグに追加情報を追加します。これは、メッセージのパーソナライゼーション、セグメンテーション、およびスタイル設定に特に役立ちます。

一般的な使用例は、アンカータグに属性を挿入して、Braze経由で送信するときにクリックトラッキングを無効にすることです。

* **SendGridです。** `clicktracking = "off"`
* **スパークポスト:** `data-msys-clicktrack = "0"`

別の一般的な使用例は、特定のリンクにユニバーサルリンクとしてフラグを立てることです。ユニバーサル リンクは、アプリにリダイレクトするリンクであり、ユーザーに統合されたエクスペリエンスを提供します。

* **SendGridです。** `universal = "true"`
* **スパークポスト:** `data-msys-sublink = "open-in-app"` ( [カスタムサブパス](https://support.sparkpost.com/docs/tech-resources/deep-links-self-serve#custom-link-sub-paths) を設定する必要があります)

ユニバーサルリンクを設定するには、 [ユニバーサルリンクとアプリリンク]({{site.baseurl}}/help/help_articles/email/universal_links/)を参照してください。

または、 [Branch]({{site.baseurl}}/partners/message_orchestration/attribution/branch/branch_for_deeplinking/) や [AppsFlyer]({{site.baseurl}}/partners/message_orchestration/attribution/appsflyer/appsflyer/#email-deep-linking-and-click-tracking)などのアトリビューションパートナーと連携して、ユニバーサルリンクを管理することもできます。

[1]: {% image_buster /assets/img/dnd/dnd_template1.png %}
[2]: {% image_buster /assets/img/dnd/dnd1.png %}
[3]: {% image_buster /assets/img/dnd/dnd2.png %}
[4]: {% image_buster /assets/img/dnd/dnd3.png %}
[5]: {% image_buster /assets/img/dnd/dnd4.png %}
[6]: {% image_buster /assets/img/dnd_custom_attributes.png %}
[7]: {{site.baseurl}}/user_guide/message_building_by_channel/email/drag_and_drop/dnd_editor_blocks/
[8]: {% image_buster /assets/img/dnd/dnd_emailvariant.png %}
[9]: {% image_buster /assets/img/dnd/dnd_content.png %}
[10]: {% image_buster /assets/img/dnd/dnd_rows.png %}
[11]: {% image_buster /assets/img/dnd/dnd_contentsettings.png %}
[12]: {{site.baseurl}}/user_guide/message_building_by_channel/email/html_editor/creating_an_email_campaign/#step-4-build-the-remainder-of-your-campaign-or-canvas
[13]: {{site.baseurl}}/user_guide/message_building_by_channel/email/drag_and_drop/dnd_email_style_settings/
