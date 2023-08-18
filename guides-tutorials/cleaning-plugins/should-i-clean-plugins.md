---
title: Should I clean plugins?
description: What plugin "cleaning" does and when it should be done.
published: true
date: 2023-08-18T11:07:21.427Z
tags: 
editor: markdown
dateCreated: 2023-08-18T11:06:47.119Z
---

# Should I "clean" plugins?

The process of "cleaning" plugins by undeleting and disabling references and removing ITMs is somewhat controversial. It has been recommended as a basic step at the start of building a setup, often by people who do not fully grasp what "cleaning" does.

Cleaning addresses the following *potential* causes of problems:

- **Undeleting references:** References that were flagged as "Deleted" can crash the game when they are called by another record. "Cleaning" will change the flag to "Initially disabled" to prevent this.
- **Removing ITMs:** Identical-to-master (ITM) records are (usually) unintentional copies which can overwrite intentionally modified versions of the same record. "Cleaning" deletes them.

> **TL;DR:** Cleaning is generally only necessary when using [DynDOLOD](/tools/dyndolod) NG.
{.is-success}

## Official Master Files

The five **official master files** contain various deleted references and ITMs which, according to Arthmoor (of the USSEP team), will cause issues:

> If you don't clean the masters and aren't using [the USSEP], there are dirty edits in some of the DLCs that will break house purchases, wreck daedric artifact quests, and raise the possibility of navmesh related crashes. So cleaning them is generally quite useful, especially in a strictly vanilla setup.

Arthmoor specifically refers to "dirty edits" (ITMs) which can occur very easily in the [Creation Kit](/tools/ck). Though I know of no specific example, an unintentional ITM from Dragonborn.esm that overwrites a vital change in HearthFires.esm can very well break the game.

However, Arthmoor also implied that the USSEP fixes those instances. Although this is circumstantial evidence, I did not use cleaned masters in several years (and therefore users of my Wabbajack lists did not either) and no issues were ever traced back to uncleaned plugins.

> Cleaning the masters is very unlikely to fix any issues that are not already addressed by the USSEP which should always be present.
{.is-success}

## Plugins from Mods

Plugins added by mods can also have deleted references and ITMs. It is generally considered good practice to clean plugins before publishing them and the presence of these issues *can* be an indicator of sloppiness in the creation of the mod.

Nevertheless, I would not consider "cleaning" plugins from mods an essential step in building a setup. While it is true that ITMs can overwrite crucial edits from other plugins, such cases would create obvious conflicts in SSEEdit that you would be expected to check for and address anyway.

As with the official master files, I have yet to see an example of a mod where "cleaning" fixes a specific issue.

# Conclusion

I would not generally recommend "cleaning" plugins *for the sake of it*.

Undeleting large references is a prerequisite for [DynDOLOD](/tools/dyndolod) NG, so you <u>should</u> clean plugins if you intend to use that. At the very least you need to make sure there are no deleted large references.

ITMs can sometimes cause unintentional conflicts, but those will be very visible in SSEEdit when you do your conflict resolution. You can address them then.

It is unlikely that "cleaning" ever *breaks* anything, so there is nothing wrong with doing it. For the most part it simply does not fix anything, either. Like other common practices in the modding scene, it is generally misunderstood and overrated.*

<font size=2>\**I am referring to those YouTube videos which promise to solve all your issues, turning your modded setup into the smoothest possible experience - and then simply show how to clean the official master files. No, this will not magically fix everything.*</font>

(**Intentional ITMs:** Some mods warn against cleaning because they claim to require an ITM, i.e., they require a vanilla record to be in its original form and not changed by other mods. It can be *convenient* to keep the ITM, but removing it also does not break anything as long as you ensure there is no unintentional interaction with another mod.)

> Cleaning plugins cannot address actual **errors** in plugins. These <u>must</u> be fixed which can only be done manually.
{.is-danger}
