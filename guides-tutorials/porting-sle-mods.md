---
title: Porting SLE Mods
description: SLE to SSE porting process for various types of files.
published: true
date: 2023-08-20T09:33:40.929Z
tags: 
editor: markdown
dateCreated: 2023-08-20T09:33:40.929Z
---

# Porting SLE Mods

Not all mods made for Skyrim LE will work out-of-the-box in Skyrim SE. A fair amount of them will need porting.

> A mod being available on the Skyrim SE Nexus does not automatically mean it was ported properly (or at all).
{.is-info}

- **Plugins:** Must always be ported using the [Creation Kit](/tools/ck). Occasionally require manual updates.
- **Archives:** Must always be [unpacked](/guides-tutorials/extracting-bsas) or they will crash the game. Can be repacked afterwards.
- **SKSE Plugins:** Must always be ported for the newest version of SKSE.
- **Meshes:** Should be processed with [Cathedral Assets Optimizer](/tools/cao) (though not always necessary).
- **Textures:** Some older formats must be changed to avoid crashes. Compression recommended.
- **Animations:** Should be processed with [Cathedral Assets Optimizer](/tools/cao).
- **Scripts:** No porting steps required.

## Plugins

Plugins created for Skyrim LE must always be ported. This requires the [Creation Kit](/tools/creation-kit/) and sometimes [SSEEdit](/tools/sseedit) for additional steps.

Check the [Porting SLE Plugins](/skyforge/modding-resources/porting-sle-plugins/) page for instructions.

## Archives

Archives (BSAs) created for Skyrim LE must always be extracted. They will otherwise crash Skyrim SE on launch.

- [Extracting BSAs *How to extract BSAs with Mod Organizer 2, BAE, or CAO.*](/guides-tutorials/extracting-bsas)
{.links-list}

# Assets

Some **textures** and **meshes** as well as all **animations** created for Skyrim LE need to be optimised for Skyrim SE.

> You cannot port [Fore's New Idles in Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/3038) (FNIS) animations this way, only vanilla replacers.
{.is-warning}

## Texture Compression

Textures created for Skyrim LE sometimes need to be compressed or changed to a different format for Skyrim SE.

Since Skyrim SE, the engine supports the **BC7 compression format** which combines the small file size of a compressed texture while retaining nearly the same quality as an uncompressed texture of an older format. Textures for Skyrim LE were sometimes left uncompressed for better visual quality, but should be compressed to BC7 for use in Skyrim SE.

> Only <u>uncompressed</u> textures can be compressed to BC7. If a texture is already formatted as a DXT5/BC3, recompressing it to BC7 will not improve the quality or save any more space.
{.is-warning}