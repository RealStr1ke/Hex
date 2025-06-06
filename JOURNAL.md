---
title: "Hex 80HE"
author: "Thandi Menelas"
description: "An open-source Hall Effect 80%/TKL keyboard, built for gaming and customization."
created_at: "2025-06-05"
---

<!--
## YYYY-MM-DD - Journal Entry Title
< Journal entry notes here >
--->

## 2025-06-05 23:00 — Research & Planning

Spent the day diving into custom keyboard territory for this project since it's my first ever hardware keyboard lol. I started with research into layout types, firmware options, and feature planning.

After comparing 60%, 65%, 75%, 80% (TKL), and 100%, I landed on 80% since it strikes the perfect balance between space-saving (since I'd like this to be somewhat portable) and full key access. I also plan to go **hot-swappable**, assuming I can pull it off on the PCB side.

I initially considered doing a tri-mode keyboard (Wired + Bluetooth + Wireless w/ 2.4GHz), but ended up sticking with **wired-only** for now to fully lean into QMK, which has better support for advanced features — and because I'll be using **Hall Effect switches**. That said, I might revisit wireless/bluetooth later on depending on how far I get. Also adding **RGB lighting** (south-facing LEDs — shoutout Hipyo Tech) with multiple customizable effects.

Inspired by Wooting and DrunkDeer (especially since I play osu!), here's the feature set I'm planning:

- **Keyboard Profiles (w/ FN layers)** 
  - Up to 5 profiles (hopefully saved onto the keyboard), each with its own keymap and settings
  - Layer switching via FN key combos or the rotary knob
  - Import/export profiles to/from JSON files for easy sharing and backup
- **Rapid Trigger**, both normal and continuous (with potential for separate press/release RT sensitivity)
- **Key Remapping**
- **Macros**
- **Dynamic Keystrokes (DKS)** (cloutiful method 💀 iykyk)
- **Mod Tap (MT)**
- **Toggle Key (TGL)**
- **Adjustable Actuation Points**
- **SOCD** with selectable modes:
  1. Neutral (default): both keys are ignored
  2. Last Key Wins (LKW): the last key pressed wins
  3. First Key Wins (FKW): the first key pressed wins
  4. Both Keys: both keys are registered
  5. Priority: one key has priority over the other (e.g., left arrow over right arrow)
- **Custom Layers** with layer switching via key combos or the rotary knob
Design-wise, I'm modifying the standard TKL layout: removing the top 3 nav cluster keys (Insert, Home, Page Up) and replacing them with a **programmable rotary knob** and a **small OLED display**. I haven't decided what to do with the OLED just yet — maybe layer indicators, maybe memes. I'm also adding a small RGB light bar below the 6 keys, not sure what to do with that either, but it should look cool lol.

Still on the fence about **analog input support**, but that's on the "future if possible" list since I still need to survive the initial build lol. 

Looking into onboard memory support for storing profiles directly on the keyboard — will probably use QMK's EEPROM feature or emulate it via flash. Target is to store at least 5 full profiles, each with custom keymaps, rapid trigger settings, etc.

Also planning a custom web-based configurator built using **WebHID or WebUSB** to let me tweak these settings easily from the browser. Ideally, I'll be able to:
- Sync profiles from the keyboard
- Export/import JSON configs
- Adjust settings like RGB, RT sensitivity, actuation depth, and layers in real-time

Might reference VIA/Vial for ideas but plan to make something personalized and open-source.
