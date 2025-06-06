# Hex 80HE - Project Specifications

**Author:** Thandi Menelas
**Last Updated:** 2025-06-05
**Description:** An open-source Hall Effect 80%/TKL keyboard, built for gaming and customization.

## I. General Specifications
- **Layout:** 80% (Tenkeyless)
- **Mounting Style:** (To be determined)
- **Connectivity:** Wired (USB-C)
- **Switches:** Hall Effect (Hot-swappable)
- **Keycaps:** Any keycaps compatible with MX-style stems
- **Case Material:** (To be determined)
- **Plate Material:** (To be determined)

### Personal Specifications
- **Switches:** Gateron Magnetic Jade Pro HE Switches
- **Keycaps:** MOA profile keycaps (or Cherry/OEM/MDA/XDA)

## II. Hardware Features
- **Microcontroller:** (To be determined, QMK compatible)
- **RGB Lighting:**
	- Per-key RGB
	- South-facing LEDs
	- Customizable effects
	- Small RGB light bar below the 6-key navigation cluster (above arrow keys)
- **Rotary Knob:**
	- Programmable
	- Replaces Insert, Home, Page Up keys
- **OLED Display:**
	- Small, positioned near the rotary knob
	- Potential uses: layer indicators, status display, memes
- **Onboard Memory:**
	- Target: Store at least 5 full profiles (keymaps, settings)
	- Method: QMK EEPROM feature or flash emulation

## III. Firmware & Software Features (QMK-based)
- **Keyboard Profiles:**
	- Up to 5 profiles stored on the keyboard
	- Each profile with its own keymap and settings
	- Layer switching via FN key combos or rotary knob
	- Import/export profiles to/from JSON files
- **Rapid Trigger (RT):**
	- Normal and Continuous modes
	- Potential for separate press/release RT sensitivity
- **Key Remapping:** Full key remapping capabilities
- **Macros:** Programmable macros
- **Dynamic Keystrokes (DKS):** Support for DKS
- **Mod Tap (MT):** Support for Mod Tap functionality
- **Toggle Key (TGL):** Support for Toggle Key functionality
- **Adjustable Actuation Points:** Customizable actuation depth for Hall Effect switches
- **Simultaneous Opposing Cardinal Directions (SOCD) Cleaning:**
	- Selectable modes:
		1. Neutral (default): both keys are ignored
		2. Last Key Wins (LKW): the last key pressed wins
		3. First Key Wins (FKW): the first key pressed wins
		4. Both Keys: both keys are registered
		5. Priority: one key has priority over the other
- **Custom Layers:**
	- User-definable layers
	- Layer switching via key combos or rotary knob

## IV. Configuration Utility
- **Type:** Web-based configurator
- **Technology:** WebHID or WebUSB
- **Features:**
	- Real-time adjustment of settings (RGB, RT sensitivity, actuation depth, layers)
	- Sync profiles from the keyboard
	- Export/import profiles as JSON files
	- Open-source

## V. Future Considerations / Stretch Goals
- **Analog Input Support:** Potential for analog input from Hall Effect switches
- **Wireless/Bluetooth Connectivity:** Revisit after initial wired version

## VI. Design Notes
- Standard TKL layout modified:
	- Top 3 navigation cluster keys (Insert, Home, Page Up) replaced by a programmable rotary knob and a small OLED display.
	- Small RGB light bar added below the remaining 6-key navigation cluster (Print Screen, Scroll Lock, Pause, Delete, End, Page Down).