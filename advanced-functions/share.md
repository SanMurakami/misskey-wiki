---
title: 共有ページのクエリ
description: 共有ページ（/share）のクエリ一覧
published: false
date: 2021-02-14T12:54:14.803Z
tags: 
editor: markdown
dateCreated: 2021-02-14T11:30:57.142Z
---

### リプライ情報
以下のいずれか

<dl>
<dt>replyId</dt>
<dd>リプライ先のノートid</dd>
<dt>replyUri</dt>
<dd>リプライ先のUrl（リモートのノートオブジェクトを指定）</dd>
</dl>

### Renote情報
以下のいずれか

<dl>
<dt>renoteId</dt>
<dd>Renote先のノートid</dd>
<dt>renoteUri</dt>
<dd>Renote先のUrl（リモートのノートオブジェクトを指定）</dd>
</dl>

### 公開範囲
※specifiedに相当する値はvisibility=specifiedとvisibleAccts/visibleUserIdsで指定する

<dl>
<dt>visibility</dt>
<dd>公開範囲 ['public' | 'home' | 'followers' | 'specified']</dd>
<dt>localOnly</dt>
<dd>0[false] or 1[true]</dd>
<dt>visibleUserIds</dt>
<dd>specified時のダイレクト先のユーザーid カンマ区切りで</dd>
<dt>visibleAccts</dt>
<dd>specified時のダイレクト先のacct（＠?username[＠host]） カンマ区切りで</dd>
</dl>

### ファイル
<dl>
<dt>fileIds</dt>
<dd>添付したいファイルのid（カンマ区切りで）</dd>
</dl>
