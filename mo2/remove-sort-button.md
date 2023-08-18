---
title: Remove Sort Button
description: How to remove the integrated LOOT Sort button.
published: true
date: 2023-08-18T08:06:54.089Z
tags: 
editor: markdown
dateCreated: 2023-08-18T08:06:54.089Z
---

# MO2 Sort Button

Mod Organizer 2 has integrated a stripped-down version of [LOOT](/tools/loot) for plugin sorting. It can be accessed by clicking the **Sort** button on top of the load order (**Plugins** tab in the right pane).

![loot-sort-button.png](/mo2/loot-sort-button.png){.align-center}

<mark>Even when you do want to use LOOT for your load order, you should not click the Sort button in MO2.</mark> The integrated version of LOOT is heavily outdated. It also does not include any warnings or the ability to create custom rules or groups. If you are working with LOOT, install the [full version](/tools/loot) and launch it through MO2.

> If you are a Wabbajack list curator and using the integrated version of LOOT with LOOT Config Loader and a custom masterlist, you will need the Sort button to apply it.
{.is-info}

# Remove Sort Button

If the Sort button annoys you and/or you want to sure you never accidentally press it, you can remove it from the interface with a small CSS snippet.

## Default Theme

Users of the default MO2 theme can do this by adding a new stylesheet:

- Navigate to `\Mod Organizer 2\stylesheets\`.
- Right-click anywhere and select **New** >> **Text Document**.
- Rename the file to **No Sort Button.qss**.
  - *Remember to change the file extension.*
- Open the new file in a text editor such as Notepad++.
- Paste the following:

```
/* Sort button */
#bossButton {
    qproperty-iconSize:0px;
    min-width:0px;
    width:0px;
    padding: 0 0 0 -30;
}
```

- Save your change and close the file.

Afterwards, you need to select the new stylesheet in the **Themes** tab in the Mod Organizer 2 settings.

![remove-sort-button.png](/mo2/remove-sort-button.png){.align-center}

## Different Theme

If you are using a different theme, you can modify its stylesheet file (.QSS). Open it in a text editor and use CTRL+F to see if it modifies anything about the `#bossButton` component. Add the snippet from above, replacing any other code for the button.

> The component is named after BOSS, the predecessor of LOOT.
{.is-info}

