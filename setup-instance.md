---
title: インスタンスの構築方法
description: 自分でインスタンスを構築する方法について
published: true
date: 2021-03-12T17:26:39.490Z
tags: 
editor: markdown
dateCreated: 2021-03-12T17:26:39.490Z
---

# 自分のサーバーにインストールする
まず、VPSないしは自宅などにサーバーを用意し、Misskeyをインストールする方法がある。
サーバーと言っても、一人で使うならRaspberry Pi 4B 4GBで十分に動作する。

基本的な手順は、[Misskeyリポジトリの「Misskey構築の手引き」にて解説されて](https://github.com/syuilo/misskey/blob/master/docs/setup.ja.md)いる。まずこの手引きを読んで、大まかな手順を理解しよう。

## Misskey Site!による解説
aqzによるブログ「Misskey Site!」にて、各種環境における詳細な構築手順書が公開されている。

https://misskey-site.com/posts/tag/misskey%e3%82%a4%e3%83%b3%e3%82%b9%e3%82%bf%e3%83%b3%e3%82%b9%e6%a7%8b%e7%af%89

## Dockerを使う
[Misskeyリポジトリには、Dockerを使った構築方法について](https://github.com/syuilo/misskey/blob/develop/docs/docker.ja.md)も解説書がある。これは、Dockerを自前でビルドするものだ。

# ホスティングサービス
misskey.ioのサーバー運用者である村上さんによって、ホスティングサービスが準備中だ。
