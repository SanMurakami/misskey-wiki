---
title: /info
description: phpinfo?
published: true
date: 2021-12-19T17:03:26.029Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:46:08.271Z
---

**/info** とは、Misskey のステータス表示である。

明確な機能名が不明のため、**/info** とした。

# 概要
**misskey.domain/info** にアクセスすることで表示できる。

バージョン情報のほかに、使用サーバーのスペックやOSの構成、利用者数、投稿数、カスタム絵文字の設定詳細など、やたら事細かくリスト化で表示されるという **Misskey 鯖缶にとっては、えちな機能であろう！**

見た目が [phpinfo](https://www.google.com/search?q=phpinfo&tbm=isch) を思わせるようなデザインとなっている（これも、[syuilo](/ja/persons/syuilo)氏 の PHP愛なの？）。

あまりにも意識しすぎだったのか v12 からは右上のロゴが削除される変貌があるが、それ以外の変更は見られない（以下の画像参照）。

[misskey.io](/ja/instances/misskey_io) では、セキュアの事情で意図的に見せられないような設定にしている。

Misskey 派生でもおそらく見ることができる。

Misskey v12.96.0にて、Misskey Hub に埋め込むための情報ページ「/\_info\_card\_」に置き換わる形で**廃止**された。
/\_info\_card\_ では /info に比べ提供される情報は少ないが、代わりに従来の/info と同様の情報を提供するAPIエンドポイントが存在する（ただし重たい）。


# 画像

<!-- 画像アップロードできなくなったので、imgur 使うことにした。はよう直せ。 -->

## v11 以前
![https://i.imgur.com/dPeeseN.png](https://i.imgur.com/dPeeseN.png)

## v12
![https://i.imgur.com/bm0B5t7.png](https://i.imgur.com/bm0B5t7.png)
