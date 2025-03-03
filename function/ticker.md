---
title: サーバー情報
description: InstanceTicker 的なもの
published: true
date: 2023-08-01T07:04:45.182Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:46:10.372Z
---

# サーバー情報

当記事では以下の機能について記述します。

- **サーバー情報**
  - いわゆる「**/about ページ**」のことです。
- **ノートのサーバー情報。旧称「ノートのインスタンス情報」**
  - 所属するサーバー名を投稿者名の下に表示される機能。別名「Instance Ticker」。

## サーバー情報

「**サーバー情報**」とは、サーバーの情報を表示するページで、サーバーの説明、Misskeyのバージョン、管理者の名前と連絡先、統計（ユーザー数・総投稿数）を確認することができます。

### 見る方法。

- **misskey.domain/about** にアクセスします。
  - この方法は、Mastodon や Pleroma なども共通し、いわゆる「**/about ページ**」と呼ばれています。
- (ログイン中の場合)「もっと!」＞「ⓘ情報」＞「ⓘサーバー情報」

## ノートのサーバー情報

「**ノートのサーバー情報**」とは、 Misskey では [v12.51.0](https://github.com/syuilo/misskey/releases/tag/12.51.0) (2020/10/27) に搭載した機能です。 

この機能は、 **[Misskey](/ja/software/misskey)** (「**ノートのサーバー情報**」) および **[めいすきー](/ja/software/meisskey)** (「**インスタンス情報**」)において、**所属するサーバー名を投稿者名の下に表示される機能**について記述していますが、このように機能名に表記ゆれがあるため、注意して下さい。

### 特徴と搭載までの経緯

![InstanceTickerの表示例](/ja_jp/function/ticker/ticker-1.png)

投稿者の所属サーバーのアイコンと名称が表示され、背景色は左から右に向けて透過グラデーションがされるもので、早い話が「Windows95」当時のウィンドウ上部「タイトルバー」のような見た目をしています。

このデザインとアイデアは、[weepjp](https://fedibird.com/@weepjp) による Mastodon用カスタムCSS の [#InstanceTicker](https://inst.ance.tk) が元になっており、Misskey および めいすきーでは、いわゆる「目コピ」で採用されています。

[syuilo](/ja/persons/syuilo)氏曰く「[InstanceTicker的なもの](https://misskey.io/notes/8e8gz9ethy)」と代名詞化され、搭載されたリリース情報にも「[Instance Ticker](https://github.com/syuilo/misskey/releases/tag/12.51.0)」と記載されました。

先述した通り、あくまでも「目コピ」であり、パッと見では似ていますが Misskey および めいすきーでは実装機能であるため、当然 Mastodon用カスタムCSSである #InstanceTicker とは完全に別物です。

かつて存在し廃止された #InstanceTicker for Misskey の後継機能としての役割を担っているため、#InstanceTicker の開発者は「支援者として名前が載ることよりもうれしかった」と好意的な感想を述べており([参照](https://www.weep.blog/2022/12/24.html))、関連する[Issue を投稿した](https://github.com/misskey-dev/misskey/issues/8079)こともあり、一切関わりはないわけでもない。

#### 名称について

#InstanceTicker と区別され、Misskey では「インスタンス情報」と言う名称搭載されました。

「インスタンス情報」という名称と機能搭載は、[めいすきー](/ja/software/meisskey) が先行して [10.102.293-m544](https://github.com/mei23/misskey/releases/tag/10.102.293-m544) (2020/07/30) に搭載していましたが、その事情を[syuilo](/ja/persons/syuilo)氏は把握しないまま、[Misskey](/ja/software/misskey) に同名称で搭載しました。これは「[偶然](https://misskey.io/notes/8e8hbfqim7)」であるとしています。

そういった経緯から、[Misskey](/ja/software/misskey) と [めいすきー](/ja/software/meisskey) では、「インスタンス情報」という名称は共通であっても、仕様は共通ではないという事情を抱えていました。

ところが、2022年頃から「インスタンス」を「サーバー」と称するほうが適切なのではないか（[インスタンス → サーバーにする](https://github.com/misskey-dev/misskey/issues/7599)）とする話題が挙がり、翌年の[v13.9.0](https://github.com/misskey-dev/misskey/releases/tag/13.9.0)(2023/03/03) には、機能名を「ノートのインスタンス情報」から「ノートのサーバー情報」と改められました。

海外では、以上の経緯を知らずしてか、内部的な名称を参照して「instance ticker」または、単に「ticker」と呼ぶようです([参照](https://akkoma.dev/FoundKeyGang/FoundKey/src/branch/main/CHANGELOG.md))。

### 有効にするには

#### 現在の方法

- 「設定」＞「クライアント設定」＞「全般」＞「ノートのサーバー情報」
- ドロップダウンリストから以下を選択
  - 「表示しない」 - 無効。表示させません。
  - 「リモートユーザーに表示」 - すなわち同一サーバーのユーザーは表示されません。
  - 「常に表示」 - 全てのユーザーに表示されます。


#### ~~搭載された当初の方法~~

~~「設定」＞「全般」＞「アピアランス」＞「ノートのインスタンス情報」から操作できます。~~

![InstanceTickerを有効かする方法](/ja_jp/function/ticker/ticker-2.png)

（歴史的資料として残しています）

### 仕様の違い

#### Misskey
![Misskeyでの表示例](/ja_jp/function/ticker/ticker-1.png)
- **設定項目では「ノートのインスタンス情報」となっています。**
- **背景色は、対象インスタンスのトップページのHTMLのメタタグに含まれるテーマカラーを抽出して取得しています。** [[1](https://misskey.io/notes/8e6sstujc6)]
- **アイコンは、当初 favicon を直リンを表示していましたが、現在はプロキシー画像を表示しています。**
- **表示名は、対象インスタンスの設定名を取得しています。**
- **角に丸みがあります。**
- **文字の縁取りは黒色です。**
- **「リモートユーザーに表示」で同一サーバーを非表示にでき、「常に表示」で全ユーザーに表示できます。**


#### めいすきー
![めいすきーでの表示例](/ja_jp/function/ticker/ticker-3.png)

- 設定項目では「インスタンス情報を表示する」となっています。
- 背景色は、おそらく Misskey と同様？
- アイコンは、favicon のプロキシー画像を表示しています。
- 表示名はおそらく Misskey と同様でインスタンスの設定名を取得して表示。さらに括弧してドメイン名も表示しています。
- Misskey と同様に角に丸みはありますが、控えめです。
- リモートユーザーのみに表示され、同一インスタンスのユーザーには表示されません
  - この仕様は、おそらく #InstanceTicker for Misskey(廃止済) と同様の振る舞いを意識していると思われます(いわゆる「リモートユーザーに表示」と同等)。

#### Foundkey

- 概ね Misskey に追従した見た目ですが、以下の違いがあります。
  - 右側にソフトウェア名を表示しています。
  - マウスカーソルを置くとソフトウェア名とバージョンを表示しています。


#### Firefish (旧 Calckey)

- 機能名は Misskey に追従した形で「サーバー情報」となっています。
  - 設定項目では「**投稿の**サーバー情報」となっています。
- 投稿者名の下でなく、相対日付に近い位置で表示がされます。
  - これはおそらく、 Soapbox および Akkoma (ともに Pleroma フォーク)にて、所属サーバーの Favicon 表示がされる位置要素を反映しているのだと思われます。
- このため、極めて表示領域が狭くなっており、控えめです。
- 文字の縁取りは白で文字色は黒。
- マウスカーソルを置くとソフトウェア名を表示します (Akkomaおよび[Foundkey](/ja/software/foundkey)も同様)。

#### #InstanceTicker (元ネタ)
![Mastodonでの表示例](/ja_jp/function/ticker/ticker-4.png)

- 背景色はSNSソフトウェア別に分類されています。また、鯖缶からの要請でも変更されます。
- アイコンは、ソフトウェアロゴの表示(Type:0)、favicon (直リンでない)を表示しています(Type:1 - Type:3)。また、鯖缶からの要請で変更できます。
- Mastodon v3 以前のバージョン(mod330) と v4.0.x 以降バージョン(mod402)が用意されており、後者は仕様の都合で Misskey での「リモートユーザーに表示」と同等のものにされています。
- 表示名は、インスタンスのドメイン名ですが、鯖缶からの要請で変更されます。
- 角に丸みなどはありませんが、表示名にはうっすら影があります。
- #InstanceTicker for Misskey (どうやら Dolphin も対応していたかも)が、かつて存在していましたが、廃止した経緯があります。
