---
title: Skyrim Script Extender
description: How to install the Skyrim Script Extender and related mods.
published: true
date: 2023-08-21T08:39:32.721Z
tags: 
editor: markdown
dateCreated: 2023-08-21T07:52:49.020Z
---

# Skyrim Script Extender

Of all the mods and tools, the **Skyrim Script Extender** is certainly among the most vital ones: It extends the scripting capabilities of the engine, allowing mod authors to implement features that would not have been possible otherwise.

A popular example of an SKSE-dependent feature is the [Mod Configuration Menu](/knowledge-base/mcm), or **MCM** for short, which is part of the UI overhaul mod [SkyUI](/mods/skyui). There are also a multitude of SKSE-based plugins which, among other things, fix engine-level bugs that could not have been addressed otherwise.

> **SKSE is required by many mods, including most of the essentials.** Modding Skyrim on XBOX or PS5 is not comparable to modding on PC partially because SKSE <u>cannot</u> be installed on consoles. The same is true for the PC Gamepass version of Skyrim.
{.is-warning}

## Skyrim Version

Before you proceed, familiarise yourself with the significance of version dependency and ensure you are using the recommended version of Skyrim SE.

- [Skyrim Versions *Differences between Skyrim ports and updates.*](/knowledge-base/skyrim-versions)
- [Skyrim Version Check *How to check which version of Skyrim is currently installed.*](/guides-tutorials/skyrim-version-check)
{.links-list}

## Downloading SKSE

The Script Extender is available on its [official website](https://skse.silverlock.org/) and on the Nexus. <mark>Read carefully and make sure you are downloading the correct file.</mark>

- Download the **Skyrim Script Extender** for **Steam** or **GOG** from the [Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/30379?tab=files) (**Mod Manager Download**).

The current version of SKSE for AE, build `2.x.x`, should correlate with the current Skyrim SE version, runtime `1.6.xxx`.

## Installing SKSE

SKSE is an unusual mod in that it consists of both **root folder files** and **data folder files**. You can either drop all root folder files into the actual root folder or use the [Root Builder](/mo2/root-builder) plugin in order to manage all parts of the mod in Mod Organizer 2.

- [Regular Installation](/mods/skse/regular)
- [Root Builder Installation](/mods/skse/root-builder)
{.links-list}

# SKSE INI

Two of SKSE's features need to be enabled in an INI file:

**iTintTextureResolution** allows you to adjust the texture resolution of tint masks. By default, Skyrim's tint masks (this includes war paints, make-up, or dirt masks applied to faces) can only have a resolution of 512 x 512 pixels which can look very blurry. Even if you install 2048 x 2048 pixel (2K) retextures, they will look like 512 x 512 in-game.

**ClearInvalidRegistrations** is intended to clean up orphaned OnUpdate() events and prevent saves from bloating or breaking as a result of uninstalling certain mods.

## Creating SKSE INI

The SKSE INI must be located under `\Data\SKSE\SKSE.ini`. We can use Mod Organizer 2 and create it from scratch.

- Click the [crossed tools icon](/basics/create-empty-mod.png) above the mod order and select **Create empty mod**.
- Name the new mod **Skyrim Script Extender - SKSE INI** and click **OK**.
- Right-click the new mod and select **Open in Explorer**.
- Inside the new mod folder, create another new folder called **SKSE**.
- Within that **SKSE** folder, right-click and select **New** >> **Text Document**.
- Rename the new file to **SKSE.ini**.
  - *Make sure to change the file extension from TXT to INI.*
- After changing the file extension and confirming, a warning window will pop up. Click **Yes**.

![skse-ini-creation.png](/mods/skse-ini-creation.png){.align-center}

## SKSE INI Edits for SKSE

Next, we need to populate our new INI file.

- Go back into **Mod Organizer 2** and press F5 to refresh.
- Double-click **SKSE INI** in your mod order and switch to the **INI Files** tab.
- Select the `\SKSE\SKSE.ini` file.
- Copy and paste the following into the empty file:

```
[Display]
iTintTextureResolution=2048

[General]
ClearInvalidRegistrations=1
```

> You can set the texture resolution for face tints to any resolution you like, although anything above 2048 (2K) is simply overkill unless you are planning to take a lot of close-up screenshots. Keep in mind that you will also have to install higher resolution retextures for tint masks later on for this setting to make a difference.
{.is-info}

- Hit **CTRL+S** to save your edits and close the window.
- Check the box for the new mod to enable it.

![skse-ini-mo2.png](/mods/skse-ini-mo2.png){.align-center}

## Other SKSE INI Settings

> The below INI settings **should not** be added to your SKSE INI. The section is *for your information* only and can be skipped.
{.is-danger}

Beyond the two settings that we added, there are other options that are relics of the SLE days.

One allows you to adjust memory allocation, but while memory was a real issue in Skyrim LE, the 64bit engine upgrade in Skyrim SE already solved the problem. The settings were very recently enabled in SKSE for SE; however, it is recommended to use the memory manager from [SSE Engine Fixes](/mods/essentials/#sse-engine-fixes) instead.

```
[Memory]
DefaultHeapInitialAllocMB=
ScrapHeapSizeMB=
```

There is also an option to enable diagnostics. I am not entirely certain if this is valid in SKSE for SE to begin with (the changelog makes no mention of it), but it would be irrelevant anyway. What it logs are missing master files and missing plugins in a save. You will be able to see the former in Mod Organizer 2 and the latter upon attempting to load a save after disabling plugins that it relies on.

```
[General]
EnableDiagnostics=1
```

# Address Library for SKSE

To alleviate the problem of SKSE and SKSE plugins breaking with every Skyrim update, **meh321** (the author of a number of groundbreaking mods) released **Address Library for SKSE**. This modder's resource <mark>allows SKSE plugins to become version independent from SKSE</mark> by storing their offsets in a separate database.

> Due to the substantial changes that were made to the SkyrimSE.exe in the AE update, patch **1.6.317.0**, there is now a new version of Address Library exclusively for post-AE Skyrim SE, covering versions **1.6.x**. Various SKSE plugins for SKSE AE were updated to use this version of Address Library.
{.is-info}

- Download and install the **All in one (Anniversary Edition)** main file from the [Address Library for SKSE](https://www.nexusmods.com/skyrimspecialedition/mods/32444) Nexus page.

# Test Run

Finally, give SKSE a test run.

<mark>**Always start the game by running the Script Extender through Mod Organizer 2.**</mark>

- Make sure all new mods are checked in the left pane.
- Select the **Skyrim Script Extender** from the executables drop-down menu.
- Click **Run** to launch the Skyrim Script Extender through Mod Organizer 2.

![mo2-run-skse.png](/mods/mo2-run-skse.png){.align-center}

Instead of opening the launcher, running the game through SKSE will bring you into the main menu directly.

Once you are in the main menu, open the **console**, a dev tool that will become quite handy, particularly for troubleshooting. You can bring it up by pressing the **tilde** key (location marked in blue below, in case you have trouble finding it):

![tilde.jpg](/basics/tilde.jpg){.align-center}

- In the console, type **skse** and hit **Enter** (capitalisation is irrelevant).
- It should return the version of SKSE you just installed.
- If everything works, close the console (press the tilde key again).
- Quit the game.

![skse-check-ingame-ae.jpg](/mods/skse-check-ingame-ae.jpg){.align-center}