---
title: Utilities
description: A list of recommended utility mods.
published: true
date: 2023-08-23T07:52:12.422Z
tags: 
editor: markdown
dateCreated: 2023-08-23T07:46:52.706Z
---

# Crash Logger

Crash Logger is absolutely essential for troubleshooting. While the logs can be hard to read, they are crucial for tracking down issues. The linked version is up-to-date for SSE, AE, and VR, and will write to `\Documents\My Games\Skyrim Special Edition\SKSE\`.

I recommend pairing the plugin with [Crash Log Tools](/mo2/crash-log-tools).

- Download and install [Crash Logger](https://www.nexusmods.com/skyrimspecialedition/mods/59818).

**Requirements:** Skyrim Script Extender, Address Library for SKSE

# QUI

QUI combines an ingame plugin explorer (extremely useful for testing) with some vanilla interface tweaks, all of it being optional.

- Download and install [QUI](https://www.nexusmods.com/skyrimspecialedition/mods/65343).

**Requirements:** Skyrim Script Extender, SkyUI

## Settings File

QUI can be configured via its **QUI.toml** which can be overwritten with a custom file. This is usually preferable as changes will not be lost when updating the main mod.

- [Create a new empty mod](/basics/create-empty-mod.png) in Mod Organizer 2 and name it **QUI - Settings**.
- Right-click the new mod and select **Open in Explorer**.
- Create the following folder structure: `\Mod Organzier 2\mods\QUI - Settings\SKSE\Plugins\`.
- Inside the **Plugins** folder, right-click, and select **New** >> **Text Document**.
- Name the file **QUI_Custom.toml**. <u>Remember to change the file extension.</u>

Back in Mod Organizer 2, press F5 to refresh the UI. Place the new mod below **QUI** and activate it.

You can now copy any settings from the default **QUI.toml** into the **QUI_Custom.toml** and customise them there.

## Controller Tweak

QUI contains the [Stay At The System Page](https://www.nexusmods.com/skyrimspecialedition/mods/18397) that is otherwise no longer available for the current version of Skyrim SE. This tweak restores behaviour from the PC version of Skyrim LE where pressing ESCAPE would open the system menu as opposed to the journal. Since controllers have fewer buttons, the system button would open the journal instead in console versions of the game. This behaviour was added to the PC version of Skyrim SE.

If you play on m+kb, I recommend leaving the tweak enabled. ESCAPE will open the System Menu while J opens the Journal.

If you play on controller and prefer quick access to the Journal over quick access to the System Menu, you can set the default option for the system button back to the Journal in the **QUI_Custom.toml**:

```
[JournalMenu]
DefaultPage = 0
```

<u>Remember to save your changes before closing the window.</u>

## Plugin Explorer

<mark>These are personal recommendations from Phoenix.</mark>

I like to pause the game while browsing through the plugin explorer. I also change the hotkey from F11 to F8 because it works better with my usual hotkey choices.

This is my **QUI_Custom.toml**:

```
[PluginExplorer]
Pause = true

[PluginExplorer.Key]
KeyboardToggle = 66
```