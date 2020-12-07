---
title: リバーシ
description: Misskeyで利用できるゲームの一つ
published: true
date: 2020-12-07T09:49:48.928Z
tags: 
editor: markdown
dateCreated: 2020-09-20T09:28:37.880Z
---

**リバーシ**とは最新版の[Misskey Games](/games)で遊ぶことができるゲームの一つだ。v12.52.0で復活した。
この項目ではリバーシの遊び方やルール説明の他、Misskey_v12に実装されている全リバーシマップを記載する。

# 遊び方
Misskeyユーザであれば誰でもプレイすることができる。左にあるサイドパネルから「もっと！」を押し、そこに出てきたポップアップメニューから Misskey Games を押せば自動的にMisskeyリバーシのページに飛ばされる仕組みとなっている。
ユーザとの対戦はゲーム内の「招待」から指定して、相手の承諾があれば開始できる。また、招待からのユーザー選択で対話型botである[藍](/aichan)を指定することも出来る。なお、藍と対戦する時のみに[Botのオプション](/reversi#Botのオプション)が追加される。
# ルール
通常のリバーシの盤面以外にも、様々な大きさ、形、初期配置の盤面を利用できる。ゲーム開始前にお互いに盤面を自由に編集することもできる。
## 基本ルール
交互に盤面へ石を打ち、相手の石を自分の石で挟むと その石を 自分の色の石に変えることが出来る。そして最終的に自分の石が最も多いプレイヤーが勝者となる。
## 先行/後攻

## ロセオ
石の少ない方が勝ちとなるルールである。
## どこでも置けるモード

## ループマップ
盤面の上下左右がループするモードである。

## Botのオプション

藍との対戦はTLから「@ai リバーシ」を含む命令で行うことができる（インスタンスによって藍のユーザー名が異なる場合があるので、気をつけていただきたい）。
また、藍との対戦のみプレイヤーの難易度を調整できる。


# 4x4
4×4マスの正方形盤を使うとても小さな盤面。主要時間はおおよそ1分なので、サクッと気軽に試合が出来る。また、三目並べ感覚で簡単に二人零和有限確定完全情報ゲームが楽しめるので、初歩的なゲーム理論の理解にも役立つかもしれない。
## 4x4

![char_x.png](/ja_jp/reversi/4x4.png)

# 6x6
## 6x6
![char_x.png](/ja_jp/reversi/6x6.png)
## 6x6 Rounded
![char_x.png](/ja_jp/reversi/6x6_rounded.png)
## 6x6 Rounded 2
![char_x.png](/ja_jp/reversi/6x6_rounded_2.png)

# 8x8
8×8マスの正方形盤を使う盤面。みんな知ってる定番のリバーシ。
## 8x8
![char_x.png](/ja_jp/reversi/8x8.png)
## 8x8 Handicap 1
![char_x.png](/ja_jp/reversi/8x8_handicap_1.png)
## 8x8 Handicap 2
![char_x.png](/ja_jp/reversi/8x8_handicap_2.png)
## 8x8 Handicap 3
![char_x.png](/ja_jp/reversi/8x8_handicap_3.png)
## 8x8 Handicap 4
![char_x.png](/ja_jp/reversi/8x8_handicap_4.png)
## 8x8 Handicap 28
![char_x.png](/ja_jp/reversi/8x8_handicap_28.png)
## 8x8 with notch
![char_x.png](/ja_jp/reversi/8x8_with_notch.png)
## 8x8 with some holes
![char_x.png](/ja_jp/reversi/8x8_with_some_holes.png)
## 8x8 Rounded
![char_x.png](/ja_jp/reversi/8x8_rounded.png)
## 8x8 Rounded 2
![char_x.png](/ja_jp/reversi/8x8_rounded_2.png)
## 8x8 Rounded 3
![char_x.png](/ja_jp/reversi/8x8_rounded_3.png)
## Circle
![char_x.png](/ja_jp/reversi/circle.png)
## Lack of black
![char_x.png](/ja_jp/reversi/lack_of_black.png)
## Minesweeper
![char_x.png](/ja_jp/reversi/minesweeper.png)
## Parallel
![char_x.png](/ja_jp/reversi/parallel.png)
## Reserved
![char_x.png](/ja_jp/reversi/reserved.png)
## Smile
![char_x.png](/ja_jp/reversi/smile.png)
## Square Party
![char_x.png](/ja_jp/reversi/square_party.png)
## Window
![char_x.png](/ja_jp/reversi/window.png)
## X
![char_x.png](/ja_jp/reversi/x.png)
# 10x10
グランドリバーシ。
## 10x10
![char_x.png](/ja_jp/reversi/10x10.png)
## Arena
![char_x.png](/ja_jp/reversi/arena.png)
アリーナマップ。
## Char X
![char_x.png](/ja_jp/reversi/char_x.png)
## Char Y
![char_x.png](/ja_jp/reversi/char_y.png)
## Checker
![char_x.png](/ja_jp/reversi/checker.png)
## CPU
![char_x.png](/ja_jp/reversi/cpu.png)
## Cross
![char_x.png](/ja_jp/reversi/cross.png)
アネクゼイションとも。
## Grid
![char_x.png](/ja_jp/reversi/grid.png)
## The Hole
![char_x.png](/ja_jp/reversi/the_hole.png)
## Japanese Curry
![char_x.png](/ja_jp/reversi/japanese_curry.png)
## Mosaic
![char_x.png](/ja_jp/reversi/mosaic.png)
## Reactor
![char_x.png](/ja_jp/reversi/reactor.png)
## Walls
![char_x.png](/ja_jp/reversi/walls.png)

# Special
常識の枠に捉えられない独特な盤面です。
## Big Board
![char_x.png](/ja_jp/reversi/big_board.png)
## Deal with it!
![char_x.png](/ja_jp/reversi/deal_with_it.png)
## Let's Experiment
![char_x.png](/ja_jp/reversi/let's_experiment.png)
## Galaxy
![char_x.png](/ja_jp/reversi/galaxy.png)
## iPhone X
![char_x.png](/ja_jp/reversi/iphone_x.png)
## Islands
![char_x.png](/ja_jp/reversi/islands.png)
## 6x8
![char_x.png](/ja_jp/reversi/6x8.png)
## Spark
![char_x.png](/ja_jp/reversi/spark.png)
## Triangle
![char_x.png](/ja_jp/reversi/triangle.png)
## Two Board
![char_x.png](/ja_jp/reversi/two_board.png)


# Test
まだ名前が付いていない、テスト中の盤面です。
## Test 1
![char_x.png](/ja_jp/reversi/test1.png)
## Test 2
![char_x.png](/ja_jp/reversi/test2.png)
## Test 3
![char_x.png](/ja_jp/reversi/test3.png)
## Test 4
![char_x.png](/ja_jp/reversi/test4.png)


## Test 6
![char_x.png](/ja_jp/reversi/test6.png)
## Test 7
![char_x.png](/ja_jp/reversi/test7.png)
## Test 8
![char_x.png](/ja_jp/reversi/test8.png)


# 外部リンク
- ４×４オセロ全手解析 http://www.net.c.dendai.ac.jp/~ksuzuki/
4×4リバーシを手動で完全解析した方のページ。

