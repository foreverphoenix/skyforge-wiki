---
title: Nexus Virus Check
description: About the automatic virus check performed by the Nexus.
published: true
date: 2023-08-15T15:58:24.058Z
tags: 
editor: markdown
dateCreated: 2023-08-15T15:55:37.809Z
---

# VirusTotal

All files that are uploaded to the Nexus will automatically be checked for viruses by [VirusTotal](https://www.virustotal.com/gui/home/upload).

You can view the report by clicking the **checkmark** in front of the file name.

![nexus-virus-check-green.png](/knowledge-base/nexus-virus-check-green.png)

Files that exceed 250MB in size are manually verified. Occasionally, VirusTotal will detect *false positives* which may happen with tools (see **Mod Organizer 2**) in which case the file is also manually verified.

## Mod Organizer 2

Mod Organizer 2 has been known to set off Antivirus software, usually due to the way that the UVFS is implemented. At times, it may still be flagged by one of the AVs used by VirusTotal in which case it will be manually verified by the Nexus that it is safe to use.

![mo2-virus-total.png](/knowledge-base/mo2-virus-total.png)