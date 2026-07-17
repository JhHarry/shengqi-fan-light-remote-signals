# SHENGQI 3-Speed Fan Light Remote Signal Collection

## Overview

This repository contains Sub-GHz RF signal files for the **SHENGQI 3-Speed Invisible Ceiling Fan Light** remote controller. These signals were captured using a [Flipper Zero](https://flipperzero.one/) device in `.sub` format, suitable for signal analysis, backup, or replay.

## Compatible Device

- **Brand**: SHENGQI (胜崎)
- **Product**: 3-Speed Invisible Ceiling Fan Light (with remote control)
- **Type**: Universal ceiling fan light remote control switch/receiver accessory

## Signal List

| File | Function | Frequency | Protocol |
|------|----------|-----------|----------|
| `Fan_off.sub` | Fan ON/Off | 433.92 MHz | Princeton |
| `Fan_low.sub` | Fan Low Speed | 433.92 MHz | Princeton |
| `Fan_mid.sub` | Fan Medium Speed | 433.92 MHz | Princeton |
| `Fan_high.sub` | Fan High Speed | 433.92 MHz | Princeton |
| `Fan_1h.sub` | Timer 1 Hour | 433.92 MHz | Princeton |
| `Fan_2h.sub` | Timer 2 Hours | 433.92 MHz | Princeton |
| `Fan_4h.sub` | Timer 4 Hours | 433.92 MHz | Princeton |
| `Fan_8h.sub` | Timer 8 Hours | 433.92 MHz | Princeton |
| `Light_control.sub` | Light On/Off | 433.92 MHz | Princeton |

## Technical Specifications

- **Frequency**: 433.92 MHz
- **Modulation**: OOK (On-Off Keying)
- **Protocol**: Princeton
- **Data Width**: 24-bit
- **Time Element (TE)**: 360 μs
- **Guard Time**: 31

## File Format

All `.sub` files follow the Flipper Zero Sub-GHz file format specification:

```
Filetype: Flipper SubGhz Key File
Version: 1
Frequency: 433920000
Preset: FuriHalSubGhzPresetOok650Async
Protocol: Princeton
Bit: 24
Key: 00 00 00 00 00 49 XX XX
TE: 360
Guard_time: 31
```

## Usage with Flipper Zero

1. Copy the `.sub` files to the `subghz/` directory on your Flipper Zero's SD card
2. Open the **Sub-GHz** application on your Flipper Zero
3. Navigate to **Read** → **Saved**, and locate the signal file
4. Select **Send** to transmit the signal

## Use Cases

- Signal analysis using SDR equipment
- Reference data for cloning remote controllers
- Smart home integration (e.g., via Home Assistant + Flipper Zero or other RF transmitter modules)

## Key Code Reference

| Function | Key (Hex) |
|----------|-----------|
| Fan Off | `00 00 00 00 00 49 03 8C` |
| Fan Low | `00 00 00 00 00 49 03 88` |
| Fan Medium | `00 00 00 00 00 49 03 82` |
| Fan High | `00 00 00 00 00 49 03 86` |
| Timer 1h | `00 00 00 00 00 49 03 84` |
| Timer 2h | `00 00 00 00 00 49 03 81` |
| Timer 4h | `00 00 00 00 00 49 03 83` |
| Timer 8h | `00 00 00 00 00 49 03 8A` |
| Light Control | `00 00 00 00 00 49 03 85` |

## Disclaimer

### Legal & Compliance Notice

The Sub-GHz RF signal files provided in this repository are intended **solely for educational, research, and study purposes**. Users assume all risks and responsibilities associated with the use of these signals.

- **Authorization Required**: Only use these signals on devices that you legally own or for which you have obtained explicit authorization. Unauthorized use of these signals to control devices belonging to others may violate applicable laws and regulations.
- **Radio Frequency Regulations**: Different countries and regions impose varying legal restrictions on radio frequency transmitting equipment. Before transmitting any RF signals, users must understand and comply with the radio regulations of their respective country or region. Unauthorized operation of radio transmitters (including but not limited to devices such as the Flipper Zero) may constitute an illegal act.
- **Prohibition of Illegal Use**: The signal files in this repository must not be used for any illegal activities, including but not limited to: unauthorized device control, interference with legitimate communications, infringement of property rights, or invasion of privacy.
- **No Liability**: The maintainers and contributors of this repository shall not be held liable for any direct or indirect damages, legal liabilities, equipment damage, or legal consequences arising from the use of these signal files. By using these files, users acknowledge that they understand the aforementioned risks and agree to assume full responsibility.
- **Security**: These signals are intended as backups and research references only. Please store them securely to prevent unauthorized access and misuse by third parties.

### Intellectual Property Notice

The RF signal codes included in this repository originate from devices manufactured under the SHENGQI (胜崎) brand. All relevant trademarks, product names, and technical specifications are the property of their respective owners. This repository is not affiliated with, endorsed by, authorized by, or sponsored by SHENGQI (胜崎) or its associated companies.

## License

The documentation and accompanying files in this repository are licensed under the [GNU General Public License v3.0 (GPL v3)](https://www.gnu.org/licenses/gpl-3.0.html). See the [LICENSE](LICENSE) file for details.

```
Copyright (C) 2025

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
```
