---
title: BSA Profile
description: How to create a CAO profile for creating and unpacking BSAs.
published: true
date: 2023-08-17T11:25:19.886Z
tags: 
editor: markdown
dateCreated: 2023-08-17T11:25:19.886Z
---

> **Prerequisite(s):** [Cathedral Assets Optimizer](/tools/cao)

# BSA Profile

**Cathedral Assets Optimizer** can be used to pack and unpack BSAs (archives). A dedicated profile is helpful for quick access to the correct configuration.

## Create new profile

- Open **Cathedral Assets Optimizer** and make sure the **SSE** profile is selected at the top.
- Check the option to **Show advanced settings**.

![cao-sse-profile.png](/tools/cao-sse-profile.png){.align-center}

- Click the **New** button to create a new profile and click **OK** to the infobox.
- Enter **SSE - Create BSA** as the name.
- Confirm to use the **SSE** profile as the basis.

(When creating a new profile, I recommend using the premade profile for the same game as the base.)

### BSA Tab

In the **BSA** tab, you will want to configure the options as follows:

![BSA Tab BSA](/Pictures/skyforge/tool-setup/cao/bsa-profile-bsa.png)

**Delete source files** is an option I tend to keep disabled just in case I messed something up. If I did, it is easier to delete the BSA and run CAO again than having to first unpack the created archive(s). Of course, this means you will always have to manually delete the source files after BSA creation. Decide for yourself whether or not to disable this option.

**Maximum Size:** <u>I recommend not changing this option.</u> BSA maximum sizes differ by game (see below) so if you use CAO for different games (i.e., Skyrim SE and Fallout 4), make sure to use separate Create BSA profiles for them.

{{< alert color="info" >}}If memory serves, Skyrim LE BSAs were limited to 2GB while Fallout 4 BSAs can be up to 4GB in size. I am not sure about Skyrim SE BSAs but keeping them below 2GB in size seems like the safest option. None of the vanilla BSAs exceed 2GB.{{< /alert >}}

### Other Tabs

I recommend leaving everything <u>disabled</u> in the other three tabs.

This is because I find it to be generally easier to do one *thing* at a time. Check through one mod at a time, run it through Octagon if you find that its textures are missing mipmaps, then run it through CAO to pack it into a BSA if necessary. Being very deliberate about how you modify files and going step-by-step can help avoid seemingly inexplicable issues down the line.