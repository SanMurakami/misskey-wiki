---
title: フォロー
description: 
published: true
date: 2023-08-07T07:28:47.992Z
tags: 
editor: markdown
dateCreated: 2023-08-07T07:28:45.392Z
---

# フォロー

Misskeyではユーザーをフォローすることで、ホームタイムラインにフォローしたユーザーのノートを表示することができます。

# リモートフォロー

Misskeyでは、他のMisskeyサーバーや[Mastodon](../software/mastodon)サーバーなど、[ActivityPub](../software/activitypub)を使用しているサーバーのユーザーをフォローすることができます。

# 他のサーバーのユーザーをフォローする

ここでは2つの方法を紹介します。

## 方法その1

1, フォローしたいユーザーのIDを取得する

MisskeyやMastodonでは、ユーザーIDは`@<ユーザー名>@<サーバー名>`のような形であり、𝕏に比べて長いものになっています。

例えば、[Misskey.ioサポート](https://misskey.io/@support)は`@support@misskey.io`、[Mastodon公式アカウント](https://mastodon.social/@mastodon)は`@mastodon@mastodon.social`となります。

2, ユーザーのIDを照会する

ログインしているMisskeyを開き、ナビゲーションバーから「照会」を選択し、ユーザーIDを入力します。
> ほとんどの場合、「もっと！」の中に「照会」が含まれています{.is-info}

3, 表示されたページでユーザーをフォローする

照会に成功した場合はユーザーページが表示されます。

ユーザーページ右上の「フォロー」を選択することでユーザーをフォローすることができます。

## 方法その2

[方法その1](#方法その1)ではMisskeyの「照会」を使用しましたが、サーバーによっては「照会」が削除されている場合もあります。そのため、URLを直接操作してフォローする方法もあります。

1, フォローしたいユーザーのIDを取得する

2, ログインしているMisskeyのURLにユーザーIDを入力する

ブラウザでURLの入力欄を選択し、`https://<ログインしているMisskeyサーバー>/@<ユーザー名>@<サーバー名>`のように入力します。

例えば、*Misskey.io*から、*mastodon.social* の *@mastodon*をフォローしたい場合、`https://misskey.io/@mastodon@mastodon.social`のように入力します。

3, 表示されたページでユーザーをフォローする

ユーザーページ右上の「フォロー」を選択することでユーザーをフォローすることができます。