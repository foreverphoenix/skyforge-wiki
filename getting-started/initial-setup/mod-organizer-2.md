---
title: Mod Organizer 2
description: How to set up Mod Organizer 2 for Skyrim SE
published: true
date: 2023-08-16T08:21:26.629Z
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

### Installer Configuration

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

I recommend disabling the log at the bottom as it is mostly unnecessary:

![mo2-new-instance.png](/getting-started/initial-setup/mo2-new-instance.png){.align-center}

I also recommend right-clicking the MO2 icon on your taskbar and **pinning** it for quick access.

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

### Create New Profile

Open the MO2 profiles settings by clicking the ID card icon in the **Toolbar**.

![MO2 Profiles Settings](/Pictures/skyforge/tool-setup/mo2/mo2-profiles-settings.png)

Click the **Create** button and enter a name for your profile.

I recommend naming your profile after the central mod or theme of the modlist you intend to build, like **Legacy of the Dragonborn**, **SimonRim**, or **Survival**. There is also nothing stopping you from simply calling it **Modded** as opposed to the unmodded **Default** profile.

{{< alert color="info" >}}If you are following the **Core Module**, you can name it that.{{< /alert >}}

Whether you check the **Default Game INI Settings** is really up to you. I recommend leaving the option enabled and running BethINI later on to modify your INIs.

- Click **OK** to create your new profile.
- I recommend enabling the **Use profile-specific Save Games** option at the bottom (while having your new profile selected).
- Click **Select** to quickly switch to your new profile.

## Interface Adjustments

Below are my personal adjustments to the Mod Organizer 2 interface. Take them as suggestions (or ignore them).

{{< alert color="warning" >}}If you are following the **Core Module** please do copy at least my changes to the categories displayed in the left pane.{{< /alert >}}

### The Right Pane

The *right pane* of Mod Organizer 2 features a number of tabs, none of which require much space to properly display. I typically reduce it take up about a fourth of the entire interface, dragging around the columns in the **Plugins** tab so that all options are comfortably displayed without wasting too much space on the **Mod Index** column.

### The Left Pane

The *left pane* of Mod Organizer 2 displays the **mod order**.

Clicking on the sorting columns above the mod order, you will see a number of options.

![MO Columns](/Pictures/skyforge/tool-setup/mo2/adjust-mo2-columns.png)

- ✔️**Conflicts:** Displays little icons to show overwrites.
- ✔️**Flags:** Not necessary, but recommended. Shows if notes are appended to a mod.*
- ✔️**Content:** Very helpful because it shows you which types of assets are contained in a mod.
- ❌**Category:** Uses Nexus categories by default. Separators are better for sorting.**
- ❌**Nexus ID:** The ID of the respective mod (which is the combination of numbers at the end of its URL).
- ✔️**Source Game:** Useful when mixing Skyrim LE and Skyrim SE mods which is not very common anymore.
- ✔️**Version:** Helpful for tracking updates.
- ❌**Installation:** Displays the date of installation. Not sure what you would need this for.
- ✔️**Priority:** Shows the position in the mod order. Does not hurt to leave on.
- ✔️**Notes:** See short notes at a glance. (AKA my favourite thing about MO2.)

<font size=2>\**There are also flags to remind you of endorsing mods and to show the tracking status. The tracking feature never worked properly for me and the only mods I have not endorsed are my own, so I typically disable both **Endorsement Integration** and **Tracking Integration** in the MO2 settings (Nexus tab). Disable these features or leave them active, it is up to you.*</font>

<font size=2>\*\**You can also create a set of custom categories (instructions forthcoming).*</font>

### My MO2 Layout

After some re-arranging of columns and ratios, this is what my MO2 instance (on a 1080p monitor) looks like:

([Click here to view the picture in full size.](/Pictures/skyforge/tool-setup/mo2/mo2-my-layout.png))

![My Layout](/Pictures/skyforge/tool-setup/mo2/mo2-my-layout.png)

---

#### If you are currently working through the Core Module, return to [Step 1](/skyforge/beginners-guide/step1/#ui-overview).