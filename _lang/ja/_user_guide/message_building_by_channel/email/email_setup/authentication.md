---
nav_title: メール認証
article_title: メール認証
page_order: 2
page_type: reference
description: "このリファレンス記事では、メールの送信元に関する検証可能な情報をメールに装備することを目的とした一連の手法であるメール認証について説明します。"
channel: email

---

# メール認証

> 電子メール認証は、電子メールの発信元に関する検証可能な情報を電子メールに提供する技術の集合体です。<br><br>インターネットサービスプロバイダー(ISP)があなたを望ましい電子メールの送信者として認識し、メールをすぐに配信するためには、適切な認証が不可欠です。認証を行わないと、アウトリーチは不正であると推定されます。 

## 認証の方法

### 送信者ポリシーフレームワーク(SPF)

この方法では、Brazeのメール送信IPアドレスが、お客様に代わってメールを送信する権限を持っていることを確認します。SPFは基本認証であり、DNS設定でテキストレコードを公開することで実現されます。受信サーバーはDNSレコードをチェックし、それらが本物かどうかを判断します。このメソッドは、電子メール送信者を検証するように設計されています。

SPFレコードは、BrazeがIPとドメインを設定する際に設定され、DNSレコードを追加する以外に、それ以上のアクションは必要ありません。

### ドメインキー識別メール(DKIM)

この方法では、Brazeのメール送信ドメインがユーザーに代わってメールを送信する権限を持っていることを確認します。このメソッドは、送信者の信頼性を検証し、メッセージの整合性が保持されていることを検証できるように設計されています。また、個別の暗号化デジタル署名を使用するため、ISPは配信するメールが送信したメールと同じであることを確認できます。

Brazeは秘密鍵でメールに署名します。ISPは、カスタムDNSレコードに保存されている公開鍵と照合して署名を検証します。まったく同じ署名は 2 つとなく、秘密鍵の署名を正常に検証できるのは公開鍵だけです。

DKIMレコードは、BrazeがIPとドメインを設定する際に設定され、DNSレコードを追加する以外に、それ以上のアクションは必要ありません。

### DMARC(Domain-based Message Authentication, Reporting, and Conformance) (ドメインベースのメッセージ認証、レポート、および準拠)

[DMARC(Domain-based Message Authentication, Reporting & Conformance)は、](https://dmarc.org/) メール送信者が自分のメールの正当性を証明するためのメール認証プロトコルであり、メールボックスの受信者の信頼を可能にし、メールの受け入れを促進します。DMARCでは、メール送信者は、SPF(Sender Policy Framework)やDKIM(Domain Keys Identified Mail)を使用して認証されなかったメールの処理方法を指定することができます。これは、SPFとDKIMの両方のチェックに合格していることを確認することで実現されます。 

送信者は、署名または認証チェックに失敗したメールをどのように処理するかをメールボックスプロバイダーに指示できます。失敗は、他の人があなたやあなたのメールを模倣しようとしていることを示している可能性があります。送信者は、メールボックスプロバイダーにメールを拒否または隔離するように指示したり、チェックに失敗したメールに関する自動レポートを送信したりすることもできます。そうすることで、メールボックスプロバイダーは、スパム送信者をより適切に特定し、悪意のある電子メールが受信トレイに侵入するのを防ぐと同時に、誤検知を最小限に抑え、より優れた認証レポートを提供して市場の透明性を高めることができます。

#### 仕組み

DMARCを導入するには、DMARCレコードをドメインネームシステム(DNS)に公開する必要があります。これは、SPFとDKIMのステータスを確認した後、メールドメインのポリシーを公に表現するTXTレコードです。DMARCは、SPFまたはDKIMのいずれか、または両方に合格した場合に認証されます。これはDMARCアライメントと呼ばれます。

また、DMARCレコードは、DMARCレコードに記載されているレポートメールアドレスにXMLレポートを送り返すようにメールサーバーに指示します。これらのレポートは、メールがエコシステム内をどのように移動しているかについての洞察を提供し、メールドメインを使用してメール通信を送信しようとしているすべてのものを特定できるようにします。

DMARCレコードのポリシーは、SPFとDKIMを通過せず、あなたのドメインからのものであると主張するメールをどう処理するかを、参加している受信者のメールサーバーに指示します。Brazeは、ルートドメインにDMARCポリシーを設定し、すべてのサブドメインに適用することを推奨しています。これは、将来、現在および新しいサブドメインで追加の設定が必要になることを意味します。設定できるポリシーには、次の 3 種類があります。

|方針 |想定される影響 |
| --- | --- |
|なし |メールボックス プロバイダーに、失敗したメッセージに対してアクションを実行しないように指示します。|
|検疫 |メールボックス プロバイダーに、失敗したメッセージをスパム フォルダーに送信するように指示します。|
|却下 |失敗したメッセージはスパム フォルダーに振り分けられ、ブロックする必要があることをメールボックス プロバイダーに伝えます。|
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

#### ドメインのDMARC認証を確認する方法

ドメインのDMARC認証を確認するには、2つの方法があります。

* **オプション 1: **[MXToolbox](https://mxtoolbox.com/dmarc.aspx)などのサードパーティのDMARCチェッカーに親ドメインまたはサブドメインを入力して、DMARCポリシーが設定されているかどうか、およびそのポリシーが何に設定されているかを監査できます。
* **オプション 2: **メールボックス内のドメインまたはサブドメインからのメールを開き、元のメッセージを見つけて、DMARCがこのメールで認証に合格しているかどうかを確認します。

たとえば、Gmail を使用している場合は、次の手順を行います。

1. 電子メール メッセージの **[その他**<i class="fa-solid fa-ellipsis"></i>] をクリックします。
2. [ **オリジナルを表示**] を選択します。
3. **DMARC**のステータスが「PASS」になっているか確認してください。

![An email that has "PASS" as the DMARC value.]({% image_buster /assets/img_archive/dmarc_example.png %})
