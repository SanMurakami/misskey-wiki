---
title: co.misskey.io
description: 常時LTL解放のmisskeyインスタンス
published: true
date: 2023-11-11T23:22:19.336Z
tags: 
editor: markdown
dateCreated: 2023-11-11T23:19:10.931Z
---

**co.misskey.io** とは、[syuilo](/ja/persons/syuilo)が運営するローカルタイムライン（LTL）が常時解放されたインスタンス。

# 概要
通称「**こみゅすきー**」。
[misskey.io](/ja/instances/misskey_io) は設立当時LTLが解放されていなかったため、LTLのコミュニティを楽しみたいユーザー向けにつくられた。2020年3月1日設立。

# 開発中Misskey試用の場として

co.misskey.io は2021年1月16日より開発中なリリース前のバージョンの misskey のコードに自動的に追従するようになっている。
技術的な言い方をすると、GitHub の Misskey リポジトリでは develop ブランチにコミットがあった場合、自動的に Docker image を作成し Docker Hub にアップロードするが、それを[30分に1回確認し](https://misskey.io/notes/8ugmh48jlu)更新があった場合に自動的に最新版に更新している。