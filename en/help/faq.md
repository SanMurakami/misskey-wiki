---
title: FAQ
description: Frequently Asked Questions
published: true
date: 2021-08-04T05:22:34.983Z
tags: 
editor: markdown
dateCreated: 2020-09-20T05:04:12.109Z
---

<!-- This translation is based on https://misskey.wiki/faq#%E8%87%AA%E5%88%86%E3%81%AB%E9%96%A2%E4%BF%82%E3%81%AE%E3%81%AA%E3%81%84%E9%80%9A%E7%9F%A5%E3%81%8C%E5%B1%8A%E3%81%8F as of Sep 20, 2020 -->

# Home, Local, Social, Global: What's the difference?

Each timeline has a different set of users which it displays notes of.

|Timeline|You will see notes of ...|
|---|---|
|Home|users you follow|
|Local|everybody in your instance|
|Social|users you follow + everybody in your instance|
|Global|everybody in all instances your instance is connected|

You can restrict who will be able to see your note (see [Timeline](/en/tl)).

# Misskey is too slow

Misskey Web makes use of a lot of animations. It is a known issue that it freezes or does not work flawlessly on low-spec environments. Turn on "Reduce UI Animation" in Settings to reduce such animations.

# Is Misskey an Mastodon instance?

No. It is not Mastodon with new appearances, either. Misskey does not have to do anything with Mastodon except that these instances can be connected over ActivityPub.

# Can Misskey cooperate with Mastodon?

Instances of Mastodon and Misskey can communicate each other to follow users in each other and reply to them as if they were on the same services. Misskey, however, does not implement anything special to make that happen. 

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

Administrators of your instance have to introduce ElasticSearch and configure Misskey to use searching.

# I found a bug in Misskey / I have an idea to improve Misskey

<!-- removed @aqz-san as the account was not found on misskey.io -->
Contact [@syuilo@misskey.io](https://misskey.io/@syuilo).

Have a GitHub account? Then file an issue after you take a look at existing issues instead. PRs are also welcome!

# How can I donate to Misskey?

Links to Amazon Wishlists and Patreon pages are available at the bottom of [joinmisskey](https://join.misskey.page/en/).

# I forgot my password, what should I do?

Contact administrators of your instance via email or a new account. They will tell you a new password once they confirm you own that account and reset its password. It is recommended to change it afterwards.

# Cannot log out of my account

Try deleting cookie of your browser.