---
title: インスタンスの構築方法
description: 自分でインスタンスを構築する方法について
published: true
date: 2021-09-16T18:08:54.558Z
tags: 
editor: markdown
dateCreated: 2021-03-12T17:26:39.490Z
---

Misskeyにおける最大の特徴の一つが「オープンソース」ということだ。これはつまりMisskeyを構築するためのコードは[全てネット上で無償公開](https://github.com/misskey-dev/misskey)されており、<small>(やる気さえあれば)</small>**誰でも自分だけのソーシャルネットワークをゼロから構築できるということ**だ。
このページでは主にAmazon Web Service(アマゾン・ウェブ・サービス、通称:AWS)を用いたMisskeyサーバーの構築方法を解説する。

# AWSで自分だけのMisskeyインスタンスを構築する方法完全解説
まずはこのあやしいサイトを見てもらいたい：https://aws.amazon.com/jp/
![スクリーンショット_2021-01-10_19-17-09.png](/ja_jp/wiki_guide/aws/スクリーンショット_2021-01-10_19-17-09.png)
「今すぐ無料サインアップ」で妙に急かしてきたり、「あと少しで AWS アカウントの作成が完了します」のAWSの単語に微妙なスペースが入っていたり、改行とかとても本家Amazonとは思えない焦りっぷりだ。ここでまず一番にすることは、そう。
## 証明書の確認
![スクリーンショット_2021-01-10_19-17-09_2.png](/ja_jp/wiki_guide/aws/スクリーンショット_2021-01-10_19-17-09_2.png)
このアドレスバー左にある鍵マークをクリックして...
![スクリーンショット_2021-09-17_02-50-07.png](/ja_jp/wiki_guide/aws/スクリーンショット_2021-09-17_02-50-07.png)
...このサイトが本当にAmazon社によるものなのかをチェックすることだ。
![aws_cert_check_one_2021-09-17_03-01-24.png](/ja_jp/wiki_guide/aws/aws_cert_check_one_2021-09-17_03-01-24.png)
「証明書を表示」をクリックすると、そのサイトの証明書を発行した国や組織が出てくるようになっている。ここに`国	US`と`組織	Amazon`と出ていればひとまず問題ないだろう。
![aws_cert_honmaka_2021-09-17_02-57-55.png](/ja_jp/wiki_guide/aws/aws_cert_honmaka_2021-09-17_02-57-55.png)
ふむ。どうやら本物っぽいな。

まぁ本物ならよいとして、まず手始めにAWSのアカウントを作る。


# Raspberry Piで簡単にMisskeyインスタンスを構築する方法

MisskeyはVPSなどのサービス利用することで簡単に構築することができます。
お一人でご利用される場合は、Raspberry Pi 4B 4GB程度のスペックで十分に動作します。

基本的な構築手順は、[Misskeyリポジトリの「Misskey構築の手引き」](https://github.com/misskey-dev/misskey/blob/master/docs/setup.ja.md)にて解説されています。

# Dockerを使った構築方法の解説

[Misskeyリポジトリには、Dockerを使った構築方法](https://github.com/misskey-dev/misskey/blob/develop/docs/docker.ja.md)についても解説書があります。