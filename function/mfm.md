---
title: Misskey Flavored Markdown
description: Misskeyで使えるMarkdown風の構文
published: true
date: 2020-11-22T21:03:56.228Z
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
実はこのMFM、メンションやハッシュタグといったMisskeyの身近なところでも使われている。
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
> アットマーク`@`やナンバーサイン`#`の後に文字を入力すると候補リストが出現する。 このリストは文字を入力していくにつれて絞り込まれていくので、もし探しているユーザーやハッシュタグがリスト内に見つかったら、矢印キーやTabを使って選択し、`Enter`キーで入力を完了することもできるぞ。さすがMisskey！
{.is-info}

![ss_hashtag2.png](/ja_jp/mfm/ss_hashtag2.png)


# 文字装飾
MFMといえばこれを連想する者が多い。テキストを特定の記号や文字列で囲うことにより文章を読みやすくしたり、文脈を明確にしたりできる機能だ。

### 太字
テキストをアステリスク記号二つ`**`と`**`で囲むと、文字を**太く表示**して**強調する**ことができる。
![ss_bold.png](/ja_jp/mfm/ss_bold.png)
```
今のはメラゾーマではない、**メラ**だ…
```
　
### 削除線
テキストをチルダ二つ`~~`と`~~`で囲むと、~~打ち消し~~**削除線**を加えることができる。
![ss_strikethrough.png](/ja_jp/mfm/ss_strikethrough.png)
```
~~でも藍ちゃんのならちょっと見たいかも~~
```
　
### 小さい字
テキストを`<small>`と`</small>`で囲うと文字を <small>小さく</small> 表示させることができる。
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

### 文字反転
テキストを反転させることができるMisskey.v12の新機能。`[flip]`

#### 左右反転
![ss_flip.png](/ja_jp/mfm/ss_flip.png)
```
牛耕式（ぎゅうこうしき）とは
[flip 主に古代ギリシアなどでの写本]
や銘文に用いられた書記方式の
[flip 一種である。　　　　　　　　]

ギリシア語ではβουστροφηδόν
[flip （ボウストロフェードン）と　　]
　　呼ばれ、語源は："βοῦς"（ボウス、牛）＋
[flip "στροφή"（ストローフェ、引き返す）に　　　]
　　　副詞化接尾辞の "-δόν"（〜のようなさま）
[flip が加わり「（畑などを耕す）牛が　　　　　　]
　　　　　　引き返すさま」という意から来ている。
```
#### 上下反転

```

```
#### 上下左右反転（180度回転）

```

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
高度と言っても内部処理が高度なだけで、構文自体は非常に書きやすい親切設計となっている。
### 検索窓
文末に`検索`の一言を添えるだけで入力済みの検索ボックスを表示させることができる。
> 検索窓召喚の文字列は`検索`のほかにも`[検索]`、`Search`、`[Search]`などがある。いずれも文末に置くだけで等しく効果を発揮するぞ。
{.is-info}

![ss_search.png](/ja_jp/mfm/ss_search.png)
```
藍ちゃん　戦闘レベル　検索

AiScript とは [検索]

Is Misskey Mastodon? Search

What is a Miskist? [Search]
```

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
> カスタム絵文字はメンションやハッシュタグのように、コロン`:`を打ち込んだ瞬間、候補リストが出現し、文字を入力するにつれだんだんと候補が絞り込まれていく仕組みだ！もちろん、お目当ての絵文字がリスト内に表示されたらそれを選ぶと入力を確定できるから大変便利だ。すごいぞMisskey！
{.is-info}

![ss_customemoji_list.png](/ja_jp/mfm/ss_customemoji_list.png)

　
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
なんか創作的かつ
Misskeyに関係のある
面白いコード
```
``````

> インラインコードやブロックコード内の文章はMFMが適用されず、（ほぼ）何を書いてもそのまま反映されるので、特殊な構文とかの引用のほか、アスキーアートなどにも使えるかもしれない…！
{.is-info}

![ss_blockcode_ai.png](/ja_jp/mfm/ss_blockcode_ai.png)

# アニメーション


# LaTeX表現


# 外部リンク
- https://yuzulia.xyz/@aqz/pages/mfm - MFM一覧。






