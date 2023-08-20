---
title: Porting Plugins
description: How to port Skyrim LE plugins to Skyrim SE using the Creation Kit.
published: true
date: 2023-08-20T09:44:41.257Z
tags: 
editor: markdown
dateCreated: 2023-08-20T09:37:07.809Z
---

> **Prerequisite(s):** [Mod Organizer 2](/mo2), [Creation Kit](/tools/ck), [SSEEdit](/tools/sseedit)

# Porting Plugins

<mark>All plugins that were created for Skyrim LE should be resaved in the Skyrim SE Creation Kit.</mark>

In Skyrim SE, some records in the vanilla game files have the new **form version 44** as opposed to the previous **form version 43** and it has been discovered that the form version of user-made SLE plugins changes from 43 to 44 when resaving them in the Creation Kit. If this is not done, the plugin <u>may</u> cause issues when loaded in Skyrim SE (including save game corruption and apparently crashes).

> Form version 43 in SSE plugins are not always problematic. Refer to this [excellent article](https://davidjcobb.github.io/skyrim-writings/articles/form-versions-43-and-44.html) by DavidJCobb if you are interested in learning about the difference between form versions and when it matters.
{.is-info}

## MO2 Warning

Mod Organizer 2 will detect plugins with Form Version 43 when they are present in the load order. Again, this does not necessarily mean that the plugin contains corrupted data, but it should be resaved to be safe.

Using xEdit scripts to check for wrong form versions in your load order is unnecessary given the MO2 warning.

![mo2-form-43-warning.png](/guides-tutorials/mo2-form-43-warning.png){.align-center}

## SSEEdit Plugin Header

You can see a plugin's form version in the **Plugin Header** in SSEEdit:

![form-version-43.png](/guides-tutorials/form-version-43.png){.align-center}

# Resaving Plugins

Converting a plugin is as easy as opening and saving it in the SSE Creation Kit. This should be done with [SSE Creation Kit Fixes](https://skyforge.wiki/tools/ck/ck-fixes) installed as the CK still misses some forms that require conversion. 

- Run the **Creation Kit** through Mod Organizer 2.
- Click the little folder icon in the toolbar to open a plugin.

![ck-open-plugin.png](/guides-tutorials/ck-open-plugin.png){.align-center}

You can only ever load <u>one</u> active plugin in the Creation Kit. If you have multiple SLE plugins, resave them one at a time.

- Select the plugin you wish to resave and click **Set as Active File**.
- Click **OK** to load the plugin.

This will load the plugin and its masters. Wait until the CK says "done".

![ck-done-loading.png](/guides-tutorials/ck-done-loading.png){.align-center}

## Save Plugin

- Go to **File** > **Save** or click the **Save** icon in the Toolbar.
- Close the Creation Kit.

![ck-save-plugin.png](/guides-tutorials/ck-save-plugin.png){.align-center}

## Form Version

As you can see in SSEEdit, the plugin was converted successfully:

![form-version-44.png](/guides-tutorials/form-version-44.png){.align-center}