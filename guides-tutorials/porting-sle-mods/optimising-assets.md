---
title: Optimising Assets
description: How to port Skyrim LE assets to Skyrim SE using Cathedral Assets Optimizer.
published: true
date: 2023-08-20T09:57:24.959Z
tags: 
editor: markdown
dateCreated: 2023-08-20T09:57:24.959Z
---

> **Prerequisite(s):** [Cathedral Assets Optimizer](/tools/cao)

# Optimising Assets

You can process Skyrim LE textures, meshes, and animations with **Cathedral Assets Optimizer**. Create a dedicated profile:

- [Porting Profile *How to create a CAO profile for optimising Skyrim LE assets.*](/tools/cao/porting-profile)
{.links-list}

## Usage

You can run any Skyrim LE mod containing meshes, textures, <u>or</u> animation files through CAO using the **SSE - Porting** profile. It will also unpack BSAs which would crash the game otherwise.

If the assets are still packed in a BSA, they will be extracted and the archive deleted as it would crash Skyrim SE otherwise. You can use the CAO [Create BSA profile](/tools/cao/bsa-profile) to repack the assets after processing if you so wish.

Should a mesh still have issues after processing (causing crashes or visual bugs), try using a higher level of optimisation.

