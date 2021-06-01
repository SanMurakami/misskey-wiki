---
title: Misskey.wiki로부터 인용 방법
description: Misskey.wiki에서 정보를 인용할 때의 주의점 등을 정리합니다.
published: true
date: 2021-06-01T13:36:07.915Z
tags: 
editor: markdown
dateCreated: 2021-06-01T13:28:33.036Z
---

# URL 결정 방법
[Misskey.wiki](https://misskey.wiki/)에서 정보를 입력할 때 URL을 다음과 같이 입력합니다.


1. `[언어]/[작성할 카테고리의 영어 표기]/[페이지명의 영어 표기]`
2. 공백이 있는 페이지나 카테고리는 스네이크 케이스(언더바)를 사용한다
	1. 잘 모르겠다면 https://titlecase.com/ 에서 `snake_case`로 변환한 것을 붙여넣기
  
**다국어를 대응할 수 없게 되므로, 페이지 주소에 한국어를 사용하지 말아 주세요.**


## 작성 사례
### 전
![transplantation_guide_1.png](/ja_jp/wiki_guide/transplantation_guide_1.png)

### 후
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