---
title: Cathedral Assets Optimizer
description: How to set up Cathedral Assets Optimizer.
published: true
date: 2023-08-17T11:44:45.253Z
tags: 
editor: markdown
dateCreated: 2023-08-17T11:10:01.903Z
---

> **Prerequisite(s):** [Tools Folder](/tools/tools-folder)

# Cathedral Assets Optimizer

**Cathedral Assets Optimizer (CAO)** is an all-in-one asset processing tool for Skyrim (SE/LE) and Fallout (NV/3/4). Among other things, it can create and unpack archives, optimise meshes, and perform some basic texture modifications like changing the resolution, creating mipmaps, or compressing.

## Installation

While CAO is meant to modify mods, it should target separate modding folders as opposed to being run on an entire setup. Do not try to launch it through Mod Organizer 2.

- Download the latest stable version from the [Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/23316?tab=files).
- Create a folder called **Cathedral Assets Optimizer** in your **Tools** folder.
- Extract the downloaded archive into the new folder.

For quick access, I recommend **pinning** the executable to your taskbar.

## Antivirus Exclusions

The author of CAO recommends creating an exclusion in [Windows Defender](https://support.microsoft.com/en-us/windows/add-an-exclusion-to-windows-security-811816c0-4dfd-af4a-47e4-c301afe13b26) to prevent slowdowns (follow link for instructions).

Third-party antivirus software, if you have any installed, may also cause CAO to not work properly (or at all) and you may need to create an exclusion for them as well. You should be able to find instructions by googling for the name of the antivirus and "exclusion".

# Create BSA Profile

Cathedral Assets Optimizer is built for a variety of use cases across multiple different games. Configurations can be saved as **presets** to avoid having to manually apply them when using the tool.

- [BSA Profile *How to create a CAO profile for packing and unpacking BSAs.*](/tools/cao/bsa-profile)
{.links-list}