---
title: Misskey Flavored Markdown
description: Misskeyで使えるMarkdown風の構文
published: true
date: 2020-11-22T19:05:55.716Z
tags: 
editor: markdown
dateCreated: 2020-09-20T08:21:41.404Z
---

**Misskey Flavored Markdown**または**MFM**とは、Misskey内の様々な場所で使用できる文字装飾。

Misskeyサーバ同士であれば他のサーバでも表示されるが、ActivityPub対応の他のSNSサービスでは装飾が全て表示されることは保証されない。

- MFMが適用される部分

- [ノート](/function/note)
> ノートメニューで`内容をコピー`すると元のテキストがクリップボードにコピーされるため、メモ帳等にペーストすることでどのようなMFMが使われているかが確認できる。
{.is-info}

- [トーク](/function/messaging)のメッセージ
- [ページ](/function/page)
- [プロフィールの自己紹介](/function/user_profile)
- インスタンスの説明文
- インスタンスのお知らせ

# 基本的なMFM
MFMはメンションやハッシュタグといったMisskeyの基本的な機能にも使われている。
### メンション
アットマーク`@` + ユーザー名で、特定のユーザーにメンションを送ることができる。
![mention.png](/ja_jp/mfm/mention.png)
```
@ai
```

### ハッシュタグ
ナンバーサイン`#` + タグ名で、ハッシュタグを付けることができる。
![ss_hashtag.png](/ja_jp/mfm/ss_hashtag.png)
```
#Misskey自己紹介部
```
　
　
 ---
　

> アットマーク`@`やナンバーサイン`#`の後に文字を入力すると候補リストが出現する。 このリストは文字を入力していくにつれて絞り込まれていくので、もし探しているユーザーやハッシュタグがリスト内に見つかったら、矢印キーやTabを使って選択し、`Enter`キーで入力を完了することもできるぞ。さすがMisskey！
{.is-info}

![ss_hashtag2.png](/ja_jp/mfm/ss_hashtag2.png)


# 文字装飾
### 太字
テキストをアステリスク記号二つ`**`と`**`で囲むと、文字を**太く表示**して**強調する**ことができる。
> わーーーーーー **わーーーーーーーーーーーー！！！！** わーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー 
```
わーーーーーー **わーーーーーーーーーーーー！！！！** 
わーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー 
```
　
### 削除線
テキストをチルダ二つ`~~`と`~~`で囲むと、~~打ち消し~~**削除線**を加えることができる。
![ss_strikethrough.png](/ja_jp/mfm/ss_strikethrough.png)
```
~~でも藍ちゃんのならちょっと見たいかも~~
```
　
### 目立たない字
テキストを`<small>`と`</small>`で囲うと内容を <small>小さく</small> 表示させることができる。
> へ、編集してくれたって別にあんたのコトなんて何とも思ってないんだからね！
<small>･･････でもほんのちょっとだけ嬉しい、かも･･･</small>
```
へ、編集してくれたって別にあんたのコトなんて何とも思ってないんだからね！
<small>･･････でもほんのちょっとだけ嬉しい、かも･･･</small>
```
　
### 中央寄せ
文章を`<center>`と`</center>`で囲うと中央に寄せて表示することができる。
![ss_center3.png](/ja_jp/mfm/ss_center3.png)
```
<center>殺伐としたスレにインド象が！</center>
<center>（しまうま）</center>
<center>🐶</center>
<center>「にゃーん！！」</center>
<center>　ハ　ム　ス　タ　ー　</center>
```
### テキストの引用
行頭に`> `を付けると内容が引用であることを示すことができる。
![ss_quote.png](/ja_jp/mfm/ss_quote.png)
```
> シャミ子が悪いんだよ
↑言ってない
```
また、`>> `で二重引用を示すこともできる。
![ss_doublequote.png](/ja_jp/mfm/ss_doublequote.png)
```
>> シャミ子が悪いんだよ
> ↑言ってない
たまたまそういうとこが描かれてないだけで普通に言ってるんだよなぁ
```

# 高度なMFM

### URL
URLを貼ると自動的にリンク付けされる。
![ss_link.png](/ja_jp/mfm/ss_link.png)
```
https://misskey.io/mfm-cheat-sheet
```
　
### リンク
リンクにしたいテキストを角括弧`[]`で囲い、そのすぐ隣に丸括弧`()`で囲んだURLを書き足すことにより、角括弧内の文を丸括弧内のURLに紐づけることが出来る。
![ss_link2.png](/ja_jp/mfm/ss_link2.png)
```
[省略しています。全て読むにはこのリンクをクリック！](https://dic.nicovideo.jp/a/%E5%85%A8%E3%81%A6%E8%AA%AD%E3%82%80%E3%81%AB%E3%81%AF%E3%81%93%E3%81%AE%E3%83%AA%E3%83%B3%E3%82%AF%E3%82%92%E3%82%AF%E3%83%AA%E3%83%83%E3%82%AF%21)
```
　
### カスタム絵文字
コロン`:` `:`でカスタム絵文字名を囲むと、カスタム絵文字を表示させることができる。
![ss_customemoji.png](/ja_jp/mfm/ss_customemoji.png)
```
:ai_icon:
```
　

　
### インラインコード
プログラムなどのコードを行内（インライン）でグレイヴアクセント`` ` ``と`` ` ``に囲んであげるとシンタックスハイライトしてくれる。
![ss_inlinecode.png](/ja_jp/mfm/ss_inlinecode.png)
```
`　<:"Hello, AiScript!"　`
```
　
### ブロックコード
複数行のコード等をシンタックスハイライトしたい場合、三連グレイヴアクセント` ``` `と` ``` `で囲むとコードブロックを作成することができる。どうやら[Prism.js](https://prismjs.com/)を使用しているらしく<small>[要検証]</small> 、もしそうであればなんと**236言語**のシンタックスハイライティングに対応していることとなる。ヤバいぞMisskey！

``````
```

```
``````

> インラインコードやブロックコード内の文章はMFMが適用されず、（ほぼ）何を書いてもそのまま反映されるので、特殊な構文とかの引用のほか、アスキーアートなどにも使えるかもしれない・・・！
{.is-info}

![ss_blockcode_ai.png](/ja_jp/mfm/ss_blockcode_ai.png)

# 外部リンク
- https://yuzulia.xyz/@aqz/pages/mfm - MFM一覧。






