# Inside a Computer System — TryHackMe Writeup

- **Room:** Inside a Computer System
- **Path:** Pre Security
- **Date Completed:** <!-- add date, e.g. 2026-09-19 -->
- **Room Link:** <!-- add room URL, e.g. https://tryhackme.com/room/insideamachine -->

## Summary

This room breaks down the fundamental hardware components inside a computer and walks through what physically happens between pressing the power button and the operating system taking over. It's a foundational room aimed at building the hardware literacy needed before diving into more advanced security topics.

## Key Concepts

### Task 1: Introduction

- **Core concept:** You can't secure a system without first understanding its architecture and components.
- **Analogy:** Defending an unknown system is like protecting a castle without knowing its layout, entrances, or where the valuables are kept.

### Task 2: Inside a Computer System

| Component | Function | Human Analogy |
|---|---|---|
| **Motherboard** | Main circuit board connecting all physical components | Skeleton / Nervous System |
| **CPU** (Central Processing Unit) | Executes calculations and processes instructions | Brain |
| **RAM** (Random Access Memory) | High-speed, **volatile** short-term memory for actively used data | Short-term memory |
| **Storage** (HDD/SSD) | **Non-volatile** long-term memory for files, apps, and OS data | Long-term memory |
| **PSU** (Power Supply Unit) | Converts electrical current to power every component | Heart pumping blood |
| **GPU** (Graphics Processing Unit) | Renders images, video, and complex graphics | Eyes / Visual perception |
| **NIC** (Network Card) | Enables communication over local networks or the internet | Mouth & Ears / Voice |

- Key distinction: **RAM is volatile** (cleared on power loss), **storage is non-volatile** (persists permanently).

### Task 3: What Happens When You Press the Start Button?

1. **Press the power button** – a physical signal tells the **PSU** to distribute power.
2. **Firmware starts** – the motherboard's firmware (**UEFI**, or legacy **BIOS**) boots up to initialize low-level hardware.
3. **POST** (Power-On Self Test) – UEFI checks that essential components (CPU, RAM, drives) are detected and functioning.
4. **Select boot device** – UEFI consults its boot priority list to locate the OS.
5. **Initiate bootloader** – the bootloader loads the OS from storage into RAM and hands off control.

- **Exercise flag:** `THM{pc5ucce55fully5t4rt3d}`

### Task 4: Conclusion

- **Key takeaway:** Understanding component interaction and the boot sequence matters for security — low-level hardware and boot processes (e.g., UEFI/BIOS, bootloaders) are frequent targets for advanced attacks (e.g., bootkits, firmware exploits).

## My Takeaways

- It surprised me how directly the hardware analogies (CPU as brain, RAM as short-term memory) map onto real security concepts like volatility — this is exactly why RAM forensics is a thing.
- I want to dig deeper into **UEFI/BIOS security** and firmware-level attacks (bootkits, Secure Boot bypasses) since this room made it clear that the boot chain is an attack surface, not just a startup formality.
- This is a good reminder that strong fundamentals in systems/hardware are the foundation for more specialized paths later (like digital forensics or malware analysis) — worth revisiting once I get further into the Pre Security path.

---

#tryhackme #presecurity #cybersecurity #careers #infosec
