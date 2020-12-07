---
title: リバーシ
description: Misskeyで利用できるゲームの一つ
published: true
date: 2020-12-07T08:17:49.719Z
tags: 
editor: markdown
dateCreated: 2020-09-20T09:28:37.880Z
---

**リバーシ**はMisskeyで利用できるゲームの一つ。この項目では基本的な設定とMisskey_v12に実装されている全リバーシマップを解説する。


ユーザや対話型botである[藍](/aichan)との対戦を行うことができる。

~~**ただし、執筆現在まだv12のクライアント側に実装されていない。**~~
v12.52.0で復活しました。

Misskeyユーザであれば誰でもプレイすることができる。ユーザとの対戦はゲーム内の「招待」から指定して、相手の承諾があれば開始できる。


通常のリバーシの盤面以外にも、様々な大きさ、形、初期配置の盤面を利用できる。ゲーム開始前にお互いに盤面を自由に編集することもできる。

## ロセオ
石の少ない方が勝ちとなるルールである。


## ループマップ
盤面の上下左右がループするモードである。


# 4x4
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
みんな知ってる定番のリバーシ。
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
## Big Board
## Deal with it!
## Let's Experiment
## Galaxy
## iPhone X
## Islands
## 6x8
## Spark
## Triangle
## Two Board


# Test
## Test 1
## Test 2
## Test 3
## Test 4
## Test 5
## Test 6
## Test 7
## Test 8






# 藍との対戦
藍との対戦はTLから「@ai リバーシ」を含む命令で行うことができる（インスタンスによって藍のユーザー名が異なる場合があるので、気をつけていただきたい）。
また、藍との対戦のみプレイヤーの難易度を調整できる。
