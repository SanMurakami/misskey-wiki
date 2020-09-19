---
title: Misskey
description: 
published: true
date: 2020-09-19T17:40:11.825Z
tags: 
editor: markdown
dateCreated: 2020-09-19T17:40:11.825Z
---

**Misskey**は、2014年から[syuilo](/persons/syuilo)により開発されているオープンソースの[分散マイクロブログソフトウェア](/decentralized-social-networking-service#%E5%88%86%E6%95%A3%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%83%96%E3%83%AD%E3%82%B0%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2)である。***A forever evolving, sophisticated microblogging platform.***（いつまでも進化する、洗練されたマイクロブログSNS）をスローガンにしている。

Misskeyはオープンソースソフトウェアで、ソースコードはAGPLv3ライセンスの下でほぼ自由に利用できる。
そのため、自分でインスタンスを建てて運営することができる。

Misskeyという名前はMay'nの楽曲「Brain Diver」の歌詞から採られている（syuiloが名前を考えていたときにたまたま聴いていた）。

# 歴史
Misskeyは大きなバージョンアップごとにコードネームが変わる。
コードネームは、*aoi*、*nighthike*、*daybreak*、*indigo*のように変わってきている。現在のコードネームは*indigo*である。

*2018年8月以降の出来事については[Misskeyをはじめようのブログ](https://joinmisskey.github.io/ja/blog/)を、Misskey自体の変更については[リリースノート](https://github.com/syuilo/misskey/blob/develop/CHANGELOG.md)も参照。*

## nighthike以前(swallowtail、aoi等)の時代 (2014/6~)
- 2014年6月 開発開始と思われる
- 2014年7月 試験的な運用が始まる
- 2014年8月 本格的に運用が始まる
- 2014年9月 しゅいろのミスでデータ全消滅
- 2014年9月上旬 DDOS攻撃を受ける
- 2015年2月 [misskey.xyz](/ja/instances/misskey-xyz)死亡
- 2015年2月 misskey.xyz復活
- 2015年3月 misskey.xyz死亡
- 2015年4月 misskey.xyz復活（データ全消滅）
- 2015年7月 資金難でmisskey.xyz死亡
- 2015年8月 misskey.xyz復活（データ全消滅）
- 2015年12月 misskey.xyz復活（データ全消滅）
- 2016年3月 misskey.xyz死亡
- 2016年 いろいろミラーができたりなくなったり
- 2016年8月 misskey.xyz復活
- 2017年8月 [aqz](/ja/persons/aqz)がzawazawaグループ（2世代前のWiki）を発足。
- 2017年9月20日 セキュリティ上のミスがあり一部データ喪失。
- 2018年3月24日 サイトダウン [^1]
  - ConoHaのチャージが尽きたため、サイトがダウン。しかし寄付により同日中に復活。

## nighthike時代 (2018/4~)
- 2018年4月8日 nighthikeがリリース[^2]
  - [ActivityPub](/ja/activitypub)に対応。コードネームをnighthikeと改称。分散型SNSとしての道を歩み始める。これをきっかけに、他の連合型SNSソフトの開発・運営者に知られ、Misskeyの知名度が急上昇した。
- 2018年4月10日 himasaku.netに避難[^3]
  - CloudFlareのCDNが未知の理由で破壊され、misskey.xyzがダウン。翌日、CloudFlareを外して復活
- 2018年4月 このころ、i18nなどの多言語化や、インスタンスの立て方などのユーザーコンテンツが整備され始める。
- 2018年4月15日
  - ~~[OpenCollective](https://opencollective.com/misskey)~~と[Patreon](https://www.patreon.com/syuilo)のアカウント開設。
  - misskey.wtf開設
    * Knzk.me氏によって開設→現在は閉鎖
- 2018年7月10日 [joinmisskey](/joinmisskey)がaqzにより開設される。
- 2018年8月11日 Hostdonのベータプログラムとして、初のMisskeyホスティングサービスの募集申込みが始まる [記事](https://joinmisskey.github.io/ja/blog/2018/08/12_3_hostdon/)
- 2018年8月12日 Wiki機能をzawazawaからjoinmisskeyに移管。zawazawaは閉鎖。
- 2018年8月20日 misskey.xyzが数時間ダウンするものの、村上さんの手により蘇生。 [^4]

## daybreak時代 (2019/4~)
- 2019年4月14日 データベースソフトウェアにPostgreSQLを採用したv11がリリースされる。コードネームをdaybreakとした。
- 2019年4月15日 v11移行に伴い、データの移行が難しいと判断されたため、misskey.xyzから[misskey.io](/ja/instances/misskey-io)への引っ越しが決定された。misskey.ioが新規に作られ、misskey.xyzの新規登録が停止した。
- 2019年5月31日 この日を以てmisskey.xyzが閉鎖された。
- 2019年6月3日 Misskey Wikiが開設される。joinmisskeyからWiki機能を移動開始。

## indigo時代 (2020/2~)
- 2020年2月6日 v12がリリースされる。コードネームをindigoとした。

# 主要なフォーク
## nighthikeベース
- [めいすきー](/meisskey)
- [twista](/twista)

## daybreakベース

- [Groundpolis (~v2)](/ja/software/groundpolis)

## indigoベース

- [Groundpolis (v3~)](/ja/software/groundpolis)


# 外部リンク
- [GitHub syuilo/misskey](https://github.com/syuilo/misskey)
- [Misskeyをはじめよう](https://joinmisskey.github.io)

[^1]: https://twitter.com/syuilo/status/977270402786344960
[^2]: https://twitter.com/misskey_io/status/982910410461343745
[^3]: https://twitter.com/syuilo/status/983634753977909253
[^4]: https://joinmisskey.github.io/ja/blog/2018/08/20_2_ddos/