---
title: Misskey.io
description: Misskey.ioは、Misskeyのサーバー。syuiloが運営し村上さんがサーバー資源を提供する。
published: true
date: 2024-02-06T15:14:25.382Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:46:24.548Z
---

[**Misskey.io**](https://misskey.io)は、[Misskey HQ](/group/misskeyhq)が運営している[Misskey](/software/misskey)サーバーです。
かつて公式インスタンスとして[misskey.xyz](/instances/misskey_xyz)が運営されていましたが、v11(daybreak)にてデータベースソフトウェアの変更が行われた際に長期運用によるデータの破損等から移行が難しいと判断されたため後継としてMisskey.ioが新規に開設されました。しかし、現在Misskey.ioは公式サーバーではありません ^[村上さんによるノート https://misskey.io/notes/99kpfiw8ku] ^[しゅいろによるノート https://misskey.io/notes/9aqm5ec6x1] ^[しゅいろによるノート https://misskey.io/notes/9bd9z2yics]。

# 独自機能
Misskey.ioは[Github misskey-dev](https://github.com/misskey-dev/misskey)のソースコードをそのまま使っているわけではなく独自に機能を追加している。(github.com/MisskeyIO/misskey/tree/io で公開されている。)


## 独自効果音の追加
ノート受信や通知などで流れる効果音について、Misskeyに付属している効果音の他に独自の専用ボイスを選択できるようになっている。

<!--
## 検索機能の強化
強化された検索構文はv13移行に伴い廃止されました。

`since:` `until:` `host: ` のキーワードが使用できる。

2021年1月1日〜
`since:2021-01-01 キーワード`

〜2021年1月31日
`until:2021-01-31 キーワード`

2021年1月1日〜1月31日
`since:2021-01-01 until:2021-01-31 キーワード`

mstdn.jpから検索する
`host:mstdn.jp キーワード`

Misskey.io内で検索する
`host:local キーワード`

## 独自RSSフィード
Misskey.ioでRSSウィジェットを追加した場合、デフォルトで[Misskey.ioユーザーが興味のありそうな](https://misskey.io/notes/8u54uauvae)記事を表示するようになっている。

独自RSSフィードはv13移行に伴い廃止されました。
-->


# 歴史
*[Misskey#歴史](/software/misskey)も参照*

- 2020年12月8日 LTLを毎日定期的に開放するように
- 2020年6月 LTLを常時開放するように
- 2021年8月14日 GDPR/UK GDPRへの対応が困難なことからEU加盟国およびイギリスからの登録が禁止に
- 2021年9月10日 児童への安全性やプライバシー保護の観点から13歳未満の登録が禁止に
- 2021年10月1日 登録がメールアドレス必須に
- 2021年10月3日 データベースが破損し、直近のバックアップも壊れていたため長時間のメンテナンスを経て2021年4月16日のデータに巻き戻された。
  4月16日以降のデータは他のインスタンスには残されているものの、その期間に作られたアカウント含めmisskey.io側からは存在しない扱いになっており一切の操作ができない。


# 関連項目
- [co.misskey.io](/ja/instances/misskey_io/co_misskey_io)
- [demo.misskey.io](/ja/instances/misskey_io/demo_misskey_io)
- [mc.misskey.io](/ja/instances/misskey_io/mc_misskey_io)
- [syuilo](/persons/syuilo)
- [村上さん](/persons/aureoleark)
- [ゆずりょー](/persons/yuzuryo61)
- [aqz](/persons/aqz)

# 公式アカウント
- [@notify（お知らせ）](https://misskey.io/@notify)
- [@support（サポート）](https://misskey.io/@support)
- [@admin（管理用）](https://misskey.io/@admin)
- [@official（グッズ等）](https://misskey.io/@official)

その他、Misskey HQ によって本人確認が行われたアカウントには Official ロールが付与されている。

# 関連リンク
<!--
利用規約URLの遍歴
- [利用規約](https://github.com/MisskeyIO/policy)
- [プライバシーポリシー](https://github.com/MisskeyIO/policy)
↓
- [利用規約](https://service.misskey.io/ja/tos)
↓
- [利用規約](https://support.misskey.io/hc/ja/articles/6564530842767)
- [プライバシーポリシー](https://support.misskey.io/hc/ja/articles/6861195754255)
-->
- [利用規約](https://go.misskey.io/tos)
- [プライバシーポリシー](https://go.misskey.io/policy)
- [サポートデスク](https://support.misskey.io/hc/ja)
- [Misskey.io Status](https://status.misskey.io/)
- [Misskey.io Tools](https://tools.misskey.io/)
- [公式Discord](https://go.misskey.io/discord)
- ~~[Patreon](https://www.patreon.com/m/misskeyio)~~(Patreon運営により削除されました)
- ~~[Patreon連携](https://link.misskey.io)~~(調整中)
- [pixivFANBOX](https://misskeyhq.fanbox.cc)
- [広告掲載](https://service.misskey.io/ads)
