---
title: Load Order Optimisation Tool
description: How to set up the Load Order Optimisation Tool (LOOT).
published: true
date: 2023-08-18T08:11:43.942Z
tags: 
editor: markdown
dateCreated: 2023-08-18T08:11:09.515Z
---

> **Prerequisite(s):** [Mod Organizer 2](/mo2), [Tools Folder](/tools/tools-folder)

# Load Order Optimisation Tool

The **Load Order Optimisation Tool** (LOOT) is a tool for automatically sorting plugins in the load order. Drawing on a masterlist maintained by the community, LOOT aims to place plugins in a way that minimises unintentional conflicts.

<u>LOOT cannot determine the ideal load order by itself.</u> You **must** use [SSEEdit](/tools/sseedit) and manually adjust.

When LOOT is not used for sorting plugins, it can still be helpful for finding plugins that need "[cleaning](/guides-tutoruals/cleaning-plugins)" as a prerequisite for [generating LODs](/guides-tutorials/generating-lods).

> Do not use the outdated version of LOOT integrated in Mod Organizer 2 by pressing the **Sort** button. There are instructions for removing the button [here](/mo2/remove-sort-button).
{.is-warning}

## LOOT & Wabbajack

If you are building a Wabbajack list and you wish to add optional mods that also have plugins, you may want to use Parapets' [LOOT Config Loader](https://www.nexusmods.com/skyrimspecialedition/mods/60864) plugin ([readme](https://github.com/Exit-9B/LOOTConfigLoader/blob/main/README.md)). It allows you to create a custom masterlist for a portable instance of Mod Organizer 2 so that your users only have to click **Sort** to update the load order.

Note that the LOOT Config Loader tool uses the version of LOOT integrated in Mod Organizer 2 which is somewhat outdated. To use Parapets' plugin with the full version of LOOT, you need to grab [version 0.17.0](https://github.com/loot/loot/releases/tag/0.17.0).

# Installation

LOOT is available on the Nexus.

- Download the installer from the [Nexus page](https://www.nexusmods.com/site/mods/439?tab=files) and run it.
- You can pick your **Tools** folder as the installation directory.
- Keep **Download and install the latest masterlists** checked.
- Uncheck **Launch LOOT** before clicking **Finish**.

## MO2 Integration

LOOT requires access to the data folder and must therefore be launched through Mod Organizer 2.

- Open the [executable settings](/Pictures/skyforge/mo2-executables-settings.png) in Mod Organizer 2.
- Click the small blue plus icon and select **Add from file**.
- Navigate to your **LOOT** folder and double-click **LOOT.exe**.
- Click **OK** to add the executable to Mod Organizer 2.

For improved integration into Mod Organizer 2, I recommend installing the [LOOT Warning Checker](/mo2/loot-warning-checker) plugin.

