---
nav_title: SAMLジャストインタイムプロビジョニング
article_title: SAMLジャストインタイムプロビジョニング
page_order: 1
page_type: tutorial
description: "ここでは、SAML ジャストインタイムプロビジョニングを設定して、新しいダッシュボード ユーザー s が最初のサインインでBraze アカウントを作成できるようにする方法について説明します。" 

---

# SAMLジャストインタイムプロビジョニング 

> ジャストインタイムプロビジョニングは、[ SAML SSO]({{site.baseurl}}/user_guide/administrative/access_braze/single_sign_on/set_up/) で動作し、新しいダッシュボード ユーザーs が最初のサインイン時にBraze アカウントを作成できるようにします。これにより、管理者が新しいダッシュボード ユーザーのアカウントを手動で作成し、権限を選択してワークスペースに割り当て、アカウントの有効化を待機する必要がなくなります。

{% alert note %}
SAML ジャストインタイムプロビジョニングは、現在、アーリーアクセス中です。初期のアクセスに参加したい場合は、Braze 顧客のサクセスマネージャーにお問い合わせください。
{% endalert %}

## 前提条件

この機能を使用するには、SAML SSO がセットアップおよび統合されており、Google SSO と互換性がない必要があります。

## SAML ジャストインタイムプロビジョニングのセットアップ

Braze管理者に次の操作を依頼します。

1. **Settings** > **Security Settings**に移動します。
2. ** SAML SSO** セクションで、** 自動ユーザープロビジョニング** オプションを切り替えます。
3. デフォルト ワークスペースを選択して、新しいダッシュボード ユーザーを追加します。
4. 新しいダッシュボード ユーザーに割り当てるデフォルト権限セットを選択します。権限セットの作成方法については、[ユーザー権限の設定]({{site.baseurl}}/user_guide/administrative/app_settings/manage_your_braze_users/user_permissions/)を参照してください。
6. ページ下部の**変更の保存**を選択します
7. SSO プロバイダーの設定で、SSO プロバイダーのディレクトリーへのBraze接続が必要なすべてのユーザーを追加します。
8. これで、ユーザー s はサインアップまたはログインできます。