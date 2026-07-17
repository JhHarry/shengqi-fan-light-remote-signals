# SHENGQI 胜崎三档风扇灯遥控信号集

## 概述

本仓库包含 **SHENGQI 胜崎三档隐形吊扇灯** 遥控器的 Sub-GHz 射频信号文件。这些信号通过 [Flipper Zero](https://flipperzero.one/) 设备捕获，格式为 `.sub` 文件，可用于信号分析、备份或重放。

## 适用设备

- **品牌**：SHENGQI 胜崎
- **产品**：三档隐形吊扇灯（带遥控器）
- **类型**：吊扇灯遥控器通用隐形吊扇灯开关配件控制接收器

## 信号列表

| 文件 | 功能 | 频率 | 协议 |
|------|------|------|------|
| `Fan_off.sub` | 风扇关闭 | 433.92 MHz | Princeton |
| `Fan_low.sub` | 风扇低速 | 433.92 MHz | Princeton |
| `Fan_mid.sub` | 风扇中速 | 433.92 MHz | Princeton |
| `Fan_high.sub` | 风扇高速 | 433.92 MHz | Princeton |
| `Fan_1h.sub` | 定时 1 小时 | 433.92 MHz | Princeton |
| `Fan_2h.sub` | 定时 2 小时 | 433.92 MHz | Princeton |
| `Fan_4h.sub` | 定时 4 小时 | 433.92 MHz | Princeton |
| `Fan_8h.sub` | 定时 8 小时 | 433.92 MHz | Princeton |
| `Light_control.sub` | 灯控开关 | 433.92 MHz | Princeton |

## 技术参数

- **频率**：433.92 MHz
- **调制方式**：OOK (On-Off Keying)
- **协议**：Princeton
- **数据位宽**：24-bit
- **时间单元 (TE)**：360 μs
- **Guard Time**：31

## 文件格式

所有 `.sub` 文件遵循 Flipper Zero 的 Sub-GHz 文件格式规范：

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

## 在 Flipper Zero 上使用

1. 将 `.sub` 文件复制到 Flipper Zero 的 SD 卡 `subghz/` 目录下
2. 在 Flipper Zero 上打开 **Sub-GHz** 应用
3. 选择 **Read** → **Saved**，找到对应信号文件
4. 选择 **Send** 发射信号

## 信号分析用途

- 使用 SDR 设备进行信号分析
- 作为克隆遥控器的参考数据
- 智能家居集成（如通过 Home Assistant + Flipper Zero 或其他 RF 发射模块）

## 按键编码参考

| 功能 | Key (Hex) |
|------|-----------|
| 风扇关闭 | `00 00 00 00 00 49 03 8C` |
| 风扇低速 | `00 00 00 00 00 49 03 88` |
| 风扇中速 | `00 00 00 00 00 49 03 82` |
| 风扇高速 | `00 00 00 00 00 49 03 86` |
| 定时 1h | `00 00 00 00 00 49 03 84` |
| 定时 2h | `00 00 00 00 00 49 03 81` |
| 定时 4h | `00 00 00 00 00 49 03 83` |
| 定时 8h | `00 00 00 00 00 49 03 8A` |
| 灯控 | `00 00 00 00 00 49 03 85` |

## 免责声明

### 法律与合规声明

本仓库提供的 Sub-GHz 射频信号文件**仅供学习、研究及教育目的使用**。使用者须自行承担使用这些信号的全部风险和责任。

- **授权要求**：请仅对您拥有合法所有权或已获得明确授权的设备使用这些信号。未经授权使用这些信号操控他人设备可能违反相关法律法规。
- **无线电法规**：不同国家和地区对无线电发射设备有不同的法律限制。使用者在发射任何射频信号前，必须了解并遵守所在国家或地区的无线电管理法规。未经许可擅自使用无线电台（包括但不限于 Flipper Zero 等设备）可能构成违法行为。
- **禁止非法用途**：严禁将本仓库中的信号文件用于任何非法活动，包括但不限于：未经授权的设备控制、干扰正常通信、侵犯他人财产权或隐私权。
- **免责**：本仓库的维护者和贡献者不对因使用这些信号文件而导致的任何直接或间接损失、法律责任、设备损坏或法律后果承担责任。使用者确认其已理解上述风险，并同意自行承担全部责任。
- **安全性**：这些信号仅作为备份和研究参考，请妥善保管，避免被他人获取后用于未经授权的用途。

### 知识产权声明

本仓库中收录的射频信号编码来源于 SHENGQI 胜崎品牌设备。相关商标、产品名称及技术规格归其各自权利人所有。本仓库与 SHENGQI 胜崎或其关联公司无任何隶属、关联、授权或赞助关系。

## 许可

本仓库中的文档及附属文件采用 [GNU General Public License v3.0 (GPL v3)](https://www.gnu.org/licenses/gpl-3.0.html) 许可。详见 [LICENSE](LICENSE) 文件。

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
