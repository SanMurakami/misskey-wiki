---
title: よくある質問
description: 
published: true
date: 2021-10-14T17:46:33.987Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:46:32.604Z
---

# ホーム、ローカル、ソーシャル、グローバル 違いは？
**A. それぞれ、表示されるユーザーが違う。**

| タイムライン | 表示されるユーザー |
|--:|:--|
| **ホーム** | 自分がフォローしたユーザー |
| **ローカル** | インスタンス内のすべてのユーザー |
| **ソーシャル** | ホーム + ローカル |
| **グローバル** | リモートも含め、インスタンスに認識されているすべてのユーザー |

なお、ノートに設定された[公開範囲](https://joinmisskey.github.io/ja/usage/post/#公開範囲を設定する)も影響する。  
**[→ 機能: タイムライン](/ja/function/tl)**

# 重い
Misskey Webではアニメーションを多用しているが、これはそこそこのスペックがないと快適に動作しなかったり、長時間タブを開いているとフリーズしたりすることが報告されている。  
「UIの動きを減らす」を有効にするとそのような重いアニメーションが削減されるので、使ってみてほしい。

# MisskeyはMastodonのインスタンスなの？
**[否](//joinmisskey.github.io/ja/blog/2018/08/17_1_misskeyisnotmastodon/)**。  
Mastodonと中身が同じで操作部だけ新しく作成した、というわけでもない。MisskeyとMastodonは、ActivityPubで接続できる以外には完全に無関係なソフトだ。

# MisskeyはMastodonと連携できるの？
連携とは少し違う。MastodonとMisskeyで、相互にユーザーをフォローしたりノートやトゥートを送受信したりできる。

MisskeyからMastodonのユーザーをフォローできるし、逆にMastodonからMisskeyユーザーもフォローできる。また、ノートにリアクションを付けたりリノート（=ブースト）も行える。

MisskeyやMastodonは、別のソフトウェアの他のインスタンスのユーザーとも、同じサービスであるかのように交流できる。

# 文字装飾、検索窓や文字のアニメーションはどうやるのか？
Misskey独自の構文「Misskey Flavored Markdown (MFM)」を使うことで表現できる。  
**[→ 機能: Misskey Flavored Markdown)](/ja/function/mfm)**

# 猫耳生えてにゃって言ってるけどにゃに？　Catって？
**Cat**はMisskeyの謎機能のひとつ。  
アイコンに猫耳が生え、*な*が*にゃ*に変換される。

Catは設定画面から設定できる。  
なお、リモートにも反映される。

# 不具合を見つけた。こんな機能がほしい。
**Misskey.io**に登録している場合は、[Misskey Feedback Channel](https://misskey.io/channels/8b79iuz1af)を利用することができる。

**GitHub**を使ったことがある方は*その内容のIssueが立っていないか確認してから*[Issue](https://github.com/syuilo/misskey/issues/new/choose)で報告をお願いしたい。  
Pull Requestももちろん歓迎している。

上記のどちらも難しい場合は[@syuilo@misskey.io](https://misskey.io/@syuilo)へリプライを送ることも可能。

# Misskeyに寄付したい。
ほしいものリストやPatreonのリンクなどがあるので[**joinmisskey（トップページの一番最後のセクション）**](https://join.misskey.page/ja/#section_7)を参照されたい。

# パスワードを忘れた
メールで連絡するか新しいアカウントを作成するなどして、インスタンスの管理者（admin）に相談してほしい。

インスタンスの管理者がそのアカウントがあなたのものであると確認できたら、管理者はパスワードを初期化して新しいパスワードをあなたに伝える。

こうして新しいパスワードでログインできるようになる。念のため設定画面からパスワードを変更しておくとよいだろう。

# ログアウトできない
ブラウザのローカルストレージを削除してみてほしい。