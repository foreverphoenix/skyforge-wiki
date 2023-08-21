---
title: Root Builder Installation
description: How to install the Skyrim Script Extender with Root Builder.
published: true
date: 2023-08-21T08:26:57.851Z
tags: 
editor: markdown
dateCreated: 2023-08-21T08:26:57.851Z
---

> **Prerequisite(s):** [Mod Organizer 2](/mo2)

# Root Builder Installation

This page covers how to cover the [Skyrim Script Extender](/mods/skse) <u>with</u> [Root Builder](/mo2/root-builder).

## Data Folder Files

Install the mod as usual through Mod Organizer 2.

- Expand the **skse64_2_xx_xx** folder.
- *Right-click* the **Data** folder and select **Set as \<data> directory**.
- Click **OK** to install the mod.

![skse-through-mo2.png](/mods/skse-through-mo2.png){.align-center}

## Root Folder Files

Add the EXE and DLL to the mod with the folder structure for Root Builder.

- *Right-click* **Skyrim Script Extender** in your mod order and select **Open in Explorer**.
- Create a new folder called **Root** and open it.
- Open the downloaded archive and extract the following two files* into the **Root** folder:
	- *skse64_1_6_640.dll*
  - *skse64_loader.exe*

<font size=2>\**There used to be a third DLL, skse64_steam_loader.dll, that was part of SKSE. It is no longer required as of SKSE 2.2.3.*</font>
  
![skse-root-builder.png](/mods/skse-root-builder.png){.align-center}

## MO2 Integration

A minor disadvantage of adding SKSE in this fashion is that MO2 will not automatically recognise it. We need to set up the executable manually.

- Open the **Executables** settings by clicking the [gears icon](/basics/mo2-executables-settings.png) in the Toolbar.
- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Mod Organizer 2\mods\Skyrim Script Extender\Root\` and double-click the **skse64_loader.exe**.
- (Optional) Rename the executable in MO2 to **Skyrim Script Extender** and move it to the top of the list.
- Click **OK** to save your changes and close the window.

> The **Redirect** feature in **Root Builder** will automatically move an executable file from a mod folder into the root folder if it is launched through MO2. This is why we can simply point MO2 at the mod folder here.
{.is-info}

![mo2-skse-executable.png](/mods/mo2-skse-executable.png){.align-center}