---
title: NifSkope
description: How to set up NifSkope.
published: true
date: 2023-08-18T08:20:43.149Z
tags: 
editor: markdown
dateCreated: 2023-08-18T08:20:43.149Z
---

> **Prerequisite(s):** [Tools Folder](/tools/tools-folder), [Mod Organizer 2](/mo2)

# NifSkope

**NifSkope** is a tool for previewing and modifying [meshes](/knowledge-base/meshes). It covers the vast majority of use cases when building a setup, including changing texture paths and flags. Note that it is not meant for creating *new* meshes.

## Installation

NifSkope is available on Github.

- Download the latest version of [NifSkope](https://github.com/hexabits/nifskope/releases).
- Create a folder called **NifSkope** in your **Tools** folder.
- Extract the downloaded archive into the new folder.

## MO2 Integration

While meshes can be opened separately in NifSkope, you will not be able to preview them with their textures unless NifSkope can find the data folder. Because of this, the programme must be run through Mod Organizer 2.

- Go into the [executable settings](/Pictures/skyforge/mo2-executables-settings.png) in Mod Organizer 2.
- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Tools\NifSkope\` and double-click **NifSkope.exe**.

I recommend adding a shortcut for NifSkope to the MO2 toolbar.

## Default App

By setting .NIF files (meshes) to always open in NifSkope, you can speed up the process of previewing meshes in Mod Organizer 2. Instead of having to launch NifSkope and then dragging and dropping the mesh into the window, you can *right-click* meshes in Mod Organizer 2 and select **Open with VFS**. This will open them in NifSkope while giving access to the VFS, meaning that textures will be loaded correctly.

- *Right-click* any mesh and select **Open with**.
- Make sure **Always use this app to open .nif files** is checked.
- Select **More apps** >> **Look for another app on this PC**.
- Navigate to `\Tools\NifSkope\` and double-click **NifSkope.exe**.
