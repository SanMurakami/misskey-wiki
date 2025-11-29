---
title: 共有ページのクエリ
description: 共有ページ（/share）のクエリ一覧
published: true
date: 2025-11-29T04:52:58.084Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:45:30.772Z
---

Misskeyでは各サーバーの`/share`を開くことで、テキストが入力された投稿フォームを開くことができます。

# 各種パラメーターの詳細
`/share`以降に以下の各種パラメーターを複数付与することで、投稿フォームの内容を事前に設定することができます。
## リプライ情報
以下のいずれか

- **replyId**
  - リプライ先のノートid
- **replyUri**
  - リプライ先のUrl（リモートのノートオブジェクトを指定）

## Renote情報
以下のいずれか

- **renoteId**
  - Renote先のノートid
- **renoteUri**
  - Renote先のUrl（リモートのノートオブジェクトを指定）

## 公開範囲
- **visibility**
  - 公開範囲
  - `public`, `home`, `followers`, `specified`
> `specified`を指定する場合は`visibleUserIds`か`visibleAccts`の指定が必要です。
{.is-info}

- **localOnly**
  - 連合の有無
  - `0`(false), `1`(true)
- **visibleUserIds**
  - specified時のダイレクト先のユーザーid（カンマ区切り）
- **visibleAccts**
  - specified時のダイレクト先のacct（カンマ区切り）
  - `＠username`[`＠host`]

## ファイル
- **fileIds**
  - 添付したいファイルのid（カンマ区切りで）


# 共有フォーム中継サービス
[Misskey Hub](../website/misskeyhub)には**共有フォーム中継サービス**があり、Misskey Hubを経由することで、すべてのMisskeyサーバーに対応した共有リンクとして利用することができます。
![Misskey Hubの共有フォーム中継サービス](https://media.misskeyusercontent.jp/io/5f88b676-e485-409a-a805-1192709ee6a7.png)
前述の各種パラメーターを`https://misskey-hub.net/share/`以下に入力することで、ウェブページのリンクやゲームスコアを、ユーザーが所属するサーバーを意識することなく共有できます。