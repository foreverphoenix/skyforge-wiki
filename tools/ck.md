---
title: Creation Kit
description: How to set up the Creation Kit for Skyrim SE.
published: true
date: 2023-08-18T06:48:24.665Z
tags: 
editor: markdown
dateCreated: 2023-08-17T12:10:07.687Z
---

> **Prerequisite(s):** [Clean Install](/initial-setup/steam) (FIX LINK)

# Creation Kit

The **Creation Kit** is Bethesda's official modding tool which used to be available only from their proprietary launcher, but has since returned to Steam.

## Installation

- Search for the **Creation Kit** in the Steam store.
- Make sure to select the **Skyrim Special Edition: Creation Kit** and install it.

As the location, choose the same **Steam Library** as for the game itself. The Creation Kit will be installed into the **root folder**.

## Downgrading

Using the Creation Kit is a much better experience with [SSE CreationKit Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/20061). Unfortunately, the original mod is not updated for the newest version of the Creation Kit (the same issues of version dependency affect it that also affect the base game and SKSE). An unofficial [update](https://www.nexusmods.com/skyrimspecialedition/mods/71371) to the mod seems to have a few issues currently.*

<font size=2>\**I was warned about this by friends who use the Creation Kit far more than I ever have and I am deferring to their expertise on the matter.*</font>

To be on the safe side, I recommend rolling back to a previous version of the CK which is compatible with the original CK Fixes.

- Download halgari's [Creation Kit Downgrade Patcher](https://www.nexusmods.com/skyrimspecialedition/mods/67096?tab=files).
- Save the executable into your **root folder** and run it.
- Click **Start Patching**.

The process should only take a second. Close the window when it is done and delete the patcher.

![downgrade-ck.png](/tools/downgrade-ck.png)

# MO2 Integration

## Steam AppID

Close and re-open **Mod Organizer 2**. It should automatically recognise the presence of the Creation Kit which should appear in the executables drop-down.

Before you can run the Creation Kit through MO2, you need to manually add its Steam AppID `1946180` in the [executable settings](/basics/mo2-executables-settings.png):

![ck-steam-appid.png](/tools/ck-steam-appid.png){.align-center}

## MO2 Shortcut

I recommend selecting the Creation Kit from the drop-down and adding a shortcut to the **Toolbar** for quick access.

![ck-mo2-shortcut.png](/tools/ck-mo2-shortcut.png){.align-center}

## Root Builder

> Skip this step if you are not using [Root Builder](/mo2/root-builder).
{.is-warning}

Currently, Root Builder's cache does not include the CK files which means it will remove them from the root folder when an application is run through Mod Organizer 2. We need to rebuild the cache to solve this.

The **CreationKitPrefs.ini** will be generated upon launching the Creation Kit and it may change if you change settings in the CK. To prevent Root Builder from tripping up over those changes, I recommend adding the INI file to the list of excluded files.

![root-builder-clear-cache.png](/tools/root-builder-clear-cache.png){.align-center}

# CK Source Files

Upon launching the CK for the first time, you will get a prompt to unpack the **Scripts.zip** in the data folder installed alongside the CK. The archive contains the source files (.psc) for all vanilla scripts (.pex) which are necessary for modifying and recompiling scripts. These source files can be managed through Mod Organizer 2.

In the process of moving the source files into a mod folder, we will also adjust the folder structure. As it happens, the folder structure for scripts and source files changed for some unfathomable reason: In **SLE**, the file path was `\Data\Scripts\Source\` whereas in **SSE** it became `\Data\Source\Scripts\`. Not only does the SLE file path make more sense (all vanilla and mod-added scripts are located under `\Data\Scripts\`), but most source files packaged with mods also still use the old file path.

The **Tweaked Creation Kit INI** that we are going to install soon will revert the file path for source files back to the SLE one. All that remains is manually fixing the folder structure for the source files.

## Import Source Files

First, we need to set up a new mod folder with the correct file path:

- Create a new empty mod in MO2 and name it **Creation Kit - Source**.
- Right-click the new mod and select **Open in Explorer**.
- Create a new folder called **Scripts** and open it.
- Create a new folder called **Source** and open it.

Next, we need to extract the source files:

- Navigate to `\Steam\steamapps\common\Skyrim Special Edition\Data\`.
- Open the **Scripts.zip** in the data folder.
- Navigate to `\Source\Scripts\` within the archive.
- Select all **.psc** files (CTRL + A) and extract them into the new folder structure:
  - `\Mod Organizer 2\mods\Creation Kit - Source\Scripts\Source\`
- In Mod Organizer 2, press F5 to refresh.

## Import DialogueViews

For the **DialogueViews** folder, we can take an easier route.

- Create a new empty mod in MO2 and name it **Creation Kit - DialogueViews**.
- Right-click the new mod and select **Open in Explorer**.
- Navigate to the top level within the **Scripts.zip** archive.
- Extract the **DialogueViews** folder into the new mod folder.
- Back in Mod Organizer 2, refresh the interface (F5) and move the new mod below **Creation Kit - Source**.
- Right-click it and select **Ignore missing data** (the XMLs are not recognised as mod files).

Finally, delete the **Scripts.zip** from your data folder.

> You can leave the two new "mods" disabled in MO2 until you specifically need them.
{.is-info}

# Improving the CK

There are some additional improvements we can install for the Creation Kit.

First, create a new **separator** in Mod Organizer 2 called **Creation Kit**. I recommend placing it between the base game files (official master files and creations) and your other mods. You can move the new **Creation Kit - Source** and **Creation Kit - DialogueViews** "mods" below this new separator as well.

Install both mods listed below:

- [Tweaked Creation Kit Custom INI *A pre-configured Custom INI file with some necessary adjustments.*](/tools/ck/tweaked-ini)
- [SSE Creation Kit Fixes *A comprehensive collection of tweaks & fixes for the CK.*](/tools/ck/ck-fixes)
{.links-list}

# Separate CK EXE

> This step is optional. It is intended for Wabbajack curators of lists that include the Creation Kit and requires [Root Builder](/mo2/root-builder).
{.is-warning}

Having a downgraded version of the Creation Kit executable in your root folder should not be an issue for 99% of users. It is, however, an issue for curators of Wabbajack lists who cannot have modified files in their root folder because users would need to make the same modifications.

To work around this, move the downgraded executable into Mod Organizer 2 and verify files to restore the current version in the root folder.

![separate-ck-exe.png](/tools/separate-ck-exe.png){.align-center}

# Test Run

With everything installed, give the **Creation Kit** a test run. Launch it through Mod Organizer 2.

Thanks to CK Fixes, starting up the CK should only take a few seconds. If it loads up the main window and if the ***Overwrite*** is empty after quitting again, everything was set up correctly.