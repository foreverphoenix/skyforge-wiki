---
title: Cleaning Plugins
description: When and how to clean plugins with SSEEdit.
published: true
date: 2023-08-18T11:16:24.430Z
tags: 
editor: markdown
dateCreated: 2023-08-18T10:58:18.497Z
---

> **Prerequisite(s):** [Mod Organizer 2](/mo2), [SSEEdit](/tools/sseedit) (including Quick Auto Clean), [LOOT](/tools/loot) (optional), [LOOT Warning Checker](/mo2/loot-warning-checker) (optional)

# Cleaning Plugins

- [Should I clean plugins? *Read this article on when to "clean" plugins first.*](/guides-tutorials/cleaning-plugins/should-i-clean-plugins)
{.links-list}

## Quick Auto Clean

Plugin "cleaning" used to be a semi-involved process with multiple steps but has since been simplified. It is done with [SSEEdit](/tools/sseedit) in the **Quick Auto Clean** mode. SSEEdit comes with a preconfigured executable for it.

You can clean plugins either by manually running SSEEdit in `-QAC` mode or by using [LOOT Warning Checker](/mo2/loot-warning-checker). The latter option is slightly faster, but only works for plugins that are flagged as needing to be cleaned in the LOOT masterlist.

In the following, both methods will be demonstrated using the official master files as an example.

> When cleaning plugins is needed, you can use [LOOT](/tools/loot) to find plugins that are "unclean". However, keep in mind that LOOT's masterlist is limited and may be outdated or incomplete. If you missed any plugins, DynDOLOD NG should warn you about them.
{.is-info}

## Backups

When modifying offical files (the official master files or creations), it is safer to create *copies* rather than modifying the files in the default installation folder. This has the advantage that you can move or verify the game folder without having to repeat the process.

> In the case of an actual update to the game, (some of) the official files are usually modified in which case you do need to repeat the process with the new version(s).
{.is-info}

- Create a new mod in MO2 and name it **Official Master Files - Cleaned**.
- Copy the following ESMs from your installation folder into the new mod folder:
  - *Update.esm*
  - *Dawnguard.esm*
  - *Hearthfires.esm*
  - *Dragonborn.esm*
- Place the new "mod" below the originals in Mod Organizer 2.

> **Skyrim.esm** <u>cannot</u> be cleaned. It consists exclusively of new records and has no masters.
{.is-danger}

![overwrite-omf.png](/guides-tutorials/overwrite-omf.png){.align-center}

For creations I tend to copy all plugins that need cleaning into a similar **Creation Club - Cleaned** mod before processing them. LOOT will tell you which creations have ITMs and/or deleted references.

For plugins from mods you do not need to create separate copies. However, adding a reminder in the **Notes** tab in Mod Organizer 2 that the plugin was modified can be very helpful. This way, you will know that you need to check and possibly re-clean the plugin when the mod is updated.

# Cleaning Methods

## Manual Cleaning

Plugins can be "cleaned" with SSEEdit Quick Auto Clean <u>one at a time</u>. When cleaning the official master files, start with Update.esm and proceed according to their load order (Dawnguard > HearthFires > Dragonborn).

When cleaning plugins from mods, clean masters before dependencies.

- Run **SSEEdit QAC** through Mod Organizer 2.
- Check the plugin you wish to clean and click **OK**.

![cleaning-1.png](/guides-tutorials/cleaning-1.png){.align-center}

The remainder of the process is fully automated and will take a few minutes. Simply wait for SSEEdit to return `Quick Clean mode finished` at which point you can close the tool.

## LOOT Warning Checker

The [LOOT Warning Checker](/mo2/loot-warning-checker) plugin will list all plugins that the LOOT Masterlist considers in need of cleaning. Its handy **Fix** button that will automatically run SSEEdit QAC. For plugins that are in the masterlist, this is slightly faster than launching QAC manually.

![fix-to-clean.png](/guides-tutorials/fix-to-clean.png){.align-center}