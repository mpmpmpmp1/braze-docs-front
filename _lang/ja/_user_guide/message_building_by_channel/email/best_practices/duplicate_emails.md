---
nav_title: メールの重複
article_title: メールの重複
page_order: 7
page_type: reference
description: "この記事では、重複メールを管理するためのベストプラクティスを紹介する。"
channel: email

---

# メールの重複

> 重複メールについては、あるメールが配信停止になった場合、そのメールアドレスを持つ他のプロファイル（最大100プロファイル）が更新され、同じ購読状態が反映される。これは、配信停止や、グローバルメール購読状態や個々の購読グループの状態のような、購読状態のその他の変更に適用される。

## 電子メール購読の更新

Brazeは、Eメールキャンペーンを送信する際に、重複するEメールアドレスを自動的にチェックし、削除する。この方法では、メールは一度しか送信されず、複数のユーザー・プロファイルが共通のアドレスを共有していても、同じメールが何度もヒットしないようにチェックする「重複排除」が行われる。

{% alert tip %}
[ユーザーのメール購読を管理]({{site.baseurl}}/user_guide/message_building_by_channel/email/managing_user_subscriptions/#managing-user-subscriptions)し、特定の購読状態のユーザーをターゲットにしたキャンペーンを行うためにBrazeが提供するツールに精通していることを確認する。これらのツールは、[反スパム法を]({{site.baseurl}}/help/best_practices/spam_regulations/#spam-regulations)遵守するために不可欠である。
{% endalert %}

ユーザーがメールアドレスを共有している場合、これらのユーザーの1人を更新すると、これらのユーザー（最大100ユーザー）にサブスクリプションの変更が伝搬される。

## メッセージ送信の動作

重複排除は、ターゲットユーザーが同じディスパッチに含まれるときに発生するため、トリガーキャンペーン（APIトリガーキャンペーンを除く）やCanvasesでは、一致するEメールを持つ異なるユーザーが異なる時間にトリガーイベントを記録した場合、同じEメールアドレスに複数のディスパッチが発生する可能性がある。

## 例

例えば、ユーザーAとユーザーBがEメール`johndoe@example.com` を共有しているが、プロフィールが異なるタイムゾーンにある場合、キャンペーントリガーイベントにユーザーのタイムゾーンでの送信が含まれていると、Eメール`johndoe@example.com` は2通のEメールを受信することになる。

ユーザーAのEメールアドレスを、既存のユーザーBと共有する別のEメールアドレスに設定または更新した場合、**Eメールを更新したときにユーザーを再登録する**設定がオンになっていない限り、ユーザーAはすでに存在するユーザーBの購読状態を継承する。

{% alert important %}
APIコールでAPIキャンペーンを送信する場合（APIトリガーキャンペーンを除く）、セグメントオーディエンスに同じメールアドレスを持つ複数のユーザーが指定されている場合、コールでリストされた回数だけそのアドレスに送信する。これは、APIコールが意図的に作られたものだと仮定しているからだ。
<br><br>
**API トリガーキャンペーン**<br>
APIトリガーキャンペーンは、オーディエンスが定義されている場所によって、重複排除または重複送信を行うことに注意しよう。<br>\- 対象セグメント内に重複メールがある場合、またはAPIトリガー呼び出しの[受信者フィールド]({{site.baseurl}}/api/endpoints/messaging/send_messages/post_send_triggered_campaigns/)内に重複IDがあるために重複メールがある場合、デデューピングが発生する可能性がある。<br>\- APIトリガー呼び出しの受信者フィールド内で別々のユーザーIDを直接ターゲットにした場合、メールの重複が発生する。
{% endalert %}