---
title: インスタンスの構築方法
description: 自分でインスタンスを構築する方法について
published: true
date: 2021-09-16T07:05:53.987Z
tags: 
editor: markdown
dateCreated: 2021-03-12T17:26:39.490Z
---

Misskeyにおける最大の特徴の一つが「オープンソース」ということだ。これはつまりMisskeyを構築するためのコードは[全てネット上で無償公開](https://github.com/misskey-dev/misskey)されており、<small>(やる気さえあれば)</small>**誰でも自分だけのソーシャルネットワークをゼロから構築できるということ**だ。
このページでは主にAmazon Web Service(アマゾン・ウェブ・サービス、通称:AWS)を用いたMisskeyサーバーの構築方法を解説する。

# AWSで自分だけのMisskeyインスタンスを構築する方法完全解説するよ
まずはこのあやしいサイトを見てもらいたい：https://aws.amazon.com/jp/







# Raspberry Piで簡単にMisskeyインスタンスを構築する方法

MisskeyはVPSなどのサービス利用することで簡単に構築することができます。
お一人でご利用される場合は、Raspberry Pi 4B 4GB程度のスペックで十分に動作します。

基本的な構築手順は、[Misskeyリポジトリの「Misskey構築の手引き」](https://github.com/misskey-dev/misskey/blob/master/docs/setup.ja.md)にて解説されています。

# Dockerを使った構築方法の解説

[Misskeyリポジトリには、Dockerを使った構築方法](https://github.com/misskey-dev/misskey/blob/develop/docs/docker.ja.md)についても解説書があります。