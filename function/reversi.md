---
title: リバーシ
description: Misskeyで利用できるゲームの一つ
published: true
date: 2022-05-01T01:35:54.387Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:46:06.045Z
---

**リバーシ**とはの[Misskey Games](/games)で遊ぶことができるゲームの一つである。<!--v12.52.0で復活した。--> 現在はサーバー用のプラグインの開発のため一時的に廃止されている。
この項目ではリバーシの遊び方やルール説明の他、Misskey_v12に実装されている全リバーシマップを記載する。

# 遊び方
Misskeyユーザであれば誰でもプレイすることができる。左にあるサイドパネルから「もっと！」を押し、そこに出てきたポップアップメニューから Misskey Games を押せば自動的にMisskeyリバーシのページに飛ばされる仕組みとなっている。
ユーザとの対戦はゲーム内の「招待」から指定して、相手の承諾があれば開始できる。また、「招待」からのユーザー選択で対話型botである[藍](/aichan)を指定することも出来る。なお、藍と対戦する時のみ特別に[Botのオプション](/function/reversi#Botのオプション)がルールに追加される。
![menu.png](/ja_jp/reversi/menu.png)
![select.jpg](/ja_jp/reversi/select.png)
# ルール
交互に盤面へ石を打ち、相手の石を自分の石で挟むと その石を 自分の色の石に変えることが出来る。そして最終的に自分の石が最も多いプレイヤーが勝者となる。これがリバーシのもっとも基本的な遊び方である。
Misskeyリバーシでは、対局を始める前に特殊ルールを決めることができる。
![char_x.png](/ja_jp/reversi/rule.png)
## 石の少ないほうが勝ち(ロセオ)
石が最も多いプレイヤーが勝つのではなく、逆に石の最も少ない方が勝ちとなるルールである。~~これには正邪さんもニッコリ~~
## ループマップ
盤面の上下左右がループするモード。角の安置が実質消滅するので、エンディングまで超エキサイティングな試合をプレーすることができる。角のないリバーシ繋がりで多少ニップ感がでるかもしれない［要検証］
## どこでも置けるモード
文字通りどこにでも石を配置することができるローカルルールオプション。完全に別ゲーと化する。［筆者の主観］

## 先行/後攻
どのプレイヤーが先に石を置くことが出来るのかをここで決めることができる。デフォルトはランダムに設定されている。
![char_x.png](/ja_jp/reversi/turn.png)

## Botのオプション（特殊項目）
対戦相手を[藍](/aichan)にした時にだけ設定出来る特殊オプション。
![bot_option.png](/ja_jp/reversi/bot_option.png)
### 藍が対局情報を投稿するのを許可
リバーシを初めた時、藍がノートで「対局を○○さん始めました！」とタイムラインに投稿するのを許可するかどうかをここで決めることができる。ちなみにこのノートはホームにのみ表示される（グローバルには表示されない）。
![ai_post.png](/ja_jp/reversi/ai_post.png)
### 強さ
藍の強さを指定できる。最弱は「接待」で、全力で負けようとしてくる。強さが上がるに連れ、思考時間が長くなる。もっとも強い「最強」レベルではたまに長時間考え過ぎちゃうことがある。


# マップ
Misskeyリバーシでは、通常のリバーシの盤面以外にも、様々な大きさ、形、初期配置の盤面を利用できる。ゲーム開始前にお互いに盤面を自由に編集することもできる。

## -Custom-
カスタムマップ。下に表示されている盤面のマスを触るとそのマスの状態を「自分の石／相手の石／空白／壁(穴)」に変えることができる。こうやって出来たマップは `-Custom-` と表示され「カスタムマップ」として扱われる。
![custom.png](/ja_jp/reversi/custom.png)

## ランダム
ここにあるマップからひとつだけランダムで選ぶ設定。Misskeyリバーシは全体的に見てやや独特なマップが多く、このオプションはギャンブル要素がややつよい。

## 4x4
4×4マスの正方形盤を使うとても小さな盤面。主要時間はおおよそ1分なので、サクッと気軽に試合が出来る。また、三目並べ感覚で簡単に二人零和有限確定完全情報ゲームが楽しめるので、初歩的なゲーム理論の理解にも役立つかもしれない。
### 4x4
フォー・バイ・フォー。
4×4の正方形盤に交差する石が真ん中に配置されている最も基本的な盤面。完全解析されている。
![char_x.png](/ja_jp/reversi/4x4.png)

## 6x6
6×6マスの正方形盤を使用する小さな盤面。数分ぐらいで簡単な試合をすることができる。
### 6x6
シックス・バイ・シックス。
6×6の正方形盤に交差する石が真ん中に配置されている基本的な盤面。完全解析されているらしい。
![char_x.png](/ja_jp/reversi/6x6.png)
### 6x6 Rounded
シックス・バイ・シックス・ラウンデッド。
6×6の盤に交差する石が真ん中に配置されているが、各角が削られており、裏返すことの出来ない高得点地が増えているのが特徴。
![char_x.png](/ja_jp/reversi/6x6_rounded.png)
### 6x6 Rounded 2
シックス・バイ・シックス・ラウンデッド・ツー。
6×6の盤に交差する石が真ん中に配置されているが、各角が削られており、裏返すことの出来ない高得点地が増えているのが特徴。
![char_x.png](/ja_jp/reversi/6x6_rounded_2.png)

## 8x8
8×8マスの正方形盤を使う盤面。みんな知ってる定番のリバーシ。
### 8x8
スタンダード・リバーシ。（エイト・バイ・エイト）

![char_x.png](/ja_jp/reversi/8x8.png)
### 8x8 Handicap 1
ハンディキャップ・ワン。
![char_x.png](/ja_jp/reversi/8x8_handicap_1.png)
### 8x8 Handicap 2
ハンディキャップ・ツー。
![char_x.png](/ja_jp/reversi/8x8_handicap_2.png)
### 8x8 Handicap 3
ハンディキャップ・スリー。
![char_x.png](/ja_jp/reversi/8x8_handicap_3.png)
### 8x8 Handicap 4
ハンディキャップ・フォー。
![char_x.png](/ja_jp/reversi/8x8_handicap_4.png)
### 8x8 Handicap 28
ハンディキャップ・トウェンティーエイト。
![char_x.png](/ja_jp/reversi/8x8_handicap_28.png)
### 8x8 with notch
ウィズノッチ。
![char_x.png](/ja_jp/reversi/8x8_with_notch.png)
### 8x8 with some holes
ホールズ。
![char_x.png](/ja_jp/reversi/8x8_with_some_holes.png)
### 8x8 Rounded
ラウンデッド。
![char_x.png](/ja_jp/reversi/8x8_rounded.png)
### 8x8 Rounded 2
ラウンデッド・ツー。
![char_x.png](/ja_jp/reversi/8x8_rounded_2.png)
### 8x8 Rounded 3
ラウンデッド・スリー。
![char_x.png](/ja_jp/reversi/8x8_rounded_3.png)
### Circle
サークル。
![char_x.png](/ja_jp/reversi/circle.png)
### Lack of black
ラック・オブ・ブラック。
![char_x.png](/ja_jp/reversi/lack_of_black.png)
### Minesweeper
マインスイーパー。
![char_x.png](/ja_jp/reversi/minesweeper.png)
### Parallel
パラレル。
世界遊戯法大全（1907年）に記載されている20世紀リバーシの定番配置。8×8の正方形盤に、平行に重なり合った石を2個づつ、真ん中に配置する。
![char_x.png](/ja_jp/reversi/parallel.png)
### Reserved
![char_x.png](/ja_jp/reversi/reserved.png)
### Smile
![char_x.png](/ja_jp/reversi/smile.png)
### Square Party
![char_x.png](/ja_jp/reversi/square_party.png)
### Window
![char_x.png](/ja_jp/reversi/window.png)
### X
![char_x.png](/ja_jp/reversi/x.png)
## 10x10
グランドリバーシ。
### 10x10
![char_x.png](/ja_jp/reversi/10x10.png)
### Arena
![char_x.png](/ja_jp/reversi/arena.png)
アリーナマップ。
### Char X
![char_x.png](/ja_jp/reversi/char_x.png)
### Char Y
![char_x.png](/ja_jp/reversi/char_y.png)
### Checker
![char_x.png](/ja_jp/reversi/checker.png)
### CPU
![char_x.png](/ja_jp/reversi/cpu.png)
### Cross
![char_x.png](/ja_jp/reversi/cross.png)
アネクゼイションとも。
### Grid
![char_x.png](/ja_jp/reversi/grid.png)
### The Hole
![char_x.png](/ja_jp/reversi/the_hole.png)
### Japanese Curry
![char_x.png](/ja_jp/reversi/japanese_curry.png)
### Mosaic
![char_x.png](/ja_jp/reversi/mosaic.png)
### Reactor
![char_x.png](/ja_jp/reversi/reactor.png)
### Walls
![char_x.png](/ja_jp/reversi/walls.png)

## Special
常識の枠に捉えられない独特な盤面です。
### Big Board
![char_x.png](/ja_jp/reversi/big_board.png)
### Deal with it!
![char_x.png](/ja_jp/reversi/deal_with_it.png)
### Let's Experiment
![char_x.png](/ja_jp/reversi/let's_experiment.png)
### Galaxy
![char_x.png](/ja_jp/reversi/galaxy.png)
### iPhone X
![char_x.png](/ja_jp/reversi/iphone_x.png)
### Islands
![char_x.png](/ja_jp/reversi/islands.png)
### 6x8
![char_x.png](/ja_jp/reversi/6x8.png)
### Spark
![char_x.png](/ja_jp/reversi/spark.png)
### Triangle
![char_x.png](/ja_jp/reversi/triangle.png)
### Two Board
![char_x.png](/ja_jp/reversi/two_board.png)


## Test
まだ名前が付いていない、テスト中の盤面です。
### Test 1
![char_x.png](/ja_jp/reversi/test1.png)
### Test 2
![char_x.png](/ja_jp/reversi/test2.png)
### Test 3
![char_x.png](/ja_jp/reversi/test3.png)
### Test 4
![char_x.png](/ja_jp/reversi/test4.png)


### Test 6
![char_x.png](/ja_jp/reversi/test6.png)
### Test 7
![char_x.png](/ja_jp/reversi/test7.png)
### Test 8
![char_x.png](/ja_jp/reversi/test8.png)

# その他
## 藍との対戦
藍との対戦はTLから「@ai リバーシ」を含む命令で行うことができる（インスタンスによって藍のユーザー名が異なる場合があるので、気をつけていただきたい）。

# 外部リンク
- ４×４オセロ全手解析 http://www.net.c.dendai.ac.jp/~ksuzuki/
4×4リバーシを手動で完全解析した方のページ。

