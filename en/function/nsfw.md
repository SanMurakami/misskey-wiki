---
title: NSFW
description: NSFW flags can be set to files on the drive.
published: true
date: 2020-09-22T12:22:01.345Z
tags: 
editor: markdown
dateCreated: 2020-09-22T12:22:01.345Z
---

<!-- This translation is based on the Japanese version of this article as of Sep 22, 2020. -->

**NSFW (Not Safe For Work)** is a type of flag which can be set to files on the [drive](/function/drive).

It is recommended to mark images or files that seem inappropriate to be seen in public as NSFW so that others are aware of that before they open those files. [Moderators](/function/moderator) of [Misskey](/software/misskey) instances may set NSFW to your files.

A file with NSFW look like the screenshot below, with an overlay with the notice "NSFW":
![2020-09-22_20-53.png](/en_us/function/nsfw/2020-09-22_20-53.png)

It prevents the file from being shown suddenly. Click or tap on it to show the content.

Note that if you (un)mark a file as NSFW, remote instances will not be aware of that.

# How to (un)mark as NSFW

1. Open the drive
2. Right-click/Tap the file to open its menu
3. Push "Mark as NSFW" / "Undo NSFW"

# Comparison with Mastodon

On Misskey you can (un)mark each file as NSFW to make the most of the drive feature. NSFW can be set whenever, not only when you upload it. On the other hand, [Mastodon](/software/mastodon) requires you to mark each toot (is a note in Misskey), not each file, as NSFW and you cannot (un)mark it once the toot is sent.

Therefore, when Misskey instances convey notes to Mastodon ones, all the files attached to them are marked as NSFW if any one of them is marked as NSFW; when Misskey instances communicate one another, such a loss of information does not occur because they understand file-based NSFW flags.
