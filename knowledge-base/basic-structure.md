---
title: Basic Structure
description: Summary of basic files and folders for vanilla and mods.
published: true
date: 2023-08-18T09:33:42.251Z
tags: 
editor: markdown
dateCreated: 2023-08-18T09:33:00.729Z
---

# Basic Structure

The base game ("vanilla Skyrim") consists of two directories:

1. The **root folder** which contains the executables and the **data folder**.
2. The **Documents folder** which contains the INI files and save files.

## Root Folder

The **root folder** is the default game installation folder.

![skyrim-root-folder.png](/knowledge-base/skyrim-root-folder.png){.align-center}

## Data Folder

The **data folder** is located within the root folder and contains all game **assets**.

![skyrim-data-folder.png](/knowledge-base/skyrim-data-folder.png){.align-center}

## Documents Folder

The **Documents folder** is located under `C:\Users\<Your User Name>\Documents\My Games\Skyrim Special Edition\`.

![skyrim-documents-folder.png](/knowledge-base/skyrim-documents-folder.png){.align-center}

# Game Files

The game consists of two types of files which are located inside the **data folder**:

1. Plugins contain game data. They are specific to the Creation Engine.
2. Assets include textures, sounds, and more. They are either loose or BSA-packed.

Nearly all mods consist of plugins and/or assets and belong into the **data folder**. They can be managed with [Mod Organizer 2](/mo2).

## Root Folder Files

In rare cases, a mod contains executables or .DLL plugins instead of plugins or assets. These mods hook into the engine at launch and must be located in the **root folder**.

Examples include:

- [Skyrim Script Extender](/mod-recommendations/skse)
- [SKSE Preloader](/mod-recommendations/skse)
- [ENBSeries](/mod-recommendations/enbseries)
- [ReShade](/mod-recommendations/reshade)

Mods containing **root folder files** can only be managed with [Mod Organizer 2](/mo2) if the [Root Builder](/mo2/root-builder) plugin is installed.

# Further Reading

- [INI Files *Default (vanilla) INI files, content and differences.*](/knowledge-base/ini-files)
- [Plugins *Plugin basics: Records, FormIDs, Load Order, Formats.*](/knowledge-base/plugins)
- [Assets *Asset basics: Types, Loose vs Packed, Mod Order.*](/knowledge-base/ini-files)
{.links-list}


