---
title: Assets
description: Asset basics: Types, loose vs packed, BSAs, mod order.
published: true
date: 2023-08-18T10:33:21.213Z
tags: 
editor: markdown
dateCreated: 2023-08-18T10:33:21.213Z
---

# Assets

Mods (and the game data of the vanilla game) consists of two basic file types: [Plugins](/knowledge-base/plugins) and **assets**.

## Asset Types

All asset types must be located in the **data folder** in a top-level folder of the same name, i.e., `\Skyrim Special Edition\Data\Textures\`.

The following file types are recognised by the game:

- **Textures** (.DDS)
- **Meshes** (.NIF)
- **Scripts** (.PEX)
- **Animations** (.HKX)
- **Interface** (.SWF)
- **SKSE\Plugin** (.DLL)
- **Sound\Voice** (.FUZ)
- **Sound\FX** (.WAV)
- **Music** (.XWM)

<font size=2>*The list is not 100% complete, but these are the important ones.*</font>

Different asset types handle very differently from each other (unlike plugins) and more time is required to learn how to substantially modify them. On the other hand, sound design, 3D modelling, etc, are (again, unlike plugins) widely applicable skills and not unique to Bethesda's Creation Engine.

> Generally speaking, you do not need to become as adept at modifying different types of assets as you should at modifying plugins in order to build a solid setup.
{.is-success}

# Bethesda Softworks Archives

Assets can be present in two forms: as **loose files** or **BSA-packed**. <mark>Loose files <u>always</u> overwrite packed assets.<mark>

**Bethesda Softworks Archives** (BSA) are essentially 7ZIP or WinRAR archives for Creation Engine assets. All vanilla assets are packed into the 17 BSAs in the data folder which are compressed to save space. Many mods are also published with their assets packed into a BSA.
  
> In Skyrim SE, BSAs have a size limit of **2GB**.
{.is-warning}

## BSA Types

There are two types of BSAs:

- Example.bsa
- Example - Textures.bsa

The latter type is intended specifically for textures. Use the regular type for all other kinds of assets.

BSAs can be **compressed** or **uncompressed**. Looking at the vanilla BSAs, you will notice that archives containing textures and meshes are *compressed* while all others are *uncompressed*. This logic should be mirrored when creating new BSAs.

> There are also some additional flags uncovered by fireundubh [as documented here](https://wiki.fireundubh.com/skyrim/bsa-flags).
{.is-info}

## Loading BSAs

**A BSA always requires a plugin with the same name to be loaded.**

*Example.esp* (or ESL/ESM) can load *Example.bsa* and *Example - Textures.bsa*. If the name does not match exactly the BSA will not be loaded. The plugin does not need to have any content, it can be an empty 'dummy' (in which case it should ideally be an ESP-FE).

> The vanilla BSAs are actually loaded via the **Skyrim.ini** file. It should  *technically* be possible to load additional BSAs by adding them to the INI; however, this is not particularly convenient and so it is not done.
{.is-info}

## Manipulating BSAs

You can preview and extract BSAs with [Mod Organizer 2](/mo2), [Bethesda Archive Extractor](/tools/bae), or [Cathedral Assets Optimizer](/tools/cao).

Unlike Fallout 4, there is no need to worry about massive performance drops with loose files over archived ones. Unpacking BSAs definitely helps with asset management with the increased space requirement being the only downside.
  
The only files you should <u>never</u> unpack are `\lodsettings\example.lod` files because the game only recognises them when they are in a BSA.

# Mod Order

Similar to how [plugins](/knowledge-base/plugins) overwrite each other according to their placement in the **load order**, so do assets overwrite each other according to their placement in the **mod order**.

The mod order is a concept created by [Mod Organizer 2](/mo2) and its *virtual data folder* which prevents assets from irrevocably overwriting and replacing each other by placing them in separate folders.

> **The mod order is functionally identical to the load order:** If multiple mods [plugins] contain different versions of the same asset [record], the mod [plugin] that is placed lowest will win the conflict and overwrite.
{.is-success}

## BSAs & Load Order

As a consequence of being attached to plugins, **BSAs adhere to load order** rather than mod order. This means that <u>assets packed into BSAs overwrite each other in the order of their plugins</u>.

It makes sense to BSA-pack assets from mods that serve as a baseline intended to be overwritten. On the flipside, assets from mods that should generally overwrite are best kept as loose files.

You may also want to extract an archive in order to be able to compare its assets to other assets in your mod order. [NifSkope](/tools/nifskope), for example, can only load loose textures and meshes, not BSA-packed ones.

# Further Reading
    
- [Extracting BSAs *How to extract BSAs with BAE, CAO, or MO2.*](/guides-tutorials/extracting-bsas)
{.links-list}