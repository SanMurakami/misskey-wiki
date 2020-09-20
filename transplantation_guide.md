---
title: Misskey.wiki からの移植ガイド
description: Misskey.wiki から情報を移植する際の注意点などをまとめています。
published: true
date: 2020-09-20T01:51:56.426Z
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
![transplantation_guide_1.png](/wiki_guide/transplantation_guide_1.png)

### 移植先
![transplantation_guide_2.png](/wiki_guide/transplantation_guide_2.png)


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
