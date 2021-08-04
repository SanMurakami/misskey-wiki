---
title: よくある質問
description: 
published: true
date: 2021-08-04T04:21:02.110Z
tags: 
editor: markdown
dateCreated: 2020-09-19T17:30:57.943Z
---

# ホーム、ローカル、ソーシャル、グローバル 違いは？
**A. それぞれ、表示されるユーザーが違います。**

| タイムライン | 表示されるユーザー |
|--:|:--|
| **ホーム** | 自分がフォローしたユーザー |
| **ローカル** | インスタンス内のすべてのユーザー |
| **ソーシャル** | ホーム + ローカル |
| **グローバル** | リモートも含め、インスタンスに認識されているすべてのユーザー |

なお、ノートに設定された[公開範囲](https://joinmisskey.github.io/ja/usage/post/#公開範囲を設定する)も影響します。  
**[→ 機能: タイムライン](/ja/function/tl)**

# 重い
Misskey Webではアニメーションを多用しています。Misskey Webのアニメーションはそこそこのスペックがないと快適に動作しなかったり、長時間タブを開いているとフリーズしたりすることが報告されています。  
「UIの動きを減らす」を有効にするとそのような重いアニメーションが削減されるので、使ってみてください。

# MisskeyはMastodonのインスタンスなの？
**[否](//joinmisskey.github.io/ja/blog/2018/08/17_1_misskeyisnotmastodon/)**。  
Mastodonと中身が同じで操作部だけ新しく作成した、というわけでもないです。MisskeyとMastodonは、ActivityPubで接続できる以外には完全に無関係なソフトです。

# MisskeyはMastodonと連携できるの？
連携とは少し違いますが、MastodonとMisskeyで、相互にユーザーをフォローしたりノートやトゥートを送受信することができます。

MisskeyからMastodonのユーザーをフォローでき、逆にMastodonからMisskeyユーザーもフォローできます。また、ノートにリアクションを付けたりリノート（=ブースト）も行えます。

MisskeyやMastodonは、別のソフトウェアの他のインスタンスのユーザーとも、同じサービスであるかのように交流できます。

# 文字装飾、検索窓や文字のアニメーションはどうやるのか？
Misskey独自の構文「Misskey Flavored Markdown (MFM)」を使うことで表現できます。  
**[→ 機能: Misskey Flavored Markdown)](/ja/function/mfm)**

# 猫耳生えてにゃって言ってるけどにゃに？　Catって？
**Cat**はMisskeyの謎機能のひとつ。  
アイコンに猫耳が生え、*な*が*にゃ*に変換されます。

Catは設定画面から設定できます。  
にゃお、リモートにも反映されます。

# 不具合を見つけた。こんな機能がほしい。
**Misskey.io**に登録している場合は、[Misskey Feedback Channel](https://misskey.io/channels/8b79iuz1af)を利用することができます。

**GitHub**を使ったことがある方は*その内容のIssueが立っていないか確認してから*[Issue](https://github.com/syuilo/misskey/issues/new/choose)で報告をお願いします。  
Pull Requestももちろん歓迎しています。

上記のどちらも難しい場合は[@syuilo@misskey.io](https://misskey.io/@syuilo)へリプライを送ることも可能です。

# Misskeyに寄付したい。
ほしいものリストやPatreonのリンクなどがあるので[**joinmisskey（トップページの一番最後のセクション）**](https://join.misskey.page/ja/#section_7)を参照してください。

# パスワードを忘れた
メールで連絡するか新しいアカウントを作成するなどして、インスタンスの管理者（admin）に相談してください。

インスタンスの管理者がそのアカウントがあなたのものであると確認できたら、管理者はパスワードを初期化して新しいパスワードをあなたに伝えるでしょう。

こうして新しいパスワードでログインできるようになります。
念のため設定画面からパスワードを変更しておくことを推奨します。

# ログアウトできない
ブラウザのローカルストレージを削除してみてください。