---
title: SSEEdit
description: How to set up SSEEdit.
published: true
date: 2023-08-18T08:38:49.390Z
tags: 
editor: markdown
dateCreated: 2023-08-18T08:38:49.390Z
---

> **Prerequisite(s):** [Tools Folder](/tools/tools-folder), [Mod Organizer 2](/mo2)

# SSEEdit

**xEdit** is a tool for viewing and modifying Bethesda plugins.

Versions of the tool exist for most Bethesda games and its name changes depending on the game: For example, xEdit for Skyrim SE is known as **SSEEdit** while xEdit for Skyrim LE was called **TES5Edit** and **FO4Edit** is used in Fallout 4 modding.

Once you have installed the programme, you can use it for any game that is supported by either changing the name of the executable, or starting it with a specific argument such as `-sse` for Skyrim SE.

> You will see the tool referred to as SSEEdit and xEdit interchangeably.
{.is-info}

# Installation

SSEEdit is hosted on the Nexus:

- Download the latest version of [SSEEdit](https://www.nexusmods.com/skyrimspecialedition/mods/164).
- Create a folder called **SSEEdit** in your **Tools** folder.
- Extract the downloaded archive into the new folder.

## MO2 Integration

Plugins are data folder files which means **SSEEdit** must be run through Mod Organizer 2 in order to access its virtual data folder.

- In Mod Organizer 2, click the [gears icon](/basics/mo2-executables-settings.png) in the Toolbar to open the **Executables** settings.
- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Tools\SSEEdit\` and double-click **SSEEdit.exe**.
- Click **OK** to add the executable to Mod Organizer 2.

![add-sseedit-to-mo2.png](/tools/add-sseedit-to-mo2.png){.align-center}

I recommend selecting **SSEEdit** from the executables drop-down and adding a shortcut to the Toolbar for quick access.

# SSEEdit Ref Cache

When loading up your plugins in SSEEdit, the tool will spend a considerable amount of time processing all records. To cut down on the loading time, SSEEdit creates a **ref cache** (caching [reference records](/knowledge-base/references) for each plugin) which reduces the startup time from several minutes to twenty seconds or less.

The cache files can be saved into the **SSEEdit** folder so they do not clutter up the ***Overwrite***:

- In Mod Organizer 2, click the [gears icon](/bascis/mo2-executables-settings.png) in the Toolbar to open the **Executables** settings.
- Select **SSEEdit** in the list of executables.
- Under **Arguments** add the `-c:"filepath"` argument along with the file path.

Your file path should point to your SSEEdit installation and end in a `\cache\` folder. This folder does not have to exist, it will be created by SSEEdit upon generating the first cache files. <u>The file path must end on a trailing backslash.</u>

**Example:**

```
-c:"G:\Modding Tools\SSEEdit\cache\"
```

![sseedit-refcache-argument.png](/tools/sseedit-refcache-argument.png){.align-center}

## Generating Ref Cache

Launch **SSEEdit** through Mod Organizer 2 and click **OK** in the **Plugin Selection Window** to load all currently installed plugins. This will take several minutes as SSEEdit builds the cache files.

You can quit once the log at the bottom returns `Background loader: finished` or once you are prompted to activate ModGroups.

Check your `\Tools\SSEEdit\cache\` folder to make sure the files were saved to the correct location.

# Quick Auto Clean

You should also install the **Quick Auto Clean** executable in case you need to [clean plugins](/guides-tutorials/cleaning-plugins).

- In Mod Organizer 2, click the [gears icon](/basics/mo2-executables-settings.png) in the Toolbar to open the **Executables** settings.
- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Tools\SSEEdit\` and double-click **SSEEditQuickAutoClean.exe**.
- Click **OK** to add the executable to Mod Organizer 2.

<font size=2>*I like to rename the executable to "SSEEdit QAC" in the MO2 executables settings for better readability.*</font>

## -DontCache

When cleaning Dragonborn.esm with SSEEdit QAC, parts of Apocrypha will unintentionally be modified. This can be prevented by adding the -DontCache argument to the QAC exe.

- In Mod Organizer 2, click the [gears icon](/Pictures/skyforge/mo2-executables-settings.png) in the Toolbar to open the **Executables** settings.
- Select **SSEEdit QAC** in the list of executables.
- Add `-DontCache` under **Arguments**.
- Click **OK** to save your change and close the window.

# Disable Warning

To prevent the [warning window](/basics![sseedit-warning-window.png](/basics/sseedit-warning-window.png)/sseedit-warning-window.png) from appearing when trying to modify a record, add the following argument to the executables settings in Mod Organizer 2:

```
-IKnowWhatImDoing
```

![disable-warning-window.png](/tools/disable-warning-window.png){.align-center}