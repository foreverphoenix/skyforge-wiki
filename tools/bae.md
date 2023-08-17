---
title: Bethesda Archive Extractor
description: How to set up Bethesda Archive Extractor.
published: true
date: 2023-08-17T11:07:25.087Z
tags: 
editor: markdown
dateCreated: 2023-08-17T11:07:25.087Z
---

> **Prerequisite(s):** [Tools Folder](/tools/tools-folder)

# Bethesda Archive Extractor

**Bethesda Archive Extractor** is a tool for viewing and (selectively) extracting BSAs.

## Installation

- Download [Bethesda Archive Extractor](https://www.nexusmods.com/skyrimspecialedition/mods/974?tab=files) from its Nexus page.
- Create a folder called **Bethesda Archive Extractor** in your **Modding Tools** directory.
- Extract the downloaded archive into the new folder.

## Set as default

Setting BAE as the default app for opening BSAs will allow you to quickly peek inside archives the same way you can inside 7ZIP or RAR files. This can be immensely convenient for asset management.

To set it as the default app, we need a BSA.

- Navigate to your **data folder**.
- Right-click any BSA and select **Open with**.
- Check the **Always use this app to open.bsa files** option.
- Click **More apps**, scroll all the way to the bottom, and click **Look for another app on this PC**.
- Navigate to `\Modding Tools\Bethesda Archive Extractor\` and double-click **BAE.exe**.

This will immediately open whichever BSA you picked in BAE. As you can see, there is a filtering option and you have the ability to browse and unpack files. See [Extracting BSAs](/guides-tutorials/extracting-bsas) for more information.

> **Tip:** Double-clicking a BSA in Mod Organizer 2 will open MO2's own preview window which also has a filtering option and useful information about compression. However, if you right-click the BSA and select **Open**, it will use the default app (BAE) instead.
{.is-info}
