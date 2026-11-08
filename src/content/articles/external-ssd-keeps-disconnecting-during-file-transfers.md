---
title: "External SSD Keeps Disconnecting During File Transfers: Causes and Fixes"
description: "Is your external SSD disconnecting during file transfers on Windows 10 or 11? Diagnose USB cables, ports, power settings, overheating and enclosure problems."
category: "STORAGE"
categoryName: "Storage"
categoryUrl: "/storage/"
updated: "November 8, 2026"
image: "/images/articles/external-ssd-disconnecting/external-ssd-disconnecting-hero.png"
imageAlt: "External portable SSD connected to a Windows PC with a USB-C cable"
---

<div class="article-summary">

<strong>Quick answer</strong>

If your external SSD keeps disconnecting during file transfers, start by connecting it directly to another USB port on your PC, without a hub or dock. Then test with a known-good data cable that supports the drive's required speed.

If disconnects happen mainly during long transfers, also check the enclosure's temperature, USB power behavior, and Windows Event Viewer.

Before performing repeated tests, protect important files by backing up anything you can still access. Avoid repeatedly interrupting transfers or formatting the drive, especially if it contains data you cannot replace.

</div>

You are copying a large folder to your external SSD when the transfer suddenly stops.

The drive disappears from File Explorer, Windows plays the USB disconnect sound, or the device vanishes and reconnects a few seconds later.

If this keeps happening, the SSD itself is not automatically the problem.

A loose USB-C connector, an unsuitable cable, an unstable hub, a faulty port, heat inside the enclosure, or a problem with the USB-to-storage bridge can all interrupt a transfer.

Windows power management and device drivers can also contribute in some situations.

This guide explains how to troubleshoot an external SSD that disconnects during file transfers on Windows 10 and Windows 11. The goal is to isolate the cause before you spend money on a replacement.

<figure class="article-figure">
  <img
    src="/images/articles/external-ssd-disconnecting/external-ssd-usb-connection-check.png"
    alt="External SSD connected directly to a desktop computer USB port for troubleshooting"
    loading="lazy"
  />
  <figcaption>
    Start with the complete connection path: the SSD, its cable, the USB port, and any hub or adapter between the drive and the computer.
  </figcaption>
</figure>

## 1. Protect Your Files Before Troubleshooting

Repeated disconnects during write operations can interrupt file transfers and may leave incomplete or corrupted files.

If the SSD still works long enough to access important data, copy the most valuable files to another healthy storage device first.

If Windows reports read errors, the drive repeatedly disappears, or the data is irreplaceable, stop repeated transfer tests. Consider professional data recovery rather than running repair utilities or stress tests.

Do not select **Format** or **Initialize disk** if Windows suddenly prompts you to do so for a drive that already contains files.

For now, avoid running benchmarks or copying hundreds of gigabytes just to reproduce the problem. Use a small, nonessential test file after the basic checks below.

## 2. Connect the SSD Directly to Another USB Port

The first test is simple: remove unnecessary connections from the setup.

1. Safely eject the SSD if Windows still recognizes it.
2. Disconnect it from any USB hub, monitor, dock, extension cable, or adapter.
3. Connect it directly to another USB port on the computer.
4. If possible, use a port connected directly to the motherboard rather than a front-panel port.
5. Try a small file transfer and observe whether the drive disconnects.

On a desktop PC, test a rear motherboard USB port. On a laptop, try another built-in port.

A USB-C connector does not automatically mean that the port supports the same data speed or power capabilities as every other USB-C port.

If the SSD works reliably when connected directly, the hub, dock, adapter, extension, or original port becomes a stronger suspect.

## 3. Check the USB Cable

A cable can fit the connector and still be unsuitable for reliable data transfer.

Some USB-C cables are designed primarily for charging, while others support different data rates.

Check the following:

- Use the original cable supplied with the external SSD when available.
- Inspect both connectors for visible damage, dirt, or looseness.
- Avoid excessively long or damaged cables.
- Make sure the cable supports the data rate required by your SSD.
- Test with another known-good, compatible data cable.

Do not assume that a cable is suitable just because it charges a phone or powers another device.

Charging capability and USB data capability are different specifications.

If changing only the cable stops the disconnects, the original cable was likely part of the problem.

**Optional replacement:** If your cable is damaged or does not support the required data rate, compare a reputable USB-C data cable with the correct connector type and speed.

<a href="https://www.amazon.com/s?k=USB-C+10Gbps+data+cable&tag=myrigfoundry2-20" target="_blank" rel="sponsored nofollow">Browse USB-C 10Gbps data cables on Amazon</a>

## 4. Check Whether the SSD Disconnects on Another Computer

Testing the same SSD on another computer helps separate a drive-side problem from a problem with the original PC.

Use the same known-good cable if possible, and connect directly to a USB port.

- **It disconnects on both computers:** The SSD, cable, or external enclosure becomes more suspicious.
- **It works on the second computer:** Investigate the original PC's USB ports, chipset drivers, power settings, and connected hubs.
- **It works with another cable:** The original cable may be faulty or unsuitable.

Change one variable at a time.

If you replace the cable, port, and enclosure simultaneously, you will not know which change made the difference.

## 5. Check for Overheating During Long Transfers

Some external SSDs and NVMe enclosures become warm during sustained activity.

The SSD controller and the USB bridge inside an enclosure can both generate heat.

Heat alone does not prove that the drive is overheating. However, if disconnects happen only after several minutes of heavy transfers, temperature is worth investigating.

Try these checks:

1. Place the SSD on a hard, open surface.
2. Keep it away from direct sunlight and other heat sources.
3. Do not cover it with fabric or leave it inside a closed pouch during a transfer.
4. Check the manufacturer's documentation for its operating temperature range.
5. Allow the device to cool naturally before another short test.

If the enclosure is unusually hot, has a damaged case, or repeatedly disconnects under load, stop stressing it and check the manufacturer's support guidance.

For a user-installed M.2 enclosure, confirm that the SSD is installed according to the enclosure manufacturer's instructions and that any supplied thermal pad is fitted correctly.

Do not open an integrated portable SSD that is not designed to be serviced.

## 6. Check Windows USB Power Management

Windows includes USB power-management features that can reduce power use when devices are idle.

Microsoft says USB selective suspend is enabled by default and strongly recommends that it not be disabled generally.

That means disabling every USB power-saving feature should not be the first troubleshooting step.

First establish whether the disconnect happens during active transfers, after idle time, or when the computer wakes from sleep.

If the issue appears related to idle or resume behavior, check for Windows updates and computer-manufacturer chipset or USB controller drivers.

You can review the relevant Windows power options:

1. Open **Control Panel**.
2. Select **Hardware and Sound** → **Power Options**.
3. Select **Change plan settings** beside the active power plan.
4. Select **Change advanced power settings**.
5. Expand **USB settings** if that option is available.

Do not change settings blindly. On laptops, disabling power-saving features can increase battery consumption.

Microsoft documentation:

[USB selective suspend](https://learn.microsoft.com/en-us/windows-hardware/drivers/usbcon/usb-selective-suspend)

## 7. Check Device Manager and Update the Right Drivers

A USB controller or chipset driver issue can affect how connected devices behave.

Avoid generic driver-updater utilities and download drivers only from Windows Update or the official support page for your PC or motherboard.

To check the device:

1. Right-click **Start** and open **Device Manager**.
2. Expand **Disk drives** and look for the external SSD.
3. Expand **Universal Serial Bus controllers**.
4. Look for warning icons or devices that appear and disappear when you connect the SSD.
5. Check Windows Update, including optional driver updates where appropriate.
6. Visit the PC or motherboard manufacturer's support page for the exact model and review relevant chipset or USB controller updates.

Do not uninstall random USB devices or install drivers intended for a similar but different motherboard.

If the SSD is used for important work, back up accessible files before making driver or firmware changes.

## 8. Check Windows Event Viewer for Disconnect Clues

Event Viewer can help establish whether Windows logged a disk, USB, or Plug and Play event at the time the SSD disappeared.

1. Press **Windows + X** and select **Event Viewer**.
2. Open **Windows Logs** → **System**.
3. Select **Filter Current Log**.
4. Review warnings and errors around the exact time of the disconnect.
5. Look for entries whose source relates to **Disk**, **Kernel-PnP**, or USB components.

The source and event details matter more than a single Event ID copied from an unrelated PC.

Record the timestamp, source, event ID, and message. Search the exact message on the computer or device manufacturer's support site if needed.

An event in the log does not automatically prove that Windows caused the problem. It is a clue to correlate with the physical tests.

## 9. Check the External SSD Enclosure

If your external drive is an M.2 SSD installed inside a USB enclosure, the enclosure is part of the storage path.

It contains a USB-to-storage bridge and may have its own firmware, thermal design, and compatibility limits.

A faulty or incompatible enclosure can cause symptoms that look like SSD failure.

Consider the enclosure if:

- The SSD disconnects on more than one computer.
- A different cable does not help.
- The drive becomes unstable during sustained transfers.
- The enclosure connector feels loose or damaged.
- The SSD works reliably in another compatible enclosure.

Before buying a replacement, identify the exact SSD type.

M.2 SATA and M.2 NVMe are not interchangeable in every enclosure.

Check the enclosure's supported protocol, physical size, key type, and capacity limits.

**Optional replacement:** If testing points to a faulty enclosure, look for one explicitly compatible with your SSD's interface and size.

<a href="https://www.amazon.com/s?k=USB-C+NVMe+M.2+SSD+enclosure+10Gbps&tag=myrigfoundry2-20" target="_blank" rel="sponsored nofollow">Browse USB-C NVMe M.2 enclosures on Amazon</a>

## 10. When to Suspect the SSD Itself

The SSD becomes a stronger suspect if it disconnects across multiple computers and known-good cables, or if you also notice:

- Read or write errors.
- Files that cannot be opened or copied.
- The drive disappearing during light use.
- Repeated disconnects with different compatible enclosures.
- Health warnings from the SSD manufacturer's diagnostic software.

If the manufacturer provides a diagnostic utility, use the tool for the exact model and follow its instructions.

Do not run destructive tests or firmware updates before backing up important data.

If the SSD is failing and the data matters, stop repeated testing and consider professional recovery.

Replacing the drive is not a substitute for recovering files that exist only on the failing device.

## 11. Should You Use a Powered USB Hub?

A powered USB hub can be useful when a computer's port or the existing hub setup is part of the problem.

However, it is not a universal fix for an SSD that disconnects during transfers.

Test the SSD directly first.

If it works directly but disconnects through a particular hub or dock, investigate that hub or dock.

If the device manufacturer recommends a powered hub for your specific setup, choose one that supports the required USB data rate and power requirements.

Do not add another hub simply because the SSD disconnects. More connections create more points that can fail.

<a href="https://www.amazon.com/s?k=powered+USB+3.0+hub&tag=myrigfoundry2-20" target="_blank" rel="sponsored nofollow">Browse powered USB 3.0 hubs on Amazon</a>

## Quick Troubleshooting Flow

Use this order to narrow down the cause without changing too many things at once:

1. Back up important files that are still accessible.
2. Connect the SSD directly to another USB port.
3. Remove hubs, docks, adapters, and extension cables.
4. Test with a known-good compatible data cable.
5. Try the SSD on another computer.
6. Check whether disconnects happen only during long transfers or after idle time.
7. Check for heat and inspect the enclosure and connectors.
8. Review Event Viewer around the time of the disconnect.
9. Install relevant Windows and manufacturer driver updates.
10. If the problem follows the SSD across computers and cables, investigate the enclosure and drive health.

## Frequently Asked Questions

### Why does my external SSD disconnect when copying large files?

Large transfers keep the SSD and its USB enclosure active for longer.

A weak connection, damaged cable, unstable hub, thermal issue, or enclosure problem may become more noticeable under sustained activity.

Test the cable and direct USB connection first.

### Can a USB cable cause an external SSD to disconnect?

Yes.

A damaged or unsuitable cable can interrupt data communication even if it still provides power.

Use a known-good cable that supports the data rate and connector type required by the SSD.

### Does USB selective suspend cause SSD disconnects?

USB power management can be relevant to some USB device issues, particularly around idle and resume behavior.

However, Microsoft recommends against generally disabling USB selective suspend.

First determine whether the disconnect happens during active transfers or after the device has been idle.

### Why does my external SSD disconnect only during large file transfers?

A problem that appears only during long transfers may be related to heat, cable or connector stability, the enclosure, or the drive itself.

Compare a short transfer with a longer one only after important data is backed up, and stop if errors appear.

### Should I format my external SSD if it keeps disconnecting?

No.

Formatting does not fix a loose cable, unstable USB port, power issue, or failing enclosure.

It can also erase data. Diagnose the connection and protect important files before considering any filesystem repair or formatting.

### How do I know if the SSD or the enclosure is failing?

Test the drive with a known-good cable and another computer.

If it is a user-installed M.2 SSD, a compatible known-good enclosure can help isolate the original enclosure.

If the drive continues to disconnect across multiple setups or reports read errors, the SSD itself may be failing.

## Final Thoughts

An external SSD that disconnects during file transfers does not always need to be replaced.

The most useful first checks are the USB cable, direct port connection, and behavior on another computer.

If the problem happens only during long transfers, investigate heat and the enclosure.

If it happens around idle time or wake-up, review Windows and manufacturer power-management guidance without disabling system-wide features unnecessarily.

Most importantly, protect important files before running repeated tests.

Identify which part of the connection is failing before spending money on a new SSD, enclosure, cable, or hub.

## Official Resources

- [Microsoft Learn — USB selective suspend](https://learn.microsoft.com/en-us/windows-hardware/drivers/usbcon/usb-selective-suspend)
- [Microsoft Support — Fix USB-C problems in Windows](https://support.microsoft.com/en-us/windows)
- [SanDisk Support — Common causes of slow external SSD and USB flash drive performance](https://support-en.sandisk.com/app/answers/detailweb/a_id/17047/~/common-causes-of-slow-external-ssd-and-usb-flash-drive-performance-and-data)
- [Dell Support — Fix common USB port issues](https://www.dell.com/support/contents/en-en/article/product-support/self-support-knowledgebase/fix-common-issues/usb-ports-not-working)

## Related Fixes

- [NVMe SSD Disappears After Sleep: What to Check](/storage/nvme-ssd-disappears-after-sleep/)
- [SSD at 100% Usage While Idle on Windows 11: What to Check](/storage/ssd-100-usage-while-idle-windows-11/)
- [PC Stutters After Waking From Sleep: What to Check](/performance/pc-stutters-after-sleep/)

<div class="article-note">

<strong>Affiliate disclosure:</strong> This article contains affiliate links. As an Amazon Associate, MyRigFoundry earns from qualifying purchases. We may earn a commission if you buy through these links, at no additional cost to you. Recommendations are included only where a product may be relevant to the troubleshooting step.

</div>