---
title: Extracting BSAs
description: How to extract BSAs with Mod Organizer 2, BAE, or CAO.
published: true
date: 2023-08-20T09:27:56.875Z
tags: 
editor: markdown
dateCreated: 2023-08-20T09:27:56.875Z
---

> **Prerequisite(s):** [Mod Organizer 2](/mo2) or [Bethesda Archive Extractor](/tools/bae) or [Cathedral Assets Optimizer](/tools/cao)

# Extracting BSAs

You need to extract a BSA if:

1. You want to install a Skyrim LE mod that contains a BSA (it would crash the game).
2. You want assets from the BSA to overwrite loose files.
3. You want to selectively modify or remove assets from the BSA.

(Going through MO2 is easily the most convenient option. Use BAE for selective extraction or for BSAs outside of MO2.)

## Through Mod Organizer 2

If a mod is already installed via Mod Organizer 2, you can extract it through the MO2 interface.

> Please make sure you have [BSA Extractor 2](/mo2/bsa-extractor-2) installed. 
{.is-warning}

- In Mod Organizer 2, switch to the **Archives** tab.

Here, you will find all currently installed archives (BSAs). If they are checked, it means there is a plugin of the same name to load it.

- Right-click the BSA and select **Extract**.
  - *If a mod has multiple BSAs and you want to extract all of them, right-click the **mod name** instead.*
- Navigate to `\Mod Organizer 2\mods\<mod name>\` and confirm.

This will extract the BSA into the mod folder. You can delete the BSA afterwards.

> You can also extract the BSA to a different location or a new mod folder if you only want partial/temporary access.
{.is-info}

![extract-through-mo2.png](/guides-tutorials/extract-through-mo2.png){.align-center}

## Via Bethesda Archive Extractor

[Bethesda Archive Extractor](/tools/bae) is probably the most versatile tool for extracting BSAs. It allows you to unpack one BSA at a time, either in its entirety or in parts. You can also (selectively) extract files and folders via simple drag-and-drop.

The instructions linked above cover how to set BAE as the default app for BSAs. 

- View any BSA by double-clicking it or by going through the MO2 **Filetree**, right-clicking the BSA, and selecting **Open**.
- Click **Extract** to select a target folder to extract all currently checked assets to (all assets are checked by default).

Uncheck the BSA and check files or folders to selectively extract from the archive:

![bae-selective-extraction.png](/guides-tutorials/bae-selective-extraction.png){.align-center}

## Via Cathedral Assets Optimizer

You can create a dedicated profile in Cathedral Assets Optimizer for extracting BSAs:

- [BSA Profile *How to create a CAO profile for creating and unpacking BSAs.*](/tools/cao/bsa-profile)
{.links-list}

Follow these steps to unpack a BSA with CAO:

- Select the **SSE - BSA** profile in CAO.
- Click **Open Directory** and navigate to the location of the BSA.
- Click **Select Folder** and press the **Run** button.

CAO will extract the assets from <u>all BSAs within that folder</u> into the same folder.