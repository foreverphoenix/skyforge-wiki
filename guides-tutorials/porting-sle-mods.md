---
title: Porting SLE Mods
description: SLE to SSE porting process for various types of files.
published: true
date: 2023-08-21T09:38:31.183Z
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
- **Animations:** Must be processed with [Cathedral Assets Optimizer](/tools/cao).*
- **Scripts:** No porting steps required.

<font size=2>\**You can port vanilla replacers this way, but <u>not</u> [Fore's New Idles in Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/3038) (FNIS) animations.*</font>

## Tutorials

- [Porting Plugins *How to port Skyrim LE plugins to Skyrim SE using the Creation Kit.*](/guides-tutorials/porting-sle-mods/porting-plugins)
- [Optimising Assets *How to port Skyrim LE assets to Skyrim SE using Cathedral Assets Optimizer.*](guides-tutorials/porting-sle-mods/optimising-assets)
{.links-list}

# Texture Compression

Textures created for Skyrim LE sometimes need to be compressed or changed to a different format for Skyrim SE.

Since Skyrim SE, the engine supports the **BC7 compression format** which combines the small file size of a compressed texture while retaining nearly the same quality as an uncompressed texture of an older format. Textures for Skyrim LE were sometimes left uncompressed for better visual quality, but should be compressed to BC7 for use in Skyrim SE.

> Only <u>uncompressed</u> textures can be compressed to BC7. If a texture is already formatted as a DXT5/BC3, recompressing it to BC7 will not improve the quality or save any more space.
{.is-warning}