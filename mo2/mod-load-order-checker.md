---
title: Mod Load Order Checker
description: How to install the Mod Load Order Checker plugin for MO2.
published: true
date: 2023-08-26T18:11:59.581Z
tags: 
editor: markdown
dateCreated: 2023-08-16T09:49:18.791Z
---

> **Prerequisite(s):** [Mod Organizer 2](/getting-started/initial-setup/mod-organizer-2)

# Load Order Checker

**Load Order Checker** is a plugin for Mod Organizer 2 which adds a warning when *plugins* are being loaded out of order, i.e., a patch is placed before its master. Out-of-order plugins can be difficult to track, especially in a large load order, and they create broken dependencies which can prevent the game from launching properly and cause other issues.

## Installation

Load Order Checker is available on the Nexus.

- Download the latest version of [Load Order Checker](https://www.nexusmods.com/site/mods/608?tab=files).
- Extract the downloaded archive into the **plugins** folder.
- Restart Mod Organizer 2.

## Example

Without the plugin, there will be no visible error anywhere in Mod Organizer 2 when a plugin is loaded before its master. In SSEEdit, the load order will be fixed automatically, so you will see no errors, but the same does not happen ingame where you *will* have issues.

With the plugin, a warning will show up:

![out-of-order.png](/tools/out-of-order.png){.align-center}

![mo2-warning.png](/tools/mo2-warning.png){.align-center}