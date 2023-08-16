---
title: INI Files
description: About the default (vanilla) INI files.
published: true
date: 2023-08-16T12:06:39.888Z
tags: 
editor: markdown
dateCreated: 2023-08-16T11:36:00.880Z
---

# Vanilla INI Files

Various settings for Skyrim can be configured in a set of INI files:

- Skyrim.ini
- SkyrimPrefs.ini

Both can be found in the `\Documents\My Games\Skyrim Special Edition\` folder.

These INI files were regenerated during the clean install ([Steam](/getting-started/initial-setup/steam) or [GOG](getting-started/initial-setup/gog)) and a performance preset (low, medium, high, etc) was applied when opening the launcher for the first time.

There is also a `SkyrimCustom.ini` which does not exist in vanilla but can be created in the same directory to overwrite the `Skyrim.ini`.

> You can restore the set of vanilla INIs in the Documents folder by deleting them and starting Skyrim via **SkyrimSELauncher.exe**. You will be informed that the game will configure your settings (applying a preset) after which you can quit.
{.is-info}

## Valid Settings

Not all settings are valid in all INI files.

- **Skyrim.ini** can modify all settings valid in the game <u>except</u> those specific to the Launcher.
- **SkyrimCustom.ini** can modify all settings valid in the game <u>except</u> those specific to the Launcher.
- **SkyrimPrefs.ini** can modify a limited range of settings ([documented here](https://stepmodifications.org/wiki/SkyrimSE:SkyrimPrefs_INI)).

The catch is that duplicate INI settings are overwritten in the following order:

- **SkyrimPrefs.ini** >> **SkyrimCustom.ini** >> **Skyrim.ini**

> For example: If **bFXAAEnabled=** is set to **1** in the **Skyrim.ini** and set to **0** in the **SkyrimPrefs.ini**, the latter will overwrite and FXAA will be off (0) ingame.
{.is-info}

## Plugin INIs

INIs can also be attached to [plugins](/knowledge-base/plugins) (ESP, ESL, ESM). Like BSAs, they are loaded if they have the same name as the plugin.

Any setting that is <u>not valid</u> in the **SkyrimPrefs.ini** can be added to a plugin INI.

![ussep-plugin-ini.png](/knowledge-base/ussep-plugin-ini.png){.align-center}

Plugins that load INI files are displayed with a paper clip icon in the load order.

![plugin-with-ini.png](/knowledge-base/plugin-with-ini.png){.align-center}

# INI Files and MO2

## Profile-Specific INIs

Going forward, I recommend not bothering at all with the default set of INIs, nor with the settings in the launcher through which they can be modified.

Instead, make use of your <u>profile-specific INIs</u> in [Mod Organizer 2](/getting-started/initial-setup/mod-organizer-2). Each profile in a MO2 instance can hold a unique set of INIs that will replace the default ones when the game is started with that profile selected.

To enable profile-specific INI files, open the [profile settings](/basics/mo2-profiles-settings.png) and ensure **Use profile-specific Game INI files** is enabled. These INI files will be saved under `\Mod Organizer 2\profiles\<your profile>\`.

[BethINI](/tools/bethini) is able to target profile-specific INIs.

> When **copying** (duplicating) a profile in Mod Organizer 2, the profile-specific INI files will also be copied.
{.is-info}

![mo2-profile-specific-inis.png](/knowledge-base/mo2-profile-specific-inis.png){.align-center}

## Modifying INIs through MO2

You can view and edit all INI files through the INI Editor in Mod Organizer 2. It will display the profile-specific set if that option is enabled, and the default set from the Documents folder if it is not.

> When modifying INIs through the INI Editor always remember to click the **Save** button at the bottom.
{.is-warning}

![mo2-open-ini-editor.png](/basics/mo2-open-ini-editor.png){.align-center}

# INI Configuration

- [INI Configuration *How to customise the vanilla INI files with BethINI.*](/en/getting-started/initial-setup/ini-config)
{.links-list}