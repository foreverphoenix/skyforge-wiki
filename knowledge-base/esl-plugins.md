---
title: ESL Plugins
description: Usage and limitations of Elder Scrolls Light plugins.
published: true
date: 2023-08-18T12:10:29.150Z
tags: 
editor: markdown
dateCreated: 2023-08-18T12:10:29.150Z
---

# ESL Plugins

- [Plugins *Plugin basics: Records, Form IDs, load order, formats.*](/knowledge-base/plugins)
{.links-list}

The **ESL** plugin format was added in the Creation Engine's 64bit upgrade for Fallout 4 and Skyrim Special Edition. It does <u>not</u> work in the 32bit version of the engine that Skyrim LE is running on.

The format was added to allow for dozens, potentially hundreds of new plugins for the official [Creation Club](/knowledge-base/creation-club), but has proved a godsent for the modding community as well because <mark>ESLs circumvent the 256 plugin limit by reducing the size of the plugins.</mark>

# ESL Form IDs

The Form IDs in ESP and ESM plugins consist of the changeable two-character **Index** and six permanent characters unique to the record. This creates the 256 plugin limit.

Meanwhile, ESL plugins have a five-character **Index:** `FExxx`.* The *hexadecimal* FE is the *decimal* 254 which means that all ESL plugins load in a single ESP/ESM plugin slot (254).

<font size=2>*\*This is why ESL-ified ESPs are also known as ESP-FEs.*</font>

<mark>**A total of 4096 ESLs can be loaded at the same time.**<mark>

## Plugin Capacity

The downside of ESLs is that they can store fewer unique Form IDs because they only have three permanent characters as opposed to six in ESPs/ESMs. Every ESL can only store 4096 unique Form IDs of which the first 2048 are reserved by the engine.

> This limit only affects <u>new records</u>. There is no limit on how many records defined in *other* plugins can be copied into an ESL (or any other plugin type for that matter).
{.is-warning}

# Creating an ESL

Even a moderately-sized load order will quickly reach the 256 ESP/ESM limit, especially through small patches and minor tweaks which makes using the ESL format unavoidable. Thankfully, many mods now come with ESL plugins right out of the gate.

A plugin can be turned into an ESL by adding the ESL flag to it.
  
- [Creating ESL Plugins *How to create ESL plugins with SSEEdit.*](/guides-tutorials/creating-esl-plugins)
{.links-list}

## Plugins without new records

If a plugin (ESP or ESM) does <u>not</u> add any new records (Form IDs), it can always be ESL-flagged. This is typically the case for patches of all kinds and minor tweaks for vanilla or other mods.

## Plugins with new records

> Never ESL-ify a plugin that adds a new interior CELL or you will [completely break it](/beginners-guide/myrwatch-broken.jpg) as soon as another plugin attempts to modify it in any way.
{.is-danger}  
  
If a plugin (ESP or ESM) <u>does</u> add new records (Form IDs), they may need to be compacted before ESL-flagging.
  
Think about the differences in the Form ID format: While an ESP/ESM Form ID can have six character (+Index), an ESL can only have three (+Index). If there are Form IDs in the mod you wish to ESL-ify that extend beyond the final three characters, they have to be renumbered first to make room for the ESL Index.

**Remember that a plugin can only be ESL-ified if it has less than 2048 new records.**
  
Notably, not <u>all</u> plugins with new records need compacting. For example, in *SkyUI_SE.esp*, the new Form IDs only use the final three characters which means the first five characters are already freed up for the ESL Index and no change is required before adding the ESL flag:

![skyui-forms.png](/knowledge-base/skyui-forms.png){.align-center}
  
## Compacting Form IDs

When ESL-ifying a plugin that contains new record, you must compact its Form IDs first. This carries a risk: **Renumbering Form IDs will break the plugins's dependencies.** Any plugin that requires it as a *master* will be unable to find the original records that it is modifying, resulting in a wave of errors that will probably crash the game.

You can avoid this by doing the following:

1. Avoid compacting Form IDs in plugins that are likely a master to many other plugins (i.e., that have many patches).
2. Compact Form IDs in plugins only when all of their dependent plugins are also present in SSEEdit at the time.

In the latter case, those dependent plugins will be updated automatically.

# ESL or ESP-FE

When should you create a full ESL and when is an ESP-FE sufficient?

The difference lies in the fact that a full ESL loads in ESM space. It handles [references](/knowledge-base/references) differently and will always be forced to the top of the load order.

  If a given plugin does <u>not</u> contain CELL records with (temporary) references and does not need to load early because of dependencies or to be overwritten by other mods, creating an **ESP-FE** is sufficient.

Otherwise, create a **full ESL**.

> Also remember that a full ESL will load in ESM space. For a plugin that happens to have a master that is an ESP, it would be impossible to load below the master as a full ESL. Therefore it can only be turned into an ESP-FE.
{.is-warning}
