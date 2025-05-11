---
title: FAQ
description: Frequently Asked Questions
published: true
date: 2025-05-11T03:59:24.794Z
tags: 
editor: markdown
dateCreated: 2021-10-14T17:45:35.073Z
---

# Home, Local, Social, Global: What's the difference?

Each timeline has a different set of users which it displays notes of.

|Timeline|You will see notes of ...|
|---|---|
|Home|users you follow|
|Local|everybody in your server|
|Social|users you follow + everybody in your server|
|Global|everybody in all servers your server is connected|

You can restrict who will be able to see your note (see [Timeline](/en/tl)).

# Misskey is too slow

Misskey Web makes use of a lot of animations. It is a known issue that it freezes or does not work flawlessly on low-spec environments. Turn on "Reduce UI Animation" in Settings to reduce such animations.

# Is Misskey an Mastodon server?

No. It is not Mastodon with new appearances, either. Misskey does not have to do anything with Mastodon except that these servers can be connected over ActivityPub.

# Can Misskey cooperate with Mastodon?

servers of Mastodon and Misskey can communicate each other to follow users in each other and reply to them as if they were on the same services. Misskey, however, does not implement anything special to make that happen. 

Misskey implements ActivityPub protocol, so Mastodon does. They will no longer be able to communicate each other if either stopped to support ActivityPub.

Misskey users can follow Mastodon users and vice versa. The same applies to reaction/renotes (or boosts in Mastodon terms).

# Notifications look irrelevant to me 

Automatic note watching may be turned on. Navigate to "Account Settings" and turn off "[Watch note automatically](/en/watch)" to disable it.

# How can I format/animate my notes?

Use [Misskey Flavored Markdown (MFM)](/en/mfm).

# Some users have "nekomimi (cat ears)" on their icons. What is "Cat"?

"Cat" is one of Misskey's mysterious features. "Cat" users have cat ears on their icons, and 「な」(na) in notes are replaced with 「にゃ」(nya).

You can enable "Cat" in Settings. Remote users will see you as a "Cat" too. 

# It looks like searching is disabled
<!-- Original title: 「検索機能はインスタンスの設定で無効になっています。」-->

Administrators of your server have to introduce ElasticSearch and configure Misskey to use searching.

# I found a bug in Misskey / I have an idea to improve Misskey

<!-- removed @aqz-san as the account was not found on misskey.io -->
Contact [@syuilo@misskey.io](https://misskey.io/@syuilo).

Have a GitHub account? Then file an [issue](https://github.com/syuilo/misskey/issues/new/choose) after you take a look at [existing issues](https://github.com/syuilo/misskey/issues) instead. PRs are also welcome!

# How can I donate to Misskey?

Links to Amazon Wishlists and Patreon pages are available at the bottom of [Misskey Hub](https://misskey-hub.net/ja/docs/donate/).

# I forgot my password, what should I do?

Contact administrators of your server via email or a new account. They will tell you a new password once they confirm you own that account and reset its password. It is recommended to change it afterwards.

# Cannot log out of my account

Try deleting cookie of your browser.