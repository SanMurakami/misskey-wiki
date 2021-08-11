---
title: インスタンス情報
description: InstanceTicker 的なもの
published: true
date: 2021-08-11T07:25:30.638Z
tags: 
editor: markdown
dateCreated: 2020-11-19T10:30:41.443Z
---

# インスタンス情報とは

「**インスタンス情報**」とは、**[Misskey](/ja/software/misskey)** および **[めいすきー](/ja/software/meisskey)** において、所属インスタンスを投稿者名の下に表示される機能です。

Misskey では [v12.51.0](https://github.com/syuilo/misskey/releases/tag/12.51.0) (2020/10/27) に搭載されました。 

![InstanceTickerの表示例](/ja_jp/function/ticker/ticker-1.png)

アイデアは、[weepjp](https://miyon.miyon.org/@weepjp) による Mastodon用カスタムCSS の [#InstanceTicker](https://ja.mstdn.wiki/InstanceTicker) です。

[syuilo](/ja/persons/syuilo)氏曰く「[InstanceTicker的なもの](https://misskey.io/notes/8e8gz9ethy)」と代名詞化して説明され、搭載されたリリース情報にも「[Instance Ticker](https://github.com/syuilo/misskey/releases/tag/12.51.0)」と記載されました。

見た目はパッと見一緒ですが、#InstanceTicker とは別物です。

# 名称について

元ネタの #InstanceTicker と区別され、Misskey では「インスタンス情報」と言う名称です。

「インスタンス情報」という名称と機能搭載は、[めいすきー](/ja/software/meisskey) が先行して [10.102.293-m544](https://github.com/mei23/misskey/releases/tag/10.102.293-m544) (2020/07/30) に搭載していましたが、その事情を[syuilo](/ja/persons/syuilo)氏は把握しないまま、[Misskey](/ja/software/misskey) に同名称で搭載しました。これは「[偶然](https://misskey.io/notes/8e8hbfqim7)」であるとされています。

そういった経緯から、[Misskey](/ja/software/misskey) と [めいすきー](/ja/software/meisskey) では、「インスタンス情報」という名称は共通であっても、仕様は共通ではないという事情を抱えています。

# 有効にするには

「設定」＞「全般」＞「アピアランス」＞「ノートのインスタンス情報」から操作できます。

![InstanceTickerを有効かする方法](/ja_jp/function/ticker/ticker-2.png)

# 仕様

「Windows95」ウィンドウ上部の「タイトルバー」的な見た目で、投稿者の所属インスタンスのアイコンと名称が表示され、背景色は左から右に向けて透過グラデーションがされるもの。

## 仕様の違い

### Misskey
![Misskeyでの表示例](/ja_jp/function/ticker/ticker-1.png)

- **背景色は、対象インスタンスのトップページのHTMLのメタタグに含まれるテーマカラーを抽出して取得しています。** [[1](https://misskey.io/notes/8e6sstujc6)]
- **アイコンは、対象インスタンスの favicon を直リンを表示しています。**
- **表示名は、対象インスタンスの設定名を取得しています。**
- **角に丸みがあります。**
- **「常に表示」で、同一インスタンスユーザーにも表示されます。**

### めいすきー
![めいすきーでの表示例](/ja_jp/function/ticker/ticker-3.png)

- 背景色は、おそらく Misskey と同様？
- アイコンは、favicon キャッシュ(原寸サイズ)を表示しています。
- 表示名はおそらく Misskey と同様でインスタンスの設定名を取得して表示し、さらに括弧してドメイン名も表示しています。
- Misskey と同様に角に丸みはあるが、控えめです。
- リモートユーザーのみに表示され、同一インスタンスのユーザーには表示されません
  - この仕様は、おそらく #InstanceTicker for Misskey(廃止済) と同様の振る舞いを意識していると思われます

### #InstanceTicker
![Mastodonでの表示例](/ja_jp/function/ticker/ticker-4.png)

- 背景色はSNSソフトウェア別に分類されています。また、鯖缶からの要請でも変更されます。
- アイコンは、SNSロゴ(Type-0)、favicon キャッシュ(縮小サイズ)を表示(Type-1)しています。favicon キャッシュ(縮小サイズ)に自動で白フチをつけて表示(Type-2)しています。また、鯖缶からの要請でも変更されます。
- 表示名は、インスタンスのドメイン名です。また、鯖缶からの要請でも変更されます。
- 角に丸みなどはありませんが、表示名にはうっすら影があります。
- #InstanceTicker for Misskey(廃止済) では、リモートユーザーのみ表示縛り且つ、一部のリプライなど表示されないケースがありました。
