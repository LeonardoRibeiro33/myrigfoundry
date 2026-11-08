
---
title: "PC Case Fans Not Spinning: How to Diagnose and Fix It"
description: "Are your PC case fans not spinning? Learn how to check fan connections, BIOS settings, PWM modes, and fan hubs to restore proper cooling."
category: "HARDWARE"
categoryName: "Hardware"
categoryUrl: "/hardware/"
updated: "November 8, 2026"
---

<div class="article-summary">
  <strong>Quick answer:</strong> If your PC case fans are not spinning, first check whether Zero-RPM mode is enabled. Then inspect fan connections, motherboard headers, BIOS settings, and any fan hub. A loose power cable or incorrect PWM/DC setting may prevent fans from starting.
</div>

PC case fans help maintain airflow and keep your components cool. When they stop spinning, the cause may be a normal fan-control feature, a connection problem, or a defective component.

Before replacing anything, follow these checks to identify the problem.

<figure class="article-figure">
  <img src="/images/articles/pc-case-fans-not-spinning/pc-case-fans-not-spinning-hero.png" alt="PC case fans not spinning troubleshooting guide showing fan connections and BIOS fan control" loading="lazy" />
  <figcaption>Understanding fan connections and BIOS settings can help identify why your case fans are not spinning.</figcaption>
</figure>

## 1. Check Zero-RPM Mode

Some motherboards and fan controllers stop case fans when temperatures are low. This feature is commonly called Zero RPM or Fan Stop.

To check:

- Restart your PC and enter the BIOS.
- Open Hardware Monitor or Fan Control.
- Look for Zero RPM or Fan Stop.
- Temporarily select a Standard or Performance profile.
- Check whether the fans start spinning.

If the fans work after changing the profile, the hardware may be fine. The original fan curve was simply keeping them stopped.

## 2. Inspect Fan Connections

If the fans still do not spin, check their power connections.

Shut down your PC, switch off the power supply, and unplug the power cable before opening the case.

Check that:

- Fan connectors are firmly attached.
- Cables are connected to compatible motherboard headers.
- No cable or object is blocking the fan blades.
- Any fan hub has its required power connection.

Motherboard fan headers are commonly labeled `SYS_FAN`, `CHA_FAN`, or `CASE_FAN`.

## 3. Check PWM and DC Settings

Incorrect fan-control settings can prevent a fan from starting correctly.

There are two common fan types:

- **3-pin fans:** Usually use DC or voltage control.
- **4-pin fans:** Usually use PWM control.

Open your BIOS and find the fan-control settings. Make sure the selected mode matches the fan connected to that header.

If you are unsure, check your motherboard manual. Some motherboards also support automatic detection.

## 4. Check the Fan Hub

If several case fans stopped working at the same time, the fan hub may be responsible.

Many powered fan hubs require:

- SATA power from the power supply.
- A control cable connected to a motherboard fan header.

Check both connections.

If possible, test one fan directly on a compatible motherboard header. This helps determine whether the problem comes from the fan or the hub.

## 5. Test the Fan Individually

If only one fan is not spinning, test it separately.

With the PC powered off and unplugged:

1. Disconnect the suspect fan.
2. Connect it to another compatible motherboard fan header.
3. Reconnect everything securely.
4. Start the PC and check whether it spins.

If another working fan also fails on the same header, the motherboard header or its configuration may be responsible.

If the suspect fan fails while another fan works on that header, the fan or its cable may be defective.

## 6. Clean the Fan and Check for Obstructions

Dust buildup and physical obstructions can interfere with fan movement.

Check for:

- Dust accumulated around the blades.
- Cables touching the fan.
- Loose mounting screws.
- Unusual grinding or clicking noises.

Clean the fan carefully with a soft brush or suitable compressed air. Keep the computer powered off during cleaning.

If a fan continues making abnormal noises or does not rotate correctly, replacement may be necessary.

## Recommended PC Cooling Accessories

If troubleshooting reveals a damaged fan or an inadequate connection setup, these accessories may help:

- [120mm PWM PC case fans](https://www.amazon.com/s?k=120mm+PWM+PC+case+fan&tag=myrigfoundry2-20)
- [PWM fan hub with SATA power](https://www.amazon.com/s?k=PWM+fan+hub+SATA+power&tag=myrigfoundry2-20)
- [PC dust cleaning kit](https://www.amazon.com/s?k=computer+cleaning+kit&tag=myrigfoundry2-20)

<em>As an Amazon Associate, MyRigFoundry earns from qualifying purchases.</em>

## Frequently Asked Questions

### Why do my PC fans spin briefly and then stop?

Some systems use a Zero-RPM profile. If temperatures are low, the fans may stop intentionally. Check your BIOS fan curve before assuming there is a hardware failure.

### Why are all my case fans not spinning?

When multiple fans stop simultaneously, check shared connections first. A disconnected fan hub, missing SATA power, or incorrect BIOS setting can affect several fans at once.

### Can I use a 3-pin fan on a 4-pin motherboard header?

Many 4-pin motherboard headers support 3-pin fans, but speed control may work differently. Check your motherboard documentation and use the appropriate DC control mode when available.

### Should I keep using my PC if the fans are not working?

Avoid demanding workloads if temperatures are rising and cooling is not functioning correctly. Restore proper cooling before gaming or running intensive applications.

## Final Thoughts

When PC case fans stop spinning, the cause is not always a defective fan. Zero-RPM settings, incorrect PWM/DC modes, loose connections, and fan hubs can all be responsible.

Start with the simplest checks, test individual components, and replace hardware only after identifying the actual problem.

## Official Resources

- [ASUS Support – Troubleshooting](https://www.asus.com/support/)
- [Noctua – Fan Troubleshooting FAQ](https://www.noctua.at/en/support/faqs/my-fan-is-not-working-as-intended-is-it-faulty)
- [darkFlash Support](https://www.darkflash.com/support/)

## Related Fixes

- [PC Randomly Restarts Under Load](/hardware/diagnose-and-fix-random-pc-restarts-under-load/)
- [PC Freezes Only When Idle](/performance/pc-freezes-only-when-idle/)
- [PC Stutters After Sleep](/performance/pc-stutters-after-sleep/)
