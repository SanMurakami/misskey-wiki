---
title: Misskey Flavored Markdown
description: Misskeyで使えるMarkdown風の構文
published: true
date: 2020-11-19T11:11:58.619Z
tags: 
editor: markdown
dateCreated: 2020-09-20T08:21:41.404Z
---

**Misskey Flavored Markdown**または**MFM**とは、Misskey内の様々な場所で使用できる文字装飾。

Misskeyサーバ同士であれば他のサーバでも表示されるが、ActivityPub対応の他のSNSサービスでは装飾が全て表示されることは保証されない。

# MFMが適用される部分
- [ノート](/function/note)
  * ノートメニューで`内容をコピー`すると元のテキストがクリップボードにコピーされるため、メモ帳等にペーストすることでどのようなMFMが使われているかが確認できる。
- [トーク](/function/messaging)のメッセージ
- [ページ](/function/page)
- [プロフィールの自己紹介](/function/user_profile)
- インスタンスの説明文
- インスタンスのお知らせ

# MFM一覧
MFMは「メンション」や「ハッシュタグ」といった、Misskeyの基本的なマークアップにも使用されている。

## メンション
アットマーク + ユーザー名で、特定のユーザーにメンションを送ることが出来る。
> @ai
```
@ai
```

## ハッシュタグ
ナンバーサイン + タグ名で、ハッシュタグを付けることができる。
> #Misskey自己紹介部
```
#Misskey自己紹介部
```

## URL
URLを貼ると自動的にリンク付けされる。
> https://misskey.io/mfm-cheat-sheet
```
https://misskey.io/mfm-cheat-sheet
```


## リンク
文章の特定の範囲を、URLに紐づけることができる。
> [MisskeyでFediverseの世界が広がります](https://example.com)
```
[MisskeyでFediverseの世界が広がります](https://example.com)
```

## カスタム絵文字
コロンでカスタム絵文字名を囲むと、カスタム絵文字を表示させることができます。
> ![ai_icon_64px.png](/ai_icon_64px.png)
```
:ai_icon:
```

## 太字
テキストをアステリスク記号×2で囲むと、文字を太く表示して強調することができます。
> わーーーーーー **わーーーーーーーーーーーー！！！！** わーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー 
```
わーーーーーー **わーーーーーーーーーーーー！！！！** 
わーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー 
```


# 外部リンク
- https://yuzulia.xyz/@aqz/pages/mfm - MFM一覧。
