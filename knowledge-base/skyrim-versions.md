---
title: Skyrim Versions
description: Differences between Skyrim ports and updates.
published: true
date: 2023-08-21T07:15:02.985Z
tags: 
editor: markdown
dateCreated: 2023-08-21T07:15:02.985Z
---

# Skyrim Versions

Many versions and ports of Skyrim SE exist and not all are usable for modding. This wiki is written specifically for the *Steam* or *GOG* version of **Skyrim Special Edition** (Skyrim SE).

> For the vast majority, the ideal version for modding is currently Skyrim SE 1.6.640 (Steam) or 1.6.659 (GOG).
{.is-success}

- **Skyrim Legendary Edition** (SLE) has been superseded by Skyrim SE.
- The **PC Gamepass** and **Console** versions of Skyrim SE are too limited for modding.
- The **VR** port of Skyrim is similar to but not the same as Skyrim SE.

The **Skyrim Anniversary Edition** (AE) is a DLC for Skyrim SE containing all Creations and has no immediate impact on modding. Whether you own it is irrelevant.

## SKSE and Skyrim Updates

All updates to **Skyrim SE** change the main executable, **SkyrimSE.exe**, which requires the [Skyrim Script Extender](/mods/skse/) to be updated in turn because it is <u>version-dependent</u> and will only work with the specific version of Skyrim SE it was compiled for. For example, SKSE SE version **2.0.20** functions only with the last pre-Anniversary Edition version of Skyrim SE, **1.5.97**. The new SKSE AE was made for the post-AE versions of Skyrim SE.

Whenever Skyrim updates, the modding community tends to catch up within a few weeks to months. Staying indefinitely on an older version will eventually mean that you cannot use newer mods or update existing mods. Therefore it makes sense to move on to the current version once all (or at least most) of the mods in your setup have been updated.

- **Skyrim SE 1.5.97:** Last pre-AE version of Skyrim SE (requires SKSE 2.0.20)
- **Skyrim SE 1.6.317:** Skyrim SE patch that accompanied the AE release (requires SKSE 2.1.0)
- **Skyrim SE 1.6.353:** Post-AE version of Skyrim SE with most mods ported (requires SKSE 2.1.5)
- <mark>**Skyrim SE 1.6.640:** Current version of Skyrim SE (requires SKSE 2.2.3)</mark> << **recommended**

([Full Skyrim SE version history with changelogs](https://en.uesp.net/wiki/Skyrim:Special_Edition_Patch).)

The issue of version dependency not only affects SKSE and the base game, but also SKSE and SKSE plugins. While some SKSE-dependent mods only use functions added by SKSE in their scripts and do not require a specific version of SKSE to actually work, there are also the so-called **SKSE plugins**\*. These files with the **.DLL** extension are dependent on a specific SKSE version the same way SKSE is dependent on a specific Skyrim SE version.

<font size=2>\**SKSE plugins (DLLs) are not to be confused with Skyrim plugins (ESMs, ESPs, ESLs). The former are written in C or C++ and specific to the Script Extender. The latter are created in the Creation Kit or community-made tools, and specific to Creation Engine games.*</font>
