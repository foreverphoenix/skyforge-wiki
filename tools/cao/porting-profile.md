---
title: Porting Profile
description: How to create a CAO profile for optimising Skyrim LE assets.
published: true
date: 2023-08-20T09:54:58.926Z
tags: 
editor: markdown
dateCreated: 2023-08-20T09:54:58.926Z
---

> **Prerequisite(s):** [Cathedral Assets Optimizer](/tools/cao)

# Porting Profile

**Cathedral Assets Optimizer** can be used to process and optimise Skyrim LE textures, meshes, and animations for use in Skyrim SE. The Porting Profile will also unpack any BSAs as they would crash the game.

- [Porting SLE Mods *SLE to SSE porting process for various types of files.*](/guides-tutorials/porting-sle-mods)
{.links-list}

## New Profile

When creating a new profile, use the pre-made profile for the same game as the base.

- Open **Cathedral Assets Optimizer** and make sure the **SSE** profile is selected at the top.
- Check the option to **Show advanced settings**.
- Click the **New** button to create a new profile and click **OK** to the infobox.

![cao-sse-profile.png](/tools/cao-sse-profile.png){.align-center}

- Enter **SSE - Porting** as the name.
- Confirm to use the **SSE** profile as the basis.

## Configuration

Apply the configuration shown below:

### BSA Tab

![cao-extract-bsa.png](/tools/cao-extract-bsa.png){.align-center}

### Meshes Tab

![cao-optimise-meshes.png](/tools/cao-optimise-meshes.png){.align-center}

### Textures Tab

![cao-optimise-textures.png](/tools/cao-optimise-textures.png){.align-center}

### Animations Tab

![cao-optimise-animations.png](/tools/cao-optimise-animations.png){.align-center}