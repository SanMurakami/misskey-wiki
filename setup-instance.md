---
title: インスタンスの構築方法
description: 自分でインスタンスを構築する方法について
published: true
date: 2021-09-17T20:37:52.024Z
tags: 
editor: markdown
dateCreated: 2021-03-12T17:26:39.490Z
---

Misskeyにおける最大の特徴の一つが「オープンソース」ということだ。これはつまりMisskeyを構築するための手順からソースコードまで[全てネット上で無償公開](https://github.com/misskey-dev/misskey/blob/master/docs/setup.ja.md)されており、<small>(やる気さえあれば)</small>**誰でも自分だけのソーシャルネットワークをゼロから構築できるということ**だ。
このページでは主にAmazon Web Service(アマゾン・ウェブ・サービス、通称:AWS)を用いたMisskeyサーバーの構築方法を解説する。

# AWSで自分だけのMisskeyインスタンスを構築する方法完全解説
まずはこのあやしいサイトを見てもらいたい：https://aws.amazon.com/jp/
![スクリーンショット_2021-01-10_19-17-09.png](/ja_jp/wiki_guide/aws/スクリーンショット_2021-01-10_19-17-09.png)
「今すぐ無料サインアップ」や「今すぐ AWS で構築を始めましょう」と妙に急かしてきたり、「あと少しで AWS アカウントの作成が完了します」のAWSの単語に微妙なスペースが入っていたり、改行とかとても本家Amazonとは思えない焦りっぷりだ。ここでまず一番最初にすることは、そう。
## 証明書の確認
![スクリーンショット_2021-01-10_19-17-09_2.png](/ja_jp/wiki_guide/aws/スクリーンショット_2021-01-10_19-17-09_2.png)
このアドレスバー左にある鍵マークをクリックして`安全な接続`>`詳細を表示`>`セキュリティ`>...
![スクリーンショット_2021-09-17_02-50-07.png](/ja_jp/wiki_guide/aws/スクリーンショット_2021-09-17_02-50-07.png)
...このサイトが本当にAmazon社によるものなのかをチェックする！
![aws_cert_check_one_2021-09-17_03-01-24.png](/ja_jp/wiki_guide/aws/aws_cert_check_one_2021-09-17_03-01-24.png)
「証明書を表示」をクリックすると、そのサイトの証明書を発行した国や組織名が出てくるようになっている。ここに`国	US`と`組織	Amazon`と出ていればひとまず問題ないだろう。
![aws_cert_honmaka_2021-09-17_02-57-55.png](/ja_jp/wiki_guide/aws/aws_cert_honmaka_2021-09-17_02-57-55.png)
ふむ。どうやら本物っぽいな。

## AWSアカウントの作成
まぁ本物ならよいとして、まず手始めにAWSのアカウントを作る。
https://portal.aws.amazon.com/billing/signup#/start へアクセスし、AWSのいざこざが送られてきても問題の無いEメールアドレスと、パスワードマネージャーによって管理された超絶強力なパスワードを設定する。因みに筆者は[Firefox Lockwise](https://support.mozilla.org/ja/kb/getting-started-firefox-lockwise)をおすすめする。
![aws_signup_2021-01-10_19-18-36.png](/ja_jp/wiki_guide/aws/aws_signup_2021-01-10_19-18-36.png)
<center><small>最後の箱にある「AWSアカウント名」は後からでも変更できるので、かわいい名前にしても問題ない。</small></center>

色〻と記入したあと、こんな感じでサポートプランを聞かれるので、Basicのフリープランを選択しよう。お金ないし。
![aws_select_plan_2021-01-10_19-43-01.png](/ja_jp/wiki_guide/aws/aws_select_plan_2021-01-10_19-43-01.png)
そうすると...
![aws_welcome_aws_2021-01-10_19-43-42.png](/ja_jp/wiki_guide/aws/aws_welcome_aws_2021-01-10_19-43-42.png)
こんな感じでようこそスクリーンが表示される。おめでとう！これで今日から君もAWSマスターだよっ！`Sign in to the Console`から早速コンソールへサインインしよう。

...っと、これは？
## 主役「AWS無料利用枠」〜Free Tier
![aws_free_tier_2021-01-10_19-45-19.png](/ja_jp/wiki_guide/aws/aws_free_tier_2021-01-10_19-45-19.png)
そう、これは今回、いや、**今年**の主役：**AWSの12ヶ月無料利用枠**だ！！
言うのを完全に忘れていたが、筆者は天下のAmazon様に一錢たりとも落とすつもりはない。つまりMisskeyのインスタンスをAWSサーバーに完全無料で建てるつもりなのだーっ。

> 筆者が記事を書いた2021年のAWSには「12ヶ月無料利用枠」というのがあって、はじめてのユーザーさんに限って、一番ちっちゃいサーバーなら12ヶ月だけ無料で使ってもいいよーっていうサービスがあったんだよ！
{.is-info}

ちなみにこれが今回こっち側の道具として存分使わせてもらう[無料利用枠のFAQ](https://aws.amazon.com/jp/free/free-tier-faqs/)だ。
本解説は完全に無料で抑えようとするので、もし「お金は無いけど鯖は欲しい」って人が居れば、この[FAQ](https://aws.amazon.com/jp/free/free-tier-faqs/)をめっちゃ読もう。

## ようこそAWSへ！
<small>~~デジャヴかな？~~</small> 色々なボタンをポチポチした擧げ句、ついにこんな画面へとたどり着くことであろう。
https://aws.amazon.com/jp/getting-started/
![aws_getting_started_2021-01-10_21-01-58.png](/ja_jp/wiki_guide/aws/aws_getting_started_2021-01-10_21-01-58.png)
ここからまぁすぐにサーバー作ろうぜｗｗと続けて行ってもいいのだが、初心者さんなら（たとえ理解できなくても）まず[紹介動画](https://aws.amazon.com/jp/getting-started/fundamentals-overview/?e=gs2020&p=gsrc)と[AWSの主要概念](https://aws.amazon.com/jp/getting-started/fundamentals-core-concepts/?e=gs2020&p=gsrc)に目を通しておいて損は無いだろう。そんなに長くないし、ポップコーンでもつまんで見ましょうよ。

## Amazon EC2
さっきのドキュメンテーションちゃんと目を通したー？それならこちらからもおめでとう！もう君は実質AWS完全理解者と言っても差支へないことだろうーっ。
![aws_solution_list_2021-01-10_21-20-03.png](/ja_jp/wiki_guide/aws/aws_solution_list_2021-01-10_21-20-03.png)
さてと、今回はそんな星の数ほどあるAWSサービスのなかでもサーバーに関するもの...そう、[Amazon Elastic Compute Cloud](https://aws.amazon.com/jp/ec2/)、通称「EC2」を使って、Amazonの仮想サーバー上にMisskeyのインスタンスを建てて、世界中どこでもだれでもアクセスできちゃうSNSを構築しようって話なのですー！
![aws_ec2_2021-01-10_21-20-18.png](/ja_jp/wiki_guide/aws/aws_ec2_2021-01-10_21-20-18.png)
早速「Amazon EC2の使用を開始する」を押してみましょう！
そうすると...
![aws_ec2_console_first_2021-01-10_21-41-09.png](/ja_jp/wiki_guide/aws/aws_ec2_console_first_2021-01-10_21-41-09.png)
なんかこんな画面になりました！

ここからまず始めにするべきことは...えっと...あっ、そうだ。
### アベイラビリティゾーン
どこに自分のサーバーを置きたいか決めましょう！（大抵みんな東京に置くにゃ）
どこに自分のサーバーを置くのを決めるのは地味に大事です。だって例えば後に色〻作ってるときに全部別々の場所にあったら使えないから。（[因みに筆者は当初オハイオ州にセキュリティグループを作ったりオレゴン州にインスタンスを建ててしまったりで失敗しました](htps://misskey.io/notes/8gvtqd8mf2)）
![kawanerio_ohio_oregon_note_2021-09-17_07-28-20.png](/ja_jp/wiki_guide/aws/kawanerio_ohio_oregon_note_2021-09-17_07-28-20.png)

## セキュリティグループの作成
セキュリティグループとは所謂ファイアーウォール的なやつです。わるいウイルスとかの侵入を防ぐそうです。EC2はデフォルトで何もしなくても必ず初期設定としてセキュリティグループがついてくるそうです。
### アベイラビリティゾーンの再確認
まず自分のアベイラビリティゾーン（なんか右上に出てくる地名）を再確認しましょう。例えば東京にサーバーを建てたい場合は、[EC2コンソールへサインイン](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin#)し、自分のアベイラビリティゾーン（右上の地名）を`アジア・パシフィック（東京）ap-northeast-1`へと変更しましょう。
![aws_oregon_change_2021-09-17_07-05-23.png](/ja_jp/wiki_guide/aws/aws_oregon_change_2021-09-17_07-05-23.png)
アベイラビリティゾーンをしっかりと決めたら次にセキュリティグループを作成します。左下の`ネットワーク＆セキュリティ`にある`セキュリティグループ`をクリックします。
![aws_security_group_awrrow_2021-01-10_21-50-23.png](/ja_jp/wiki_guide/aws/aws_security_group_awrrow_2021-01-10_21-50-23.png)
セキュリティグループのページにこれたら、右上にあるオレンジ色の`セキュリティグループを作成`と書いてあるボタンを押します。
![aws_security_group_create_2021-01-10_21-50-23.png](/ja_jp/wiki_guide/aws/aws_security_group_create_2021-01-10_21-50-23.png)

> この[リンク](
https://ap-northeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-northeast-1#CreateSecurityGroup:)をクリックすると**東京のサーバーで**セキュリティグループを作成することができるよっ。 
https://ap-northeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-northeast-1#CreateSecurityGroup:
{.is-warning}

そうすると「セキュリティグループを作成」の画面にこれるハズだ。AWSはかなりユーザーフレンドリーで、殆どの記入欄の隣に「情報」リンクがあり、それらをクリックすることで自分が何をしているのかの詳細を知ることができる。

ここでは以下のことを記入する：
```
基本的な詳細
	セキュリティグループ名：local
	説明：local
  VPC：vpc-fc73909a（これはなんか勝手に記入されているやつなので無視でおｋ）
```
次に`インバウンドルール`から`ルールを追加`し、`タイプ`を`すべてのトラフィック`、`ソース`を`カスタム`の`172.0.0.0/6`へと設定。説明はまぁなんか適当に`local_inbound`とでも名付けておく。
![aws_securitygroup_create_2021-01-10_22-35-53.png](/ja_jp/wiki_guide/aws/aws_securitygroup_create_2021-01-10_22-35-53.png)
それじゃあアウトバウンドはどうなのさ？って思うだろ？これに関しては全く分からなかったので筆者はMisskeyの住民に問いかけることにした。
https://misskey.io/notes/8gvuifvotp
![misskey_note_aws_outbound_rule_2021-09-18_05-09-05.png](/ja_jp/wiki_guide/aws/misskey_note_aws_outbound_rule_2021-09-18_05-09-05.png)

> 当時はまだ[Misskey Forum](https://forum.misskey.io/)といった、便利な質問場がなかったんだよ！今ここでトラブルってる初心者さんは[Misskey Forum](https://forum.misskey.io/)で質問するか、[Misskey Discord](https://discord.com/invite/P4yYqYBjEp)等で聞いたほうが返信率があがると思うよ！
{.is-info}

そうするとなんとゐてるま氏から返信がっ!
https://misskey.io/notes/8gvwaibbe5
![misskey_note_aws_outbound_rule_reply_2021-09-18_05-19-04.png](/ja_jp/wiki_guide/aws/misskey_note_aws_outbound_rule_reply_2021-09-18_05-19-04.png)
目茶苦茶難解なことを言っているように感じるが、要は「触らなくておｋ」ということらしい。セキュリティグループを新規作成する際アウトバウンドルールはデフォルトで始めから`すべてのトラフィック`の`0.0.0.0/0`になってるのでそれで良いらしい。あれだ、「触らぬアウトバウンドルールにバグはなし」ってやつだ。

最後にタグをガン無視してページの一番下にある「セキュリティグループを作成」のボタンを押す。
![aws_create_security_group_2021-09-18_05-30-19.png](/ja_jp/wiki_guide/aws/aws_create_security_group_2021-09-18_05-30-19.png)
### おめでとう！
![aws_security_group_complete_2021-01-11_01-51-38.png](/ja_jp/wiki_guide/aws/aws_security_group_complete_2021-01-11_01-51-38.png)
ページ上部に「セキュリティグループが正常に作成されました」と表示されれば成功だ。おめでとう！
今度はVPCを編集するよ！
## Amazon VPC 編
Virtual Private Cloud
## CIDRの編集
## サブネットの編集
## Egress-Only インターネットゲートウェイの作成
## ルートテーブルの作成
### ルートの編集

## Amazon RDS 編
## データベースの作成

## Amazon ElastiCache

## Amazon S3 編
## バケットの作成

## Amazon CloudFront 編
## CloudFrontディストリビューションの作成

## EC2インスタンス！

## Amazon Machine Image

## キーペアの作成

## IPアドレスの編集

## ロードバランサーの設定

## 証明書のリクエスト

## ドメイン編
### 忘れてたドメインレジストレーション

## カスタムレコードの作成

## 証明書ふたたび──

## そしてSSHへ・・・
### インストール祭りだぜぇ！
#### Node.js
#### Git
#### ffmpeg

## 無料利用枠の嘆きその一「インスタンス上でのビルドが不可能」
### メモリが1GBしかなければ、ローカルでビルドして、成果物を送ればいいじゃない？



# Raspberry Piで簡単にMisskeyインスタンスを構築する方法

MisskeyはVPSなどのサービス利用することで簡単に構築することができます。
お一人でご利用される場合は、Raspberry Pi 4B 4GB程度のスペックで十分に動作します。

基本的な構築手順は、[Misskeyリポジトリの「Misskey構築の手引き」](https://github.com/misskey-dev/misskey/blob/master/docs/setup.ja.md)にて解説されています。

# Dockerを使った構築方法の解説

[Misskeyリポジトリには、Dockerを使った構築方法](https://github.com/misskey-dev/misskey/blob/develop/docs/docker.ja.md)についても解説書があります。

# 参考文献

AWSのサイト https://aws.amazon.com/jp/
AWS無料利用枠に関するよくある質問 https://aws.amazon.com/jp/free/free-tier-faqs/
AWSの基礎：紹介動画 https://aws.amazon.com/jp/getting-started/fundamentals-overview/?e=gs2020&p=gsrc
AWSの主要概念 https://aws.amazon.com/jp/getting-started/fundamentals-core-concepts/?e=gs2020&p=fundoverview