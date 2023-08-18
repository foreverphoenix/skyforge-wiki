---
title: Distant LODs
description: About object, terrain, and tree LODs.
published: true
date: 2023-08-18T11:56:42.879Z
tags: 
editor: markdown
dateCreated: 2023-08-18T11:56:42.879Z
---

# Distant LODs

> This article draws heavily on and occasionally quotes from resources written by **sheson**, the creator of [DynDOLOD](/tools/dyndolod) and authority on all things related to LODs. Please check the [DynDOLOD documentation](https://dyndolod.info/) for more detailed information.
{.is-info}

In the context of Creation Engine modding, **distant LOD** (level-of-detail) describes far-away objects and landscape. The further the object or terrain is from the player, the lower the quality in which it is rendered. This improves performance.

**LODs should be regenerated in modded setups for better quality and to integrate the installed mods.** If done with conservative settings, the performance impact can be minimised while still achieving very noticeable visual improvements.

## Types of LOD

There are multiple types of LOD:

- [Object LOD](https://dyndolod.info/Help/Object-LOD) consists of "combined meshes and textures for objects that do not change and are not animated, like buildings or landscape features like mountains and rocks."
- [Tree LOD](https://dyndolod.info/Help/Tree-LOD) is a separate LOD system for rendering distant trees as [flat cardboard cutouts](https://dyndolod.info/sites/dyndolod/files/images/tree-lod.webp). With DynDOLOD you can also generate much higher quality 3D or hybrid Object LOD for trees.
- [Terrain LOD](https://dyndolod.info/Help/Terrain-LOD-and-Water-LOD) "is the distant ground and large (cell sized) bodies of water." Regenerating it ensures that your close-up landscape textures match and blend with distant terrain.
  - *The world map uses Terrain LOD meshes and textures (LOD Level 32).*
- [Grass LOD](https://dyndolod.info/Help/Grass-LOD) visually extends grass into the distance without the performance cost of fully rendering it.

**Terrain LOD** is generated with [SSELODGen](/tools/sselodgen).

Dynamic **Object** and **Tree LOD** are generated with [DynDOLOD](/tools/dyndolod).

<font size=2>*SSELODGen can also generate Object and Tree LOD, but not as high quality as DynDOLOD.*</font>

**Grass LOD** is also generated with [DynDOLOD](/skyforge/tool-setup/dyndolod/) but requires some extra steps and tools.

> If you are interested in **Grass LOD**, please consult [Althro's guide](https://github.com/The-Animonculory/Modding-Resources/blob/main/Grass%20Lods.md).
{.is-info}

# LOD Resources

Creating matching LODs for your mods requires additional resources. Some of those are provided on the Nexus while others, namely [billboards](https://dyndolod.info/Help/Tree-Grass-LOD-Billboards), must be generated with TexGen specifically for your setup. Billboards are required for **Tree** and **Grass LOD** and must generated with TexGen before running DynDOLOD.

For **Terrain LOD** generation, LOD resources may be provided by the author for improved blending. If so, overwrite the original mod with the LOD resources while running SSELODGen and *disable them afterwards*.

DynDOLOD resources should be left <u>enabled</u> after LOD generation.

Installation instructions for resources that should be present in any setup are covered in the [SSELODGen](/tools/sselodgen) and [DynDOLOD](/tools/dyndolod) setup instructions.

# When should I generate LODs?

LOD (and Occlusion) generation are the **final steps** in building a setup because all objects and assets must be present to be incorporated. DynDOLOD copies from the final layer of each plugin so all conflict resolution must be completed at this point as well.

That being said, it is helpful to generate *temporary* object, tree, and terrain LOD after completing the visual baseline of a setup. This allows you to approximate the level of graphical quality as well as performance you can expect while giving you a good backdrop for hand-picking assets and testing ENB presets. Only generate for the Tamriel worldspace to speed up the process.

## (Re)generating Terrain LOD

**Terrain LOD** should be (re)generated after changing landscape textures.

It is possible to regenerate Terrain LOD after beginning a playthrough because it is affected by mods (mesh and texture replacers) that can be added or removed at any time. Remove your previous output, then rerun [SSELODGen](/skyforge/tool-setup/sselodgen/).

## (Re)generating Object and Tree LOD

**Object** and **Tree LOD** should be (re)generated when the position of objects changed or new objects were added (for example, a new ruin was added to the Morthal swamp or some trees were resized in the Rift).

Unless the LOD assets changed (i.e., because you changed your tree overhaul), you do <u>not</u> need to regenerate billboards with TexGen.

The **TexGen** and **DynDOLOD** outputs can be regenerated in an ongoing playthrough, but this requires some extra steps:

1. Load your save and make sure you are in an exterior cell.
2. Disable DynDOLOD in the ingame MCM.
3. Go into an interior cell (like a house or a dungeon).
4. Create a manual save and exit the game.
5. Remove your old DynDOLOD output (and TexGen, if necessary).
6. Reload your save and click OK to missing plugins.
7. Create a manual save and exit the game.
8. Update DynDOLOD and regenerate the output(s).
9. Load your save and continue your playthrough.