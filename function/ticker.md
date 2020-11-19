---
title: インスタンス情報
description: InstanceTicker 的なもの
published: true
date: 2020-11-19T11:21:44.721Z
tags: 
editor: markdown
dateCreated: 2020-11-19T10:30:41.443Z
---

# インスタンス情報とは

「**インスタンス情報**」とは、**[Misskey](/ja/software/misskey)** および **[めいすきー](/ja/software/meisskey)** において、所属インスタンスを投稿者名の下に表示される機能のこと。

Misskey では [v12.51.0](https://github.com/syuilo/misskey/releases/tag/12.51.0) (2020/10/27) に搭載された。 

![7cd0dadc9869800993cbf6c448b9fc4.png](/7cd0dadc9869800993cbf6c448b9fc4.png)

元ネタは、[みよんみよん](https://miyon.miyon.org/@miyon) と [weepjp](https://miyon.miyon.org/@weepjp) による Mastodon用カスタムCSS の [#InstanceTicker](https://ja.mstdn.wiki/InstanceTicker) である。

[syuilo](/ja/persons/syuilo)氏曰く「[InstanceTicker的なもの](https://misskey.io/notes/8e8gz9ethy)」と代名詞化して説明され、搭載されたリリース情報にも「[Instance Ticker](https://github.com/syuilo/misskey/releases/tag/12.51.0)」と書かれた。

見た目はパッと見一緒だが、#InstanceTicker とは別物である。

# 名称について

元ネタの #InstanceTicker と区別され、Misskey では「インスタンス情報」と言う名称である。

「インスタンス情報」という名称と機能搭載は、[めいすきー](/ja/software/meisskey) が先行し [10.102.293-m544](https://github.com/mei23/misskey/releases/tag/10.102.293-m544) (2020/07/30) に搭載しており、その事情を[syuilo](/ja/persons/syuilo)氏は把握しないまま、[Misskey](/ja/software/misskey) に同名称で搭載したのは、「[偶然](https://misskey.io/notes/8e8hbfqim7)」であるとしている。

そういった経緯から、[Misskey](/ja/software/misskey) と [めいすきー](/ja/software/meisskey) では、「インスタンス情報」という名称は共通であっても、仕様は共通ではないという事情を抱えている。

# 有効にするには

「設定」＞「全般」＞「アピアランス」＞「ノートのインスタンス情報」から操作できる。

![7cd0dadc9869800993cbf6c448b9fc49.png](/7cd0dadc9869800993cbf6c448b9fc49.png)

# 仕様

「Windows95」ウィンドウ上部の「タイトルバー」的な見た目で、投稿者の所属インスタンスのアイコンと名称が表示され、背景色は左から右に向けて透過グラデーションがされるもの。

## 仕様の違い

### Misskey
![7cd0dadc9869800993cbf6c448b9fc4.png](/7cd0dadc9869800993cbf6c448b9fc4.png)

- **背景色は、対象インスタンスの背景色情報を取得している。**
- **アイコンは、対象インスタンスの favicon を直リンを表示。**
- **表示名は、対象インスタンスの設定名を取得している。**
- **角に丸みがある。**
- **常に表示で、同一インスタンスユーザーも表示。**

### めいすきー
![fcc5e3f1241b190c05efd8912216449a.png](/fcc5e3f1241b190c05efd8912216449a.png)

- 背景色は、おそらく Misskey と同様。
- アイコンは、favicon キャッシュ(原寸サイズ)を表示。
- 表示名はおそらく Misskey と同様でインスタンスの設定名を取得して表示し、さらに括弧してドメイン名も表示。
- Misskey と同様に角に丸みはあるが、控えめである。
- リモートユーザーのみに表示され、同一インスタンスのユーザーには表示されない仕様は、おそらく #InstanceTicker for Misskey(廃止済) と同様の振る舞いを意識している？

### #InstanceTicker
![682009e30812ea5694a854cd519d764e.png](/682009e30812ea5694a854cd519d764e.png)

- 背景色はSNSソフトウェア別に分類されている。または鯖缶からの要請で変更される。
- アイコンは、SNSロゴ(Type-0)、favicon キャッシュ(縮小サイズ)を表示(Type-1)。favicon キャッシュ(縮小サイズ)に自動で白フチをつけて表示(Type-2)。または鯖缶からの要請で変更される。
- 表示名は、インスタンスのドメイン名。または鯖缶からの要請で変更される。
- 角に丸みなどはないが、表示名にはうっすら影がある。
- #InstanceTicker for Misskey(廃止済) では、リモートユーザーのみ表示縛り且つ、一部のリプライなど表示されないケースがあった。


# みよんみよん

![miyon2.png](/miyon2.png)

「みよんみよん」とは、 #InstanceTicker の看板娘である。

[syuilo](/ja/persons/syuilo)氏の「[みよんみよん以外の感情がない](https://misskey.io/notes/8e43jzr6or)」の「みよんみよん」とは、こいつのことである。

もともとは、weep が描いた[藍](/ja/aichan)の髪の色を変えただけの Misskey を表す代替アイコン（[藍](/ja/aichan)と同様の服を着てるのはこのため）として使用されていたが、#InstanceTicker の看板娘に昇格された。

名前の由来は、#InstanceTicker での Misskey のオフセットが 4 であり、「Misskey は 4」を縮めて「みよん」と言い出したことが開発チームにウケたことと、[藍](/ja/aichan)に対して「みよん」であること（あいみょん）。

みよんみよん以外の感情がないので、ついでに書きました。