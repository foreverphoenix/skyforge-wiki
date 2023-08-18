---
title: Asset Management
description: How Mod Organizer 2 can be used to manage assets.
published: true
date: 2023-08-18T10:49:34.584Z
tags: 
editor: markdown
dateCreated: 2023-08-18T10:49:34.584Z
---

# Asset Management

- [Assets *Asset basics: Types, loose vs packed, BSAs, mod order.*](/knowledge-base/assets)
{.links-list}

Organising assets from mods (comparing, selecting, modifying) is a major step in building a mod setup. [Mod Organizer 2](/mo2) is a brilliant tool for managing assets, mostly because of its *virtual data folder* and **mod order**. You can control assets on a per-file basis, comparing and selectively removing them when necessary.

# Asset Conflicts
  
The *left pane* of Mod Organizer 2, the **mod order**, visualises mod interaction via icons in the **Conflicts** column. Below, you can see all possible conflicts and the icons symbolising them.

> Conflicts involving BSAs will only be shown if [archive parsing](/knowledge-base/asset-management/#archive-parsing) is enabled.
{.is-info}

![mo2-conflicts-all.png](/knowledge-base/mo2-conflicts-all.png){.align-center}

## Resolving Conflicts

You can resolve asset conflicts in three ways:

1. By packing assets that are meant to be overwritten by other loose files in a BSA.
2. By changing the mod order so another mod overwrites.
3. By (selectively) hiding or removing assets.

## Viewing Conflicts

Each mod's asset conflicts can be viewed in detail in the **Conflicts** tab when you double-click the mod in the mod order. The **Advanced** tab is generally more useful.

You will see overwriting and overwritten assets, plus all mods that are overwriting and overwritten.

> Files in *italics* are from BSAs.
{.is-info}

![mo2-conflicts-tab.png](/knowledge-base/mo2-conflicts-tab.png){.align-center}

## Removing Assets

You can remove any assets by simply deleting them in the File Explorer or through the **Filetree** tab in Mod Organizer 2. Assets <u>cannot</u> be removed in the **Conflicts** tab; however, they can be *hidden*.

*Hiding* assets through Mod Organizer 2 renames their file extension to **.mohidden** which means the game will no longer recognise them. Unlike deleting the file, this can be undone at any time.

![mo2-hide-asset.png](/knowledge-base/mo2-hide-asset.png){.align-center}

Hiding files instead of outright deleting them can be very helpful in the early stages of building a setup where you may not be entirely sure which assets you want to use in the end. It can be annoying the dig through mod archives searching for that one texture that has been fully deleted. It is much easier to restore hidden files.

# File Preview

Textures and, with an additional plugin, meshes can be directly previewed and compared in Mod Organizer 2. Scripts can only be previewed if the source (.psc) files are present which can be opened in any text editor.

BSAs can also be previewed.

## Viewing Textures

Mod Organizer 2 includes a plugin for easy texture comparison. You can double-click textures in the **Filetree** and in the **Conflicts** view as well as in the **Data** tab in the right pane to open a small preview.

If you open the preview through the **Conflicts** or **Data** tab, you will be able to cycle through all <u>loose</u> copies of the same file to compare them.

Files packed in BSAs <u>cannot</u> be previewed this way. This is one reason for why loose files are easier to work with.

![texture-preview.png](/knowledge-base/texture-preview.png){.align-center}

## Viewing Meshes

Viewing the flat texture does not give a good idea of what it will look like ingame. This is easier when you can see it properly applied to its mesh. Thankfully, Parapets created the [NIF Preview](/tools/nif-preview) plugin which is functionally identically to the DDS preview, but used for meshes.

With NIF Preview installed, you can preview meshes in the same way as textures (if they are loose files). It will draw on your *loose* textures as well as the vanilla BSAs.

NIF Preview is still currently in beta so it has the occasional issue. When it does not properly show a mesh or when you want to see more detail, you can *right-click* a mesh and select **Open with VFS** to view it in [NifSkope](/tools/nifskope) (this requires having set up NifSkope as the default app for viewing NIFs).
 
# BSAs in MO2

All BSAs from currently active mods are displayed in the **Archives** tab in the right pane. They are greyed out because they cannot be enabled or disabled here, but you can tell from whether or not they are checked if they have a matching plugin to load them. If they are <u>unchecked</u> they are not currently being loaded into the game.

![mo2-archives-tab.png](/knowledge-base/mo2-archives-tab.png){.align-center}

## BSA Preview

You can preview BSAs by *double-clicking* them in the **Filetree** or **Data** tabs. If you *right-click* and select **Open**, the BSA will be opened in the default app instead which is [Bethesda Archive Extractor](/tools/bae) if you installed that.

Both views allow you to filter by file name. The MO2 preview also allows you to see the compression level and archive types while BAE is more convenient for (selectively) extracting files (see [Extracting BSAs](/guides-tutorials/extracting-bsas/)).

## Archive Parsing
  
I strongly recommend enabling **archive parsing** in the MO2 [Settings](/basics/mo2-open-settings.png) (**Workarounds** tab).

This setting can be somewhat buggy and it will slow down Mod Organizer 2 (especially in large setups), but it is important for seeing conflicts between archives and loose files in the interface.

![mo2-archive-parsing.png](/knowledge-base/mo2-archive-parsing.png){.align-center}