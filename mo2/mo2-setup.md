---
title: MO2 Setup
description: How to set up Mod Organizer 2 for Skyrim SE
published: true
date: 2023-08-17T08:25:01.196Z
tags: 
editor: markdown
dateCreated: 2023-08-15T15:37:50.614Z
---

> **Prerequisite(s):** Clean Install ([Steam](/getting-started/initial-setup/steam) or GOG)

# Installation

Mod Organizer 2 has two prerequisites. While you may already have them install, I recommend (re)installing them to be sure:

- Download [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer) and follow the instructions in the installer.
- Download the [Microsoft Visual C++ Redistributable](https://aka.ms/vs/16/release/vc_redist.x64.exe) and follow the instructions in the installer.

To finalise the installation you may be required to restart your PC.

## Downloading MO2

Mod Organizer 2 is hosted on the Nexus and on Github.

- Open the [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194?tab=files) Nexus page.
- Click the **Manual Download** button for **Mod Organizer 2** under **Main Files**.

> If you do not have **Nexus Premium**, you will need to click **Download** again on the next page after a brief countdown.
{.is-info}

![download-mo2.png](/getting-started/initial-setup/download-mo2.png){.align-center}

## Installing MO2

- Save the downloaded executable to a convenient location and double-click it.
- If there is a Windows warning, click **More Info** and **Run anyway**.

> Concerned about possible security risks? Read the [Nexus Virus Check](/knowledge-base/nexus-virus-check) article.
{.is-info}

## Installer Configuration

In the installer, accept the license agreement and proceed to the next page.

You will be asked where to install Mod Organizer 2.

- Your MO2 instance and the vanilla game *should* be **located on the same drive**.
- Selecting **an SSD or NVME is highly recommended** as it will improve load times and in-game performance.
- The MO2 folder **will contain all your mods** which may add up to **100GB** and more.
  
> Make sure you have <u>at least 50GB of free space</u> on whichever hard drive you choose. That will be sufficient to get you started.
{.is-success}

![mo2-installation-directory.png](/getting-started/initial-setup/mo2-installation-directory.png){.align-center}

- For the rest of the installer, you can simply keep clicking **Next** to install the tool with all components into your chosen directory.
- Click **Finish** once all files have been extracted.
- Mod Organizer 2 will be launched automatically so you can proceed with the next step.

## Instance Setup

After the initial installation process, the **Instance Manager** will open where we will create a new **portable instance**. These are <u>self-contained</u> and allow you to run as many copies of Mod Organizer 2 as you like, for various games or different setups.

- Click the **Create new instance** button to proceed.

![mo2-new-instance.png](/getting-started/initial-setup/mo2-new-instance.png){.align-center}
  
- Click **Next** in the configuration window.
- Select **Create a portable instance** on the next page.
- On the next page in the configuration wizard, select **Skyrim Special Edition**.
- Click **Next** again on the following page to confirm using your MO2 installation folder for all sub directories.
- Click **Connect to Nexus**\* and switch to the browser to authorise MO2 to connect your account.
	- *In the MO2 installer, you should see: **Linked with Nexus successfully**.*
- Proceed to the next step and click **Finish** to finalise your new MO2 instance.

<font size="2">\**If you are not prompted to connect MO2 to the Nexus, you have likely already done this for a previous MO2 installation.*</font>

## First Launch

Mod Organizer 2 should launch automatically.

- Go through the tutorial if you never used MO2 before.
- If asked whether MO2 should handle NXM links, click **Yes**.
	- *This enables automatic downloads from the Nexus through MO2.*

I recommend right-clicking the MO2 icon on your taskbar and **pinning** it for quick access.

# MO2 Settings

Open the **Settings** by clicking the first icon on the right in the toolbar.

![mo2-open-settings.png](/getting-started/initial-setup/mo2-open-settings.png){.align-center}

## Settings: General

Under **Download List**, I highly recommend checking **Show meta information** and **Compact list**. This will affect the Downloads tab in the right pane of MO2 where all downloaded files will appear. As the list grows, a more compact view with information about the file version and type will become invaluable.

>Check out the [default settings](https://i.imgur.com/BW4F4tD.png) versus the [compact settings](https://i.imgur.com/eNnzd6p.png).
{.is-info}

## Settings: Themes

Under **Style**, you can try out various other themes if the default light theme is not to your liking. If you want a simple dark theme, I recommend the **1809 Dark Mode** option. It is similar to the default light theme and will make following along with most screenshots on the wiki easier.

> Make sure to restart MO2 after changing the theme.
{.is-warning}

The **Colors** section below affects the colors in which mods and separators will light up when highlighting them. I strongly suggest not tampering with them until you have a proper understanding of mod order and asset conflicts.

## Settings: Paths

With Mod Organizer 2 as a portable instance, all file paths to the various directories are currently within the MO2 installation itself: `/%BASE_DIR%/`, the base directory. To save space you can change the path for the **Downloads**, meaning the archives from which the mods are installed, to a slower hard drive where space is not as precious.

<font size="2">\**It should be noted that keeping downloaded archives on a faster drive may speed up mod installation, including for Wabbajack list.*</font>

<mark>This is a recommendation, not a requirement. Manage your disk space as you see fit.</mark>

> The download archives are only required for the initial installation and only serve as backups afterwards. Keeping the archives is nevertheless recommended as you may want to reinstall a mod later on to choose different options if they come with an installer, or simply to restore it to the vanilla state if you modified it.
{.is-info}

![mo2-downloads-folder.png](/getting-started/initial-setup/mo2-downloads-folder.png){.align-center}

# New Profile

One of MO2's many lovely features is the ability to create an indefinite amount of self-contained **profiles**.

Every profile has its own:

- Load Order
- Mod Order
- Saves (optional)
- INI Files (optional)

## Create New Profile

- Open the MO2 profiles settings by clicking the [ID card icon](/getting-started/initial-setup/mo2-profiles-settings.png) in the **Toolbar**
- Click the **Create** button and enter a name for your profile.

I recommend naming your profile after the central mod or theme of the modlist you intend to build, like **Legacy of the Dragonborn**, **SimonRim**, or **Survival**. There is also nothing stopping you from simply calling it **Modded** as opposed to the unmodded **Default** profile.

Whether you check the **Default Game INI Settings** is up to you. I recommend leaving the option <u>enabled</u> and running BethINI later on to modify your INIs.

- Click **OK** to create your new profile and make sure it is selected.
- I recommend enabling the **Use profile-specific Save Games** option at the bottom.
- Click **Select** to quickly switch to your new profile.

