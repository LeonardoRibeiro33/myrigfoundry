---
title: "How to Fix 100% Disk Usage in Windows 11 (Ultimate Guide)"
description: "Is your Windows 11 PC freezing or lagging due to 100% disk usage? Follow this step-by-step guide to diagnose system bottlenecks and permanently fix disk spikes."
pubDate: "2026-11-04"
updated: "2026-11-04"
author: "MyRigFoundry"
image: "/images/articles/fix-100-percent-disk-usage.jpg"
imageAlt: "Windows Task Manager showing 100 percent disk usage and performance bottlenecks"
category: "Performance"
categoryName: "Performance"
categoryUrl: "/category/performance"
tags: ["windows-11", "troubleshooting", "ssd", "performance", "storage"]
---

*Disclaimer: MyRigFoundry is reader-supported. When you buy through links on our site, we may earn an affiliate commission at no extra cost to you.*

There are few things more aggravating than a PC that locks up, stutters, or takes five minutes just to open a web browser. When you check the Task Manager, you see the dreaded culprit: **100% Disk Usage**. 

Even though your CPU and RAM might be sitting comfortably at low percentages, a pegged disk causes massive system-wide freezes, unresponsive applications, and unbearable load times. 

In this guide, we will walk you through the most effective methods to diagnose what is eating up your drive bandwidth and how to fix 100% disk usage in Windows 11 permanently.

---

## 1. Disable SysMain (Superfetch) Service

The **SysMain** service (formerly known as Superfetch) preloads applications you frequently use into your RAM to speed up launch times. However, on many systems—especially those running traditional hard drives (HDDs) or certain SSD configurations—it triggers relentless background read/write operations that max out disk usage.

### How to Disable It:
1. Press the **Windows Key + R** to open the Run dialog.
2. Type `services.msc` and hit Enter.
3. Scroll down the list until you find **SysMain**.
4. Right-click on **SysMain** and select **Properties**.
5. Change the *Startup type* dropdown to **Disabled**.
6. Click **Stop** under the Service status, then click **Apply** and **OK**.

Restart your computer and check if the disk spike persists in the Task Manager.

---

## 2. Disable Windows Search Indexing

Windows constantly indexes your files in the background so that search results appear instantly in the Start Menu. While convenient, this indexing process can trap older or slower drives in a continuous loop of high disk activity.

### How to Temporarily Stop It:
1. Open the Start Menu, type `cmd`, right-click on **Command Prompt**, and select **Run as administrator**.
2. Type the following command and press Enter:
   ```cmd
   net.stop "windows search"