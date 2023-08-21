---
title: Creating ESL Plugins
description: How to create ESL plugins with SSEEdit.
published: true
date: 2023-08-21T08:48:08.809Z
tags: 
editor: markdown
dateCreated: 2023-08-21T08:48:08.809Z
---

> **Prerequisite(s):** [SSEEdit](/tools/sseedit)

# Creating ESL Plugins

Before starting to ESL-ify plugins in your load order, I strongly suggest familiarising yourself with the format and when/how it should be used:

- [Plugins *Plugin basics: Records, form IDs, load order, formats.*](/knowledge-base/plugins)
- [ESL Plugins *Usage and limitations of Elder Scrolls Light plugins.*](/knowledge-base/esl-plugins)
{.links-list}

## ESL Checklist

You can ESL-ify a plugin if:

1. It contains fewer than 2048 new records (or none at all).
2. It contains new records, but the Form IDs only use the final three characters.
3. It does not contain new CELL records.

If a plugin contains new records and the Form IDs use more than the final three characters, they need to be **compacted** first. Remember that compacting Form IDs will <u>break</u> all dependencies.

# ESL-ifying

You can apply the ESL flag to any ESP or ESM plugin in SSEEdit.

- Load your plugins into SSEEdit.

## Form IDs

First, you need to find out whether the plugin's Form IDs are compatible with the ESL format.

- Right-click the plugin you wish to ESL-ify and select **Compact FormIDs for ESL**.
  - *This will trigger the general warning window if you did not disable it.*

If the plugin contains no new Form IDs or only Form IDs that only use the final three characters, SSEEdit will return that there was `Nothing to do`. The plugin can be safely ESL-ified.

![sseedit-nothing-to-do.png](/guides-tutorials/sseedit-nothing-to-do.png){.align-center}

If the plugin contains new Form IDs that need to be renumbered (compacted), SSEEdit will notify you about the amount of records that need their Form IDs renumbered and that this will break dependencies (see below). If you are certain that there are no dependencies or that all dependencies are currently active and loaded, go ahead and click **Yes** to continue.

![sseedit-renumber-formids.png](/guides-tutorials/sseedit-renumber-formids.png){.align-center}

## ESL Flag

After compacting Form IDs or ensuring that there are no incompatible Form IDs, you can add the ESL flag.

- Select the plugin you wish to ESL-ify to open the **File Header** in the right pane.
- Right-click the empty space next to **Record Flags** and select **Edit**.
- Check **ESL** in the window that pops up and click **OK**.
- Close SSEEdit and save your change(s).

![esl-flag-plugin.png](/basics/esl-flag-plugin.png){.align-center}

# Full ESL

Adding the ESL flag to an ESP will create an **ESP-FE** hybrid that loads in ESP space but does not count toward the 256 ESM/ESP plugin limit. If you want to move the plugin into ESM space, you need to rename its file extension from **.ESP** to **.ESL**. This will create a full ESL.

If the plugin overwrites [references](/knowledge-base/references), you <u>must</u> also add the **ESM** flag in SSEEdit to ensure that the list of *Overriden Forms* is populated and the plugin works as intended. I would generally recommend ESM-flagging full ESLs as they are all meant to load in ESM space and there is no downside to doing this.

- [Overridden Forms *Read more about references in ESM space and the ONAM list.*](/knowledge-base/references#esm-space)
{.links-list}