---
title: Importing Creations
description: How to import creations into MO2 as mods with Curation Club.
published: true
date: 2023-08-17T07:17:33.918Z
tags: 
editor: markdown
dateCreated: 2023-08-17T07:17:33.917Z
---

> **Prerequisite(s):** [Mod Organizer 2](/initial-setup/mod-organizer-2), [Curation Club](/tools/curation-club)

# Importing Creations

Although the [creations](/knowledge-base/creation-club) are official content, they are functionally mods. Most are rather small and consist of one or several archives (BSAs) and a [plugin](/knowledge-base/plugins) (ESL, rarely ESM). Their load order is determined by the **Skyrim.ccc** file in the root folder.

When the *creations* are kept in the **data folder**, Mod Organizer 2 will treat them as official content: They will always be enabled, their load order cannot be changed, and you are unable to view/manipulate files like you can for other mods.

To simplify the management of creations with Mod Organizer 2 I recommend importing them by placing them in regular mod folders. This can be automated with the [Curation Club](/tools/curation-club/) plugin.

> Because **Curation Club** moves the creations out of the data folder rather than creating copies, you may want to create a backup first. Just copy all files starting with cc from `\Steam\steamapps\common\Skyrim Special Edition\Data\` to a convenient location.
{.is-warning}

## Curation Club

Running **Curation Club** through Mod Organizer 2 will import all creations present in your **data folder** into Mod Organizer 2 where you can manage them like any other mod.

- Run **Curation Club** (see below).
- Click **OK** to import your creations.

> If you are using the [Root Builder](/tools/root-builder) plugin, check the box for **Root Builder Support**.
{.is-warning}

![run-curation-club.png](/getting-started/initial-setup/run-curation-club.png){.align-center}