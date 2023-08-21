---
title: Update Proofing
description: How to prevent the Steam version of Skyrim SE from updating automatically.
published: true
date: 2023-08-21T07:35:50.149Z
tags: 
editor: markdown
dateCreated: 2023-08-21T07:35:00.149Z
---

> **Prerequisite(s):** [Clean Install](/guides-tutorials/clean-install) (Steam)

# Update Proofing

- [Skyrim Versions *Differences between Skyrim ports and updates.*](/knowledge-base/skyrim-versions)
{.links-list}

<mark>This only affects the **Steam** version of Skyrim SE.</mark>

The version-specific nature of the [Skyrim Script Extender](/mods/skse) and related mods makes forced updates of the base game quite disruptive. They can completely break a modded setup, potentially rendering you unable to play until the modding scene has caught up.

Fortunately, update-proofing Skyrim is simple:

- In your games library in Steam, right-click **The Elder Scrolls V: Skyrim Special Edition**.
- Select **Properties** and switch to the **Updates** tab.
- Make sure **Automatic updates** are set to **Only update this game when I launch it**.

> This would still force you to update whenever you attempt to launch the game through its default executables. However, SKSE comes with its own launcher which you must always use to launch the game for it to work properly. Launching the game through SKSE will <u>not</u> prompt Steam to update, meaning you can stay on an older version of the game indefinitely.
{.is-info}

![update-proofing.png](/knowledge-base/update-proofing.png){.align-center}