---
nav_title: カスタムイベント
article_title: カスタムイベント
page_order: 9
page_type: reference
description: "このリファレンス記事では、カスタムイベントとプロパティ、セグメンテーション、使用方法、キャンバスエントリのプロパティ、関連する分析が表示される場所などについて説明します。"
search_rank: 2
---

# [![Brazeラーニングコース]({% image_buster /assets/img/bl_icon3.png %})](https://learning.braze.com/custom-events-and-attributes){: style="float:right;width:120px;border:0;" class="noimgborder"}カスタムイベント

> この記事では、カスタムイベントとプロパティ、セグメンテーション、使用法、キャンバスエントリのプロパティ、関連する分析が表示される場所などについて説明します。Braze のイベントの詳細については、「[イベント]({{site.baseurl}}/user_guide/data_and_analytics/custom_data/events)」を参照してください。

## 概要

カスタムイベントとは、ユーザーによって実行されたアクションまたはユーザーに関する更新です。アプリケーション内での高価値のユーザーインタラクションの追跡に最適です。カスタムイベントをログに記録すると、任意の数およびタイプのフォローアップキャンペーンをトリガーでき、そのイベントの新近度と頻度についてリストされたセグメンテーションフィルターが有効になります。

### ユースケース

一般的なカスタムイベントのユースケースをいくつか示します。
- [アクションベースの配信を]({{site.baseurl}}/user_guide/engagement_tools/campaigns/building_campaigns/delivery_types/triggered_delivery/)使用して、カスタムイベントに基づいてキャンペーンまたはキャンバスをトリガーする。
- カスタムイベントを何回実行したか、最後にイベントが発生したのはいつか、などでユーザーをセグメントする。
- ダッシュボードの[カスタムイベント分析を使って]({{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_events#custom-event-analytics)、各イベントの発生頻度の集計を表示する。
- [ファネルと]({{site.baseurl}}/user_guide/data_and_analytics/reporting/funnel_reports/#step-2-select-events-for-funnel-steps) [リテンションレポートを]({{site.baseurl}}/user_guide/data_and_analytics/reporting/retention_reports/)使用して、追加の分析を見つける。
- [永続エントリのプロパティを]({{site.baseurl}}/user_guide/engagement_tools/canvas/create_a_canvas/canvas_persistent_entry_properties/)活用して、顧客イベントのメタデータをキャンバスのステップでパーソナライゼーションに使用する。
- [Currentsで]({{site.baseurl}}/user_guide/data_and_analytics/braze_currents)より高度な分析を行う。
- キャンバスの[例外イベントを]({{site.baseurl}}/user_guide/engagement_tools/canvas/create_a_canvas/exception_events#canvas-exception-events)設定して、ユーザーがキャンバスの次のステップに進むべきでないタイミングを定義する。

### カスタムイベントの管理

ダッシュボードでカスタムイベントの作成や管理を行うには、\[**データ設定**] > \[**カスタムイベント**] に移動します。

{% alert note %}
[古いナビゲーション]({{site.baseurl}}/navigation)を使用している場合、\[**カスタムイベント**] は \[**設定の管理**] の下にあります。
{% endalert %}

このページでは、既存のカスタムイベントの表示、管理、作成、または禁止リストへの追加ができます。カスタムイベントの横にあるメニューを選択し、以下のアクションを実行する：

#### ブロックリスト

カスタムイベントは、アクションメニューから個別に禁止リストに追加することも、最大 10 件のイベントを選択して一括登録することもできます。あるカスタムイベントを禁止した場合、そのイベントに関するデータは収集されず、再アクティブ化しない限り既存のデータが利用できなくなります。また、禁止リストに追加されたイベントはフィルターやグラフに表示されません。さらに、イベントが現在 Braze ダッシュボードの他の領域にあるフィルターまたはトリガーから参照されている場合、それを参照しているフィルターまたはトリガーのすべてのインスタンスが削除されてアーカイブされることを説明する警告モーダルが表示されます。

#### 説明を加える

`Manage Events, Attributes, Purchases` [ユーザー権限を持って]({{site.baseurl}}/user_guide/administrative/app_settings/manage_your_braze_users/user_permissions/)いれば、作成後にカスタムイベントに説明を追加することができる。カスタムイベントの**説明を編集を**選択し、チームへのメモなど好きなものを入力する。

### タグを追加する

`Manage Events, Attributes, Purchases` [・ユーザー権限を持って]({{site.baseurl}}/user_guide/administrative/app_settings/manage_your_braze_users/user_permissions/)いれば、作成後にカスタム・イベントにタグを追加することができる。タグは、イベントのリストをフィルタリングするために使用することができる。(この機能は現在早期アクセス中である）。この早期アクセスへの参加に興味がある場合は、カスタマー・サクセス・マネージャーに連絡すること)。

#### 利用レポートを見る

使用状況レポートは、特定のカスタムイベントを使用しているすべてのキャンバス、キャンペーン、およびセグメントを一覧表示する。このリストにはリキッドの用途は含まれていない。 

各カスタムイベントの横にあるチェックボックスを選択し、**View usage reportを**選択することで、一度に10件までの使用レポートを見ることができる。

### データをエクスポートする ###

カスタム・イベントのリストをCSVファイルとしてエクスポートするには、ページ上部の「Export all」ボタンをクリックする。CSVファイルが生成され、ダウンロードリンクがEメールで送信される。(この機能は現在、早期アクセス版として提供されている）。この早期アクセスへの参加に興味がある場合は、カスタマー・サクセス・マネージャーに連絡すること)。

### カスタムイベントのログ記録

カスタムイベントには追加の設定が必要です。以下に、さまざまなプラットフォームでカスタムイベントのログ記録に使用される方法を示します。これらのページには、カスタムイベントにプロパティと数量を追加する方法に関するドキュメントもあります。

{% details プラットフォーム別にドキュメントを拡張する %}

- [Android と FireOS]({{site.baseurl}}/developer_guide/platform_integration_guides/android/analytics/tracking_custom_events/)
- [iOS]({{site.baseurl}}/developer_guide/platform_integration_guides/swift/analytics/tracking_custom_events/)
- [Web]({{site.baseurl}}/developer_guide/platform_integration_guides/web/analytics/tracking_custom_events/)
- [React Native]({{site.baseurl}}/developer_guide/platform_integration_guides/react_native/analytics/#logging-custom-events)
- [Unity]({{site.baseurl}}/developer_guide/platform_integration_guides/unity/Analytics/logging_custom_events/)
- [Xamarin]({{site.baseurl}}/developer_guide/platform_integration_guides/xamarin/analytics/#tracking-custom-events)
- [Roku]({{site.baseurl}}/developer_guide/platform_integration_guides/roku/analytics/logging_custom_events/)

{% enddetails %}

### カスタムイベントの保存

カスタムイベントのメタデータ (最初 / 最後の発生日時、合計数、30 日間にわたる Y の X) を含む、**ユーザープロファイル**に保存されているすべてのデータは、各プロファイルが[アクティブ]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/user_archival/#active-users)である限り無期限に保持されます。

## セグメンテーションフィルター

次の表に、ユーザーのカスタムイベント別セグメンテーションに使用できるフィルターを示します。

| セグメンテーション・オプション | ドロップダウン・フィルター | 入力オプション |
| ---------------------| --------------- | ------------- |
| カスタムイベントが**X回以上**発生したかどうかをチェックする | **より大きい** | **数値** |
| カスタムイベントの発生**回数がX回未満か**どうかをチェックする | **未満** | **数値** |
| カスタムイベントが**正確にX回**発生したかどうかをチェックする | **その通りだ。** | **数値** |
| カスタムイベントが**X日以降に**発生したかどうかをチェックする | **導入後** | **時間** |
| カスタムイベントが**X日以前に**発生したかどうかをチェックする | **ビフォア** | **時間** |
| カスタムイベントが最後に発生したのが**X日以上前か**どうかをチェックする | **以上** | **過去の日数**（正の数） |
| カスタムイベントが最後に発生したのが**X日以内か**どうかをチェックする | **未満** | **過去の日数**（正の数） |
| カスタムイベントが**X(Max = 50)回以上**発生したかどうかをチェックする。 | **以上** | 過去**Y日間 (Y = 1,3,7,14,21,30)** |
| カスタムイベントの発生**回数がX（Max = 50）回未満か**どうかをチェックする。 | **未満** | 過去**Y日間 (Y = 1,3,7,14,21,30)** |
| カスタムイベントが**正確にX（最大50）回**発生したかどうかをチェックする。 | **その通りだ。** | 過去**Y日間 (Y = 1,3,7,14,21,30)** |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}

## 分析

Braze はセグメンテーション用として、これらのイベントが発生した回数と、各ユーザーの最終実行時刻を記録します。これらの分析は、\[**分析**] > \[**カスタムイベントレポート**] で確認できます。

{% alert note %}
[古いナビゲーション]({{site.baseurl}}/navigation)を使用している場合、\[**カスタムイベントレポート**] は \[**データ**] の下にあります。
{% endalert %}

ダッシュボードの **カスタムイベントレポート** ページでは、各カスタムイベントの発生頻度を集計したり、セグメント別に表示したりして、より詳細な分析ができます。キャンペーンがカスタムイベントのアクティビティにどのように影響したかを確認する場合に、Braze が時系列に重ねて表示するため、キャンペーンの最終送信時刻を示す灰色の線を調べると特に役立ちます。

![ダッシュボードのカスタム・イベント・ページにカスタム・イベントのカウント・グラフが表示され、カスタム・イベントのトレンドが示される。][8]

**フィルター**を使用して、カスタムイベントを時間、月間平均ユーザー数 (MAU)、セグメント、または KPI 式別に分類することもできます。 

![カスタム・イベント・グラフ・フィルター][9]{: style="max-width:40%;"}

{% alert tip %}
[カスタム属性を増やすと]({{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_attributes/#integers)、カスタムイベントと同様にユーザーアクションのカウンターを保持できます。ただし、カスタム属性データを時系列で表示することはできません。時系列で分析する必要のないユーザーアクションは、この方法を使用して記録する必要があります。
{% endalert %}

### カスタムイベント分析が表示されない

カスタムイベントデータを使用して作成されたセグメントでは、作成前の履歴データを表示できません。

## カスタムイベントプロパティ

カスタムイベントプロパティは、イベントの特定の発生を表すカスタムイベントのメタデータまたは属性です。したがって、これらのプロパティを使用して、トリガー条件の絞り込み、メッセージングのパーソナライゼーションの強化、コンバージョンの追跡、未加工データのエクスポートによるより高度な分析の生成ができます。

カスタムイベントプロパティは Braze のプロファイルに保存されないため、データポイントを消費しません (例外については以下の「[データポイント](#data-points)」を参照)。

{% alert important %}
各カスタムイベントまたは購入には、最大 256 個の異なるカスタムイベントプロパティを設定できます。256 個を超えるプロパティを持つカスタムイベントまたは購入がログ記録された場合、最初の 256 個のみが取得されて使用できます。
{% endalert %}

### 必要なフォーマット

プロパティ値は、キーがプロパティ名、値がプロパティ値であるオブジェクトでなければなりません。プロパティ名は、255 文字以下の空でない文字列でなければならず、先頭にドル記号 (`$`) は使用できません。

プロパティ値は、次のデータ型のいずれでもかまいません。

| データ型 | 説明 |
| --- | --- |
| 数値 | [整数](https://en.wikipedia.org/wiki/Integer)または[浮動小数点数として](https://en.wikipedia.org/wiki/Floating-point_arithmetic) |
| ブール値 | |
| 日付 | [ISO-8601](https://en.wikipedia.org/wiki/ISO_8601)または`yyyy-MM-dd'T'HH:mm:ss:SSSZ` 形式の文字列としてフォーマットされる。アレイ内ではサポートされていない。 |
| 文字列 | 255文字以下とする。 |
| 配列 | 配列に日時を含めることはできない。 |
| オブジェクト | オブジェクトは文字列として取り込まれる。 |
| ネストされたオブジェクト | 他のオブジェクトの中にあるオブジェクト。詳細については、この記事の「[階層化オブジェクト](#nested-objects)」のセクションを参照してください。
{: .reset-td-br-1 .reset-td-br-2}

配列またはオブジェクト値を含むイベントプロパティオブジェクトには、最大 50 KB のイベントプロパティペイロードを設定できます。

カスタムイベントプロパティのデータ型は変更できますが、データの収集後に[データ型を変更]({{site.baseurl}}/help/help_articles/data/change_custom_data_type/)した場合の影響に注意してください。

### カスタムイベントプロパティの使用

カスタムイベントプロパティを使用して、キャンペーントリガーの絞り込み、コンバージョンの追跡、メッセージングのパーソナライぜーションができます。

#### トリガーメッセージ

特定のキャンペーンまたはキャンバスのオーディエンスをさらに絞り込むには、カスタムイベントプロパティを使用します。例えば、e コマースアプリケーションがあり、ユーザーがカートを放棄したときにメッセージを送信する場合、カスタムイベントプロパティ `cart value` を追加することで、ターゲットオーディエンスをさらに絞り込んで、キャンペーンのパーソナライゼーションを向上できます。

![放置カードのカスタムイベントプロパティフィルタ。2つのフィルターをAND演算子で組み合わせ、カート金額が100ドルから200ドルの間にあるカードを放棄したユーザーにこのキャンペーンを送信する。][16]

ネストされたカスタムイベント・プロパティは、\[アクションベース配信][19] でもサポートされている。

![放置カードのカスタムイベントプロパティフィルタ。カートの中に100ドル以上の商品がある場合、1つのフィルターが選択される。][20]

#### メッセージのパーソナライゼーション

カスタムイベントプロパティは、メッセージングテンプレート内でパーソナライゼーションに使用することもできます。トリガーイベントを持つ\[アクションベースの配信][19] ]を使用するすべてのキャンペーンは、メッセージングパーソナライゼーションのために、そのイベントからカスタムイベントプロパティを使用することができる。

例えば、ゲームアプリケーションで、あるレベルをクリアしたユーザーにメッセージを送信する場合、ユーザーがそのレベルを完了するまでに要した時間のプロパティを使用して、メッセージをさらにパーソナライズできます。この例では、\[条件付きロジック][18]]を使って、3つの異なるセグメントに対してメッセージをパーソナライズしている。カスタムイベントプロパティ `time_spent` は、``{% raw %} {{event_properties.${time_spent}}} {% endraw %}`` を呼び出すことでメッセージに含めることができます。

{% alert warning %}
ユーザーがインターネットに接続していない場合、テンプレート化されたカスタムイベントプロパティ ({% raw %}、``{{event_properties.${time_spent}}}``、{% endraw %} など) を使用してトリガーされたアプリ内メッセージは失敗し、表示されません。
{% endalert %}

アプリ内メッセージがテンプレート化されたアプリ内メッセージとして配信されるリキッドタグの完全なリストについては、[よくある質問を]({{site.baseurl}}/user_guide/message_building_by_channel/in-app_messages/faq/#what-are-templated-in-app-messages/)参照のこと。

##### フィルターに関する考慮事項

- **API 呼び出し:**API 呼び出しを行い、かつ「空白」フィルターを使用する場合、呼び出しから除外されたカスタムイベントプロパティは「空白」と見なされます。例えば、`"event_property": ""` を含めた場合、ユーザーは「空白でない」と見なされます。
- **整数:**数値のカスタムイベントプロパティにフィルターを適用するときに、値が非常に大きい場合は、「完全一致」フィルターを使用しないでください。数値が大きすぎると特定の長さに丸められ、フィルターが意図どおりに機能しないことがあります。

#### セグメンテーション

イベントプロパティのセグメンテーションにより、取得したカスタムイベントとそれらのイベントに関連するプロパティに基づいて、ターゲットユーザーを絞り込むことができます。この機能により、購入イベントとカスタムイベントをセグメント化するときのフィルターオプションがさらに追加されます。

カスタムイベントのイベントプロパティは、それを使用するすべてのセグメントでリアルタイムに更新されます。プロパティを管理するには、\[**データ設定**] > \[**カスタムイベント**] ページでカスタムイベントの \[**プロパティの管理**] をクリックします。特定のセグメントフィルターで使用されるカスタムイベントプロパティの最大遡及履歴は 30 日間です。

{% alert note %}
イベントプロパティの新近性と頻度に基づいてセグメントを作成したい場合は、特定のカスタムイベントプロパティのセグメンテーションを有効にするように、カスタマーサクセスマネージャーに依頼してください。有効にすると、セグメンテーション時に追加のフィルターオプションにアクセスできます。
{% endalert %}

これらのセグメンテーションフィルターには次のようなものがあります。

- 過去 Y 日間に、値 B のプロパティ A を持つカスタムイベントを X 回実行した。
- 過去 Y 日間に、値 B のプロパティ A を持ついずれかの購入を行った。
- 1、3、7、14、21、30 日以内に、セグメントに加えられる条件を満たした。

![][3]

特定のイベントプロパティのデータは、カスタマーサクセスマネージャーによって有効にされた後にのみ記録されます。イベントプロパティは、その日付以降にのみ利用可能です。

##### データポイント

サブスクリプションの使用に関して、以下のフィルターでのセグメンテーション用に有効になっているカスタムイベントプロパティは、カスタムイベント自体でカウントされるデータポイントに加えて、すべて個別のデータポイントとしてカウントされます。

- `X Custom Event Property in Y Days`
- `X Purchase Property in Y Days`

### キャンバスエントリのプロパティとイベントプロパティ

キャンバスのユーザージャーニーで `canvas_entry_properties` と `event_properties` を活用できます。詳細と例については、「[キャンバスエントリのプロパティとイベントプロパティ]({{site.baseurl}}/user_guide/engagement_tools/canvas/create_a_canvas/canvas_entry_properties_event_properties/)」を参照してください。

{% tabs local %}
{% tab キャンバス・エントリーのプロパティ %}

[キャンバスエントリのプロパティ]({{site.baseurl}}/api/objects_filters/canvas_entry_properties_object/)は、アクションベースまたは API でトリガーされるキャンバスにマップするプロパティです。`canvas_entry_properties` オブジェクトのサイズ上限は 50 KB であることに注意してください。

{% alert note %}
特にアプリ内メッセージチャネルでは、以前の早期アクセスの一環として元のエディターで永続的なエントリプロパティを有効にしている場合、キャンバスフローと元のキャンバスエディターでのみ `canvas_entry_properties` を参照できます。
{% endalert %}

キャンバスフローメッセージングでは、いずれのメッセージステップでも `canvas_entry_properties` を Liquid で使用できます。これらのプロパティを参照するときには、``{% raw %} canvas_entry_properties.${property_name} {% endraw %}`` の Liquid を使用してください。このように使用するには、イベントがカスタムイベントまたは購入イベントでなければならないことに注意してください。 

#### ユースケース

{% raw %}
小売店であるRetailAppに対する次のようなリクエストを考えてみよう：`\"canvas_entry_properties\" : {\"product_name\" : \"shoes\", \"product_price\" : 79.99}`.リキッド`{{canvas_entry_properties.${product_name}}}` を使えば、メッセージに「靴」という言葉を加えることができる。
{% endraw %}

RetailAppは、ユーザーが購入イベントをトリガーした後、キャンバス内の異なる`product_name` プロパティに対して特定のメッセージをトリガーして送信することもできる。例えば、Messageステップに以下のLiquidを追加することで、靴を購入したユーザーとそれ以外のものを購入したユーザーに異なるメッセージを送ることができる。

{% raw %}
```markdown
{% if  {{canvas_entry_properties.${product_name}}} == "shoes" %}
  Your order is set to ship soon. While you're waiting, why not step up your shoe care routine with a little upgrade? Check out our selection of shoelaces and premium shoe polish.
{% else %}
  Your order will be on its way shortly. If you missed something, you have until the end of the week to add any additional items to your cart and enjoy storewide discounts. 
{% endif %}

```
{% endraw %}

{% details オリジナル・キャンバス・エディターの拡張 %}

2023 年 2 月 28 日以降、元のエディターを使用したキャンバスの作成や複製はできなくなりました。このセクションは参照のみを目的としています。

元のエディターで作成されたキャンバスの場合、`canvas_entry_properties` はキャンバスの最初のフルステップでのみ参照できます。

{% enddetails %}
{% endtab %}

{% tab イベントのプロパティ %}

{% alert important %}
`event_properties` は先頭のメッセージステップで使用できません。代わりに、`canvas_entry_properties` を使用するか、`event_properties` を含むメッセージステップの**前**に、対応するイベントを含むアクションパスを追加する必要があります。
{% endalert %}

イベントプロパティとは、カスタムイベントと購入に設定したプロパティを指します。これらの `event_properties` は、アクションベースの配信やキャンバスを含むキャンペーンで使用できます。

キャンバスフローでは、カスタムイベントと購入イベントのプロパティを、アクションパスステップに続く任意のメッセージステップで Liquid で使用できます。これらの `event_properties` を参照する場合は、必ず{% raw %} ``{{event_properties.${property_name}}}``{% endraw %} を使用してください。メッセージコンポーネントでこのように使用するには、これらのイベントがカスタムイベントまたは購入イベントである必要があります。

アクションパスに続く最初のメッセージステップでは、そのアクションパスで参照されるイベントに関連する `event_properties` を使用できます。これらの `event_properties` は、ユーザーが実際にアクションを実行した場合 (その他のユーザーグループに移動していない) にのみ使用できます。このアクションパスとメッセージステップの間に、他のステップ (別のアクションパスやメッセージステップではない) があってもかまいません。

{% details オリジナル・キャンバス・エディターの拡張 %}

2023 年 2 月 28 日以降、元のエディターを使用したキャンバスの作成や複製はできなくなりました。このセクションは参照のみを目的としています。

元のキャンバスエディターでは、スケジュールされたフルステップで `event_properties` を使用できません。ただし、アクションベースのキャンバスの最初のフルステップでは、フルステップがスケジュールされている場合でも `event_properties` を使用できます。

{% enddetails %}

{% endtab %}
{% endtabs %}

### 階層化オブジェクト {#nested-objects}

階層化オブジェクト (他のオブジェクト内にあるオブジェクト) を使用すると、カスタムイベントや購入のプロパティとして階層化された JSON データを送信できます。この階層化されたデータは、メッセージ内のパーソナライズされた情報のテンプレート作成、メッセージ送信のトリガー、およびセグメンテーションに使用できます。

詳細については、[階層化オブジェクト]({{site.baseurl}}/user_guide/data_and_analytics/custom_data/custom_events/nested_objects/)に関する記事を参照してください。

## カスタムイベントプロパティの保存

カスタムイベントプロパティは、ターゲティングの精度を高め、メッセージのパーソナライゼーションの印象を高めるように設計されています。カスタムイベントプロパティは、短期および長期のいずれでも Braze 内に保存できます。

イベントプロパティの値に基づいてセグメント化する場合、次の 2 つの方法があります。

1. **30 日以内:**Braze サポート担当者は、Braze のセグメント内にある特定のイベントプロパティ値の頻度と新近度に基づいて、イベントプロパティのセグメンテーションができます。セグメント内のイベントプロパティを活用したい場合は、Braze のアカウントエグゼクティブまたはカスタマーサクセスマネージャーにお問い合わせください。このオプションはデータ使用量に影響することに注意してください。<br><br>
2. **30 日以内およびそれ以降:**短期と長期の両方のイベントプロパティセグメンテーションに対応する目的で、[セグメントエクステンション]({{site.baseurl}}/user_guide/engagement_tools/segments/segment_extension/)を使用できます。この機能を使用すると、過去 2 年間に追跡されたカスタムイベントとイベントプロパティに基づくセグメンテーションができます。このオプションがデータ使用量に影響しないことに注意してください。

お客様の特定のニーズに応じた最適なアプローチの推奨事項については、Braze カスタマーサクセスマネージャーにお問い合わせください。


[1]: {% image_buster /assets/img/nested_object1.png %}
[2]: {% image_buster /assets/img/nested_object2.png %}
[3]: {% image_buster /assets/img/nested_object3.png %}
[4]: {% image_buster /assets/img_archive/nested_event_properties_segmentation.png %}
[5]: {% image_buster /assets/img_archive/nested_event_properties_personalization.png %}
[6]: {% image_buster /assets/img_archive/schema_generation_example.png %}
[8]: {% image_buster /assets/img_archive/custom_event_analytics_example.png %} "custom_event_analytics_example.png"
[9]: {% image_buster /assets/img/custom_events_report_filters.png %}
[16]: {% image_buster /assets/img_archive/customEventProperties.png %} "customEventProperties.png"
[18]: {{site.baseurl}}/user_guide/personalization_and_dynamic_content/liquid/conditional_logic/
[19]: {{site.baseurl}}/user_guide/engagement_tools/campaigns/scheduling_and_organizing/delivery_types/triggered_delivery/
[20]: {% image_buster /assets/img_archive/customEventPropertiesNested.png %} "customEventPropertiesNested.png"
