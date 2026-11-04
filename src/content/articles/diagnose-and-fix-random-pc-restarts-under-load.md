---
title: "How to Diagnose and Fix Random PC Restarts Under Load (GPU/PSU Guide)"
description: "Is your PC randomly rebooting or crashing to a black screen the moment you launch a heavy game or benchmark? Follow this advanced troubleshooting guide to find the culprit."
pubDate: "2026-11-04"
updated: "2026-11-04"
author: "MyRigFoundry"
image: "/images/articles/fix-random-pc-restarts.png"
imageAlt: "High-end gaming PC components under stress testing"
category: "Hardware"
categoryName: "Hardware"
categoryUrl: "/category/hardware"
tags: ["pc-restarts", "troubleshooting", "psu", "gpu", "hardware", "gaming-pc"]
---

There is arguably nothing more infuriating in PC gaming and hardware ownership than a computer that works perfectly fine while you are browsing the web, typing documents, or watching YouTube, but instantly **shuts down and reboots without warning** the exact second you launch a graphically demanding video game or rendering workload. 

When a PC spontaneously reboots under heavy load without throwing a classic Blue Screen of Death (BSOD), it usually points to a severe hardware protection trigger—such as power supply over-current protection, thermal throttling limits being breached, or unstable voltage delivery.

In this comprehensive, deep-dive troubleshooting guide, we will walk you through how to systematically diagnose the root cause of random PC reboots under load and fix them for good.

---

## Step 1: Check Windows Event Viewer for Critical Error Codes

Before opening up your PC case and tearing down components, let Windows tell you what happened right before the power cut.

1. Press the **Windows Key + X** and select **Event Viewer**.
2. Expand **Windows Logs** on the left menu and click on **System**.
3. On the right-hand panel, click **Filter Current Log...**
4. Under *Event sources*, check **Kernel-Power** and enter event ID `41`. Click OK.
5. Look at the timestamps matching your crashes. 

*What it means:* **Event ID 41 (Kernel-Power)** simply indicates that the system rebooted without cleanly shutting first. It doesn't mean your power supply is dead; it just means power was abruptly cut or lost. If you see **WHEA-Logger (Event ID 18)**, it strongly points to a CPU hardware error, voltage instability, or an unstable overclock.

---

## Step 2: Monitor and Log Component Temperatures

Overheating is a primary trigger for emergency motherboard shutdowns. When your CPU or GPU exceeds its maximum safe junction temperature (typically 95°C to 100°C for modern processors and 85°C+ for GPUs), the hardware triggers an immediate thermal shutdown to prevent permanent physical silicon damage.

### How to Test:
1. Download and install a reliable hardware monitor like **HWMonitor** or **HWiNFO64**.
2. Launch the software in "Sensor-only" mode and keep it running in the background.
3. Open a demanding game or run a free stress test like **Cinebench** (for CPU) or **FurMark** (for GPU).
4. Watch the maximum temperature columns closely. If temperatures spike rapidly toward critical limits right before a reboot, your cooling solution is failing.

*Verification:* Ensure your CPU cooler fans are spinning at 100% under load, thermal paste isn't dried out, and the plastic peel on the CPU cooler block was removed during installation.

---

## Step 3: Test and Verify Power Supply Unit (PSU) Stability

If your temperatures look completely normal and the PC still reboots instantly during heavy GPU and CPU spikes, your **Power Supply Unit (PSU)** is the most likely suspect. 

Modern graphics cards (like the RTX 40/50 series or RX 7000/8000 series) draw massive instantaneous power transients—quick millisecond spikes that can double the card's rated TDP. If your PSU lacks the rail capacity or overall wattage headroom, its Over-Current Protection (OCP) or Over-Power Protection (OPP) will trip, instantly cutting power to protect your system.

### How to Check:
* **The Daisy-Chain Mistake:** Ensure your high-end GPU is powered by **two or three separate independent PCIe / 12VHPWR cables** running directly from the PSU, rather than using a single "daisy-chained" cable splitter.
* **Wattage Headroom:** If you are running an RTX 4080 or 4090 on an old 650W power supply, random reboots under load are guaranteed.

If your PSU is failing or underpowered, upgrading to a modern, high-efficiency, ATX 3.0 compliant power supply is mandatory. You can explore high-wattage, reliable power supplies directly via trusted retailers:

<div style="display: flex; gap: 12px; margin: 20px 0; flex-wrap: wrap;">
  <a href="https://www.amazon.com/s?k=Corsair+RM850x+Shift+Power+Supply&tag=myrigfoundry2-20" target="_blank" rel="noopener noreferrer" style="background-color: #232f3e; color: #ffffff; padding: 12px 20px; border-radius: 6px; text-decoration: none; font-weight: bold; display: inline-block;">Check Corsair RM850x on Amazon</a>
  <a href="https://www.amazon.com/s?k=Seasonic+Focus+GX-850+PSU&tag=myrigfoundry2-20" target="_blank" rel="noopener noreferrer" style="background-color: #232f3e; color: #ffffff; padding: 12px 20px; border-radius: 6px; text-decoration: none; font-weight: bold; display: inline-block;">Check Seasonic Focus 850W on Amazon</a>
</div>

---

## Step 4: Disable XMP / EXPO / Overclocks to Test Stability

Aggressive RAM overclocks (Intel XMP or AMD EXPO profiles) or unstable CPU voltage offsets are notorious for causing random game crashes, black screens, and sudden reboots under load.

### How to Test:
1. Restart your PC and repeatedly press **Del** or **F2** to enter your motherboard's UEFI/BIOS settings.
2. Locate the **XMP**, **DOCP**, or **EXPO** memory profile setting.
3. Temporarily **Disable** it (set it back to default JEDEC speeds, e.g., 4800MHz or 2133MHz).
4. Save changes (`F10`) and boot into Windows. Test your games again.

*Verification:* If the random reboots stop entirely with XMP disabled, your RAM kit is either unstable at rated speeds, needs a slight voltage bump, or your motherboard's memory topology is struggling with four sticks instead of two.

---

## Step 5: Reseat GPU, RAM, and Power Cables

Micro-vibrations, thermal expansion, or poorly seated components can cause intermittent electrical contact that breaks the moment the system draws high current under load.

### Action Plan:
1. Power down your PC completely and unplug the power cable from the wall.
2. Open both side panels of your case.
3. Remove your graphics card, inspect the PCIe slot for dust, and firmly reseat it until the retention latch clicks securely.
4. Remove your RAM sticks, wipe the contacts gently if needed, and click them back into slots **A2 and B2** (slots 2 and 4 from the CPU).
5. Unplug and firmly re-plug all modular power cables on both the component side and the PSU side.

---

## Summary Troubleshooting Checklist
* [ ] Checked Windows Event Viewer for Kernel-Power (Event 41) or WHEA errors.
* [ ] Monitored CPU and GPU temperatures under stress testing to rule out thermal throttling.
* [ ] Verified GPU power cables (avoiding daisy-chaining) and checked PSU headroom.
* [ ] Tested system stability with RAM XMP/EXPO disabled in BIOS.
* [ ] Fully reseated the graphics card, RAM modules, and all internal power connections.
* [ ] Upgraded an insufficient power supply to a reliable unit like the <a href="https://www.amazon.com/s?k=Corsair+RM850x+Shift+Power+Supply&tag=myrigfoundry2-20" target="_blank" rel="noopener noreferrer" style="color: #0066c0; font-weight: bold;">Corsair RM850x Shift PSU</a>.