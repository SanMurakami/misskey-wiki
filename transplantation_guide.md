---
title: Misskey.wiki からの移植ガイド
description: Misskey.wiki から情報を移植する際の注意点などをまとめています。
published: true
date: 2020-09-20T02:49:58.995Z
tags: 
editor: markdown
dateCreated: 2020-09-20T01:32:29.340Z
---

# URLの決め方
[Misskey.wiki](https://misskey.wiki/) から情報を移植する際、URLは以下のようにしてください。


1. `[言語]/[移植元カテゴリの英語表記]/[ページ名の英語表記]`
2. スペースが入るページやカテゴリについてはスネークケース(アンダーバー)を使う
	1. わからない場合は https://titlecase.com/ で`snake_case`に変換したものを貼り付け
  
**多言語対応できなくなるので、くれぐれもページパスに日本語を使わないでください**


## 移植例
### 移植元
![transplantation_guide_1.png](/ja_jp/wiki_guide/transplantation_guide_1.png)

### 移植先
![transplantation_guide_2.png](/ja_jp/wiki_guide/transplantation_guide_2.png)


# 未掲載項目のURL化
未掲載項目は赤文字になりますが、**赤文字のリンクをクリックすると新規ページを作成できる**様になるので、掲載できそうな項目はなるべく全てにリンクを貼っていってください。

例えば`ヘルプ`カテゴリ内の`よくある質問`を未掲載リンクとして記述する場合は以下の通りになります。

未掲載項目のリンクは以下のようになります
<small>※以下のページはデモ用ですので、実際には作成しないでください</small>
[未掲載項目の例](/ja/demo/notfound_demo)

ページパス
```
/ja/demo/notfound_demo
```

Markdown
```md
[未掲載項目の例](/ja/demo/notfound_demo)
```

# 画像ファイル等のアップロード時の注意点

## ファイルパスについて

**rootディレクトリには何も置かないでください**
ディレクトリは必ず以下のようにしてください


#### 言語が関係ない共通ファイル
`/root/common/[ページのカテゴリ]/[ページタイトル]/[ファイル]`

#### UIのスクリーンショット等、言語の影響を受けるファイル
`/root/[言語]/[ページのカテゴリ]/[ページタイトル]/[ファイル]`


### 例
「機能」カテゴリ内の[「ノート」](/ja/function/note)より

ページのURL
```
/ja/function/note
```
画像ファイルのURL
```
/ja_jp/function/note/note_form.png
```

ページのURLが`ja`なのにディレクトリが`ja_jp`なのはWiki.jsの仕様でルートには3文字以下のページやディレクトリを作成できないためです。

なので、他の言語のファイルをアップロードする際も`en`なら`en_us`という形にしてください。



## ディレクトリの移動
Wiki.jsはディレクトリの移動が独特なので気づきにくいですが、画像の赤枠の部分でディレクトリの移動が可能です。
![directory_guide_1.png](/ja_jp/wiki_guide/directory_guide_1.png)


## 一度作ったフォルダは消せません
Wiki.jsは現在開発中のためまだフォルダの管理は未実装で、現状では間違って作成したフォルダはデータベースからしか消せないため、フォルダを作る際は十分気をつけてください。

もし間違ったフォルダを作ってしまった場合は [@AureoleArk@misskey.io](https://misskey.io/@AureoleArk) までご連絡ください。