---
title: クライアント
description: 投稿したりタイムラインを表示したりできるアプリ・ソフトウェア
published: true
date: 2025-05-11T02:54:14.095Z
tags: 
editor: markdown
dateCreated: 2022-05-03T06:30:29.644Z
---

<!-- 項目が大きくなったらこのページをディレクトリ化する -->
Misskeyの機能をひととおり利用できる、いわゆる「クライアント」と呼ばれるアプリ・ソフトウェアの一覧。  

また、ブラウザの機能を利用してMisskey標準のWebクライアントをアプリのようにインストールすることもできる（[下記参照](#misskey-web%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B)）ので、こちらも検討されたい。

# アプリの一覧
## マルチOS
### Miria
- OS: Android, iOS, macOS, Windows, Linux
- Flutter

[そらいろ](https://misskey.io/@shiosyakeyakini)氏による無料のMisskeyクライアント。
複数アカウントでログイン可能であり、タブ移動がしやすいのが特徴的である。また、WebViewを使わずに[MFM](../function/mfm)表示が可能な数少ないクライアントでもある。Misskeyの大幅な機能更新に積極的に追従している。
Flutterベースのため、FlutterがサポートするWeb以外の環境すべてで動作する。
Windows版及びLinux（Snapパッケージ）版は[GitHub Releases](https://github.com/shiosyakeyakini-info/miria/releases)からダウンロードできる。

**[Miria公式サイト](https://shiosyakeyakini.info/miria_web/index.html)**
**[MiriaをAppStoreでインストール🍎](https://apps.apple.com/jp/app/miria/id6449201469)**
**[MiriaをPlayStoreでインストール🤖](https://play.google.com/store/apps/details?id=info.shiosyakeyakini.miria)**
[shiosyakeyakini-info/miria on GitHub](https://github.com/shiosyakeyakini-info/miria)

### Aria
- OS: Android, iOS, macOS, Windows, Linux
- Flutter, Rust

[poppingmoon](https://github.com/poppingmoon)氏によって開発されているMiriaからフォークされた無料のMisskeyクライアント。

Miriaに搭載された機能の他、Rustで実装された[AiScript](/function/AiScript) (Misskey Play)をアプリ上で利用することができるクライアントである。

**[Aria公式アカウント](https://misskey.io/@aria_app)**
**[AriaをAppStoreでインストール🍎](https://apps.apple.com/app/aria-for-misskey/id6499410880)**
**[AriaをGooglePlayでインストール🤖](https://play.google.com/store/apps/details?id=com.poppingmoon.aria)**
**[AriaをSnapStoreでインストール🐧](https://snapcraft.io/aria)**
[poppingmoon/aria on GitHub](https://github.com/poppingmoon/aria)

### TheDesk
- OS: Windows, macOS, Linux  
- Node.js, Electron

[Cutls P](https://2m.cutls.com/@Cutls)氏による無料のマルチカラム対応Mastodonクライアント。  
Misskeyに対応していたが[v24(Anastasia)よりサポートが削除された](https://github.com/cutls/TheDesk/releases/tag/v24.0.0)。
その後、Mastodon APIに対応したMisskeyインスタンス「~~[kids鯖](https://kids.0px.io/)~~」のサービスが開始された（2025年現在はサービスを終了している）。
v25から[Fedistar](https://fedistar.net)をベースとして再構築されており、Misskeyを部分的にサポートしている。

**[TheDesk公式サイト](https://thedesk.top/)**  
~~**[TheDeskをMicrosoftStoreでインストール🪟](https://www.microsoft.com/store/productId/9P2NDNZ0GWZF)**~~
**[TheDeskをSnapStoreでインストール🐧](https://snapcraft.io/thedesk)**
[cutls/TheDesk on GitHub](https://github.com/cutls/TheDesk) v24以前のコード。アーカイブ済み。
[cutls/thedesk-next on GitHub](https://github.com/cutls/thedesk-next)

## iOS/iPadOS
### MissFARM
[高橋牧場](https://misskey.io/@SvEzs)氏が開発している無料のMisskeyクライアント。
Twitterアプリに近い操作感でMisskeyを利用することができる。

**[MissFARMをAppStoreでインストール🍎](https://apps.apple.com/jp/app/id6468420277)**

### SocialHub
[akihiro（うるし）](https://misskey.io/@U_Akihir0)氏が開発している有料のiPhone向けマルチSNSクライアント。v1.5（2020年4月27日リリース）よりMisskeyに対応。  
akihiro氏は、かつて人気を博したTwitterクライアント『TheWorld』の作者であり、SocialHubは、TheWorldの後継アプリとして開発されている。  
複数のSNSをひとつのアプリで操作できることが最大の特徴であり、2023年7月19日時点で𝕏, Mastodon, Slack, Tumblr, Pleroma, Pixelfed, Bluesky,そしてMisskeyの8種をサポートしている。

**[SocialHubをAppStoreでインストール🍎](https://apps.apple.com/jp/app/id1474451582)**
[uakihir0/SocialHub on GitHub](https://github.com/uakihir0/SocialHub)

## Android
### MilkTea
[パン太](https://misskey.io/@Panta)氏が開発している無料のAndroid向けMisskey・Mastodonクライアント。

> 2024年9月まで開発が続けられている一方、2023年12月以降PlayStoreの更新がされておらず、バージョンが乖離している。{.is-info}


**[MilkTeaをPlayStoreでインストール🤖](https://play.google.com/store/apps/details?id=jp.panta.misskeyandroidclient)**
[pantasystem/Milktea on GitHub](https://github.com/pantasystem/Milktea)

### ぞーぺん(ZonePane)
[たけうちひろあき](https://fedibird.com/@takke)氏が開発している無料のAndroid用Mastodon・Misskey・Blueskyクライアント。
ZonePaneは、Twitterの人気クライアント『TwitPane』の後継アプリであり、TwitPaneと同じUIで利用することができる。
アプリ内広告は広告解除パックの定期購入により削除可能。

**[ZonePane公式アカウント](https://fedibird.com/@zonepane)**
**[ZonePaneをPlayStoreでインストール🤖](https://play.google.com/store/apps/details?id=com.zonepane)**
[ZonePaneをDeployGateでインストール🤖](https://deploygate.com/distributions/5059f5a50da677b5eed9081b46cf48753658662a)

## Misskeyのサポートを終了したアプリ
> ここでは、2025年3月現在Misskeyのサポートを終了したアプリについて解説しています。これらのアプリでは一部Misskeyの機能が正常に動作しない可能性があります。{.is-warning}
### MissCat
[wada](https://misskey.io/@wada)氏が開発している無料のiPhone・iPad向けMisskeyクライアント。2020年4月3日にβ版が[リリースされた](https://misskey.io/notes/85nl8qgjsf)。

2025年5月頃、App Storeから削除された。

**[MissCat公式サイト](https://yuiga.dev/misscat/)**  
~~**[MissCatをAppStoreでインストール🍎](https://apps.apple.com/jp/app/id1505059993)**~~
[YuigaWada/MissCat on GitHub](https://github.com/YuigaWada/MissCat)

### Subway Tooter
[tateisu](https://mastodon.juggler.jp/@tateisu)氏が開発している無料のAndroid向けMastodonクライアント。現在はMisskeyはサポート外となっている。2.7.0よりMisskeyに対応していたが、5.519にて[サポートを終了](https://github.com/tateisu/SubwayTooter/releases/tag/v5.519)している。

**[Subway TooterをPlayストアでインストール🤖](https://play.google.com/store/apps/details?id=jp.juggler.subwaytooter&hl=ja)**
[tateisu/SubwayTooter on GitHub](https://github.com/tateisu/SubwayTooter)  
[Subway Tooter Blog](http://subwaytooter.hatenadiary.jp/)  
[Subway Tooter @SubwayTooter@mastodon.juggler.jp](https://mastodon.juggler.jp/@SubwayTooter)   

### Whalebird
- OS: Windows, macOS, Linux  
- Node.js, Electron

[h3poteto](https://pleroma.io/users/h3poteto)氏による無料のMastodon/Pleromaクライアント。
[megalodonのMisskeyサポート終了](https://h3poteto.hatenablog.com/entry/2023/09/25/220706)に伴いMisskeyのサポートを終了し、代わりにFirefishをサポートしている。

**[Whalebird公式サイト](https://whalebird.social/ja)**
**[WhalebirdをMicrosoftStoreでインストール🪟](https://apps.microsoft.com/store/detail/whalebird/9NBW4CSDV5HC)**
**[WhalebirdをMacAppStoreでインストール🍎](https://apps.apple.com/jp/app/whalebird/id6445864587)**
**[WhalebirdをSnapStoreでインストール🐧](https://snapcraft.io/whalebird)**
[h3poteto/whalebird-desktop on GitHub](https://github.com/h3poteto/whalebird-desktop)
# Misskey Webをインストールする
Misskey Webは、モバイルOSやブラウザの機能によってストアアプリのようにホーム画面に登録することができる。
追加されたアイコンからMisskeyを起動した場合、ブラウザのアドレスバーが表示されず、ストアからダウンロードしたアプリのように全画面で表示される。


## Chrome
Google Chromeを使うと、Android（またはデスクトップOS）でネイティブアプリケーションのように端末へMisskeyをインストールできる。
MisskeyをChromeからインストールすると、次のようになる。

- ホーム画面（デスクトップ）にMisskeyアイコンが表示され、直接起動できるようになる
  * ここから起動した場合、アドレスバーが表示されない。
- Androidの共有メニューにMisskeyが表示されるようになる

### 追加方法
1. ChromeでMisskeyを開く
2. 右上の「︙」をタップ（クリック）しメニューを表示
3. 「ホーム画面に追加（Misskeyをインストール）」をタップ
4. ポップアップが出てくるので、「追加（インストール）」をタップ

以上の手順を踏むと、Misskeyがホーム画面（デスクトップ）に追加される。

ChromeでMisskeyを直接何度か開いていると、「ホーム画面に Misskey を追加」というバナーが現れることがあり、それをタップすることでも同様のことが行える。

参照：[プログレッシブ ウェブアプリを利用する - Google Chrome ヘルプ](https://support.google.com/chrome/answer/9658361?hl=ja&co=GENIE.Platform%3DAndroid&oco=1)

## iOS Safari
1. SafariでMisskeyを開く
2. 下部中央の共有アイコンをタップ
3. 下段の「[+]ホームに追加」をタップ

以上の手順を踏むと、Misskeyがホーム画面に追加される。

参照：[iPhoneのSafariでWebサイトをブックマークに登録する - iPhoneユーザーガイド](https://support.apple.com/ja-jp/guide/iphone/iph42ab2f3a7/ios) 

