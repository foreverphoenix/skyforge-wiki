---
title: Skyrim Script Extender
description: How to install the Skyrim Script Extender and related mods.
published: true
date: 2023-08-21T08:29:03.898Z
tags: 
editor: markdown
dateCreated: 2023-08-21T07:52:49.020Z
---

# Skyrim Script Extender

Of all the mods and tools, the **Skyrim Script Extender** is certainly among the most vital ones: It extends the scripting capabilities of the engine, allowing mod authors to implement features that would not have been possible otherwise.

A popular example of an SKSE-dependent feature is the [Mod Configuration Menu](/knowledge-base/mcm), or **MCM** for short, which is part of the UI overhaul mod [SkyUI](/mods/skyui). There are also a multitude of SKSE-based plugins which, among other things, fix engine-level bugs that could not have been addressed otherwise.

> **SKSE is required by many mods, including most of the essentials.** Modding Skyrim on XBOX or PS5 is not comparable to modding on PC partially because SKSE <u>cannot</u> be installed on consoles. The same is true for the PC Gamepass version of Skyrim.
{.is-warning}

## Skyrim Version

Before you proceed, familiarise yourself with the significance of version dependency and ensure you are using the recommended version of Skyrim SE.

- [Skyrim Versions *Differences between Skyrim ports and updates.*](/knowledge-base/skyrim-versions)
- [Skyrim Version Check *How to check which version of Skyrim is currently installed.*](/guides-tutorials/skyrim-version-check)
{.links-list}

## Downloading SKSE

The Script Extender is available on its [official website](https://skse.silverlock.org/) and on the Nexus. <mark>Read carefully and make sure you are downloading the correct file.</mark>

- Download the **Skyrim Script Extender** for **Steam** or **GOG** from the [Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/30379?tab=files) (**Mod Manager Download**).

The current version of SKSE for AE, build `2.x.x`, should correlate with the current Skyrim SE version, runtime `1.6.xxx`.

## Installing SKSE

SKSE is an unusual mod in that it consists of both **root folder files** and **data folder files**. You can either drop all root folder files into the actual root folder or use the [Root Builder](/mo2/root-builder) plugin in order to manage all parts of the mod in Mod Organizer 2.

- [Regular Installation](/mods/skse/regular)
- [Root Builder Installation](/mods/skse/root-builder)
{.links-list}


