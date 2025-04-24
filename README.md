# SpectrumBreaker
# 🚨 ESP32 2.4GHz Jammer & Wireless Attack Toolkit

> *Author:* Balwant
> *Tool Type:* Wireless Penetration Testing & Research  
> *Disclaimer:* 🔒 FOR EDUCATIONAL & RESEARCH PURPOSES ONLY

---

## 🔍 Overview

This project is a compact but powerful wireless attack tool built using *ESP32, **3x NRF24L01 modules, **OLED display, **NeoPixel LED, and **push buttons* for control.  
It supports full-spectrum scanning, jamming, and spoofing across the 2.4GHz band, including:

- 📡 *Wi-Fi Deauth + Scanner + Analyzer*
- 📶 *Full 2.4GHz Band Jammer*
- 📘 *BLE Spoofer & BLE Scanner*
- 🍏 *Sour Apple Attack*
- 💡 Real-time *status display* with OLED + NeoPixel
- 🎮 Button-based *menu navigation*

---

## 🛠 Components Used

| Component       | Function                          |
|----------------|-----------------------------------|
| ESP32           | Main controller                   |
| NRF24L01 x3     | Wireless jamming and spoofing     |
| OLED 128x32     | Display for menu/status           |
| NeoPixel LED    | Visual status indicator           |
| Push Buttons    | Menu navigation (up/down/select)  |
| Battery / USB   | Power supply                      |

---

## 🚧 Feature List

### ✅ 1. *Wi-Fi Scanner*
- Lists all nearby 2.4GHz Wi-Fi networks
- Displays SSID, RSSI, channel, encryption

### ✅ 2. *Wi-Fi Deauth Jammer*
- Disconnects all clients from selected AP
- Sends continuous deauth packets

### ✅ 3. *Full 2.4GHz Jammer*
- Uses NRF24L01 to send noise-like packets across *all channels (1-13)*
- Effectively blocks communication in 2.4GHz spectrum including:
  - Wi-Fi
  - Bluetooth Classic / BLE
  - ZigBee / RF toys

### ✅ 4. *BLE Scanner*
- Scans and lists active BLE devices
- Shows MAC address and device name

### ✅ 5. *BLE Spoofer*
- Mimics known BLE device names and MACs
- Broadcasts fake BLE beacons (advertising spoof)

### ✅ 6. *Sour Apple Attack*
- Specialized spoofing used to trick Apple devices into connecting or leaking info
- Exploits BLE advertisement weaknesses

---

## ⚙ How the 2.4GHz Jammer Works

### 📡 Technical Insight:

The *NRF24L01 module, though originally designed for short-range data transfer, can be **misused to flood the 2.4GHz spectrum* by sending random packets or bursts of data at high rates. Here's how it works:

1. *Channel Selection:*  
   The 2.4GHz ISM band (used by Wi-Fi, BLE, ZigBee) ranges from *2400 MHz to 2483.5 MHz, divided into **13 channels for Wi-Fi (in most regions)*.

2. *Noise Generation:*  
   The NRF24L01 can be programmed to transmit continuously on any of these channels. It sends *malformed packets or random bytes* repeatedly, overwhelming legitimate packets.

3. *Interference Behavior:*  
   This causes:
   - Wi-Fi packets to be corrupted or dropped
   - BLE advertisements to get lost
   - ZigBee communications to slow or fail
   - General 2.4GHz chaos in the area

4. *Multi-Module Parallel Jamming:*  
   Using 3 NRF24 modules allows the tool to *jam multiple channels simultaneously*, making it more effective and harder to counter.

5. *Detection Resistance:*  
   No real MAC is used during noise transmission. Makes it hard to trace and identify via standard sniffing tools.

---

## 📲 How to Use

1. *Power on the device*
2. *Menu appears on OLED*
3. Use *UP / DOWN / SELECT* buttons to choose:
   - Wi-Fi Scanner
   - Wi-Fi Jammer
   - 2.4GHz Full Jammer
   - BLE Scanner
   - BLE Spoofer
   - Sour Apple

4. *Select Target* (for Wi-Fi/BLE spoof attacks)
5. Status shows on OLED + LED (color-coded)

---

## 🔵 LED Status Indicators

| Color  | Status              |
|--------|---------------------|
| Green  | Idle / Ready        |
| Blue   | Scanning            |
| Red    | Jamming / Attack    |
| Yellow | Spoofing in progress|

---
## 📷 Screenshots 

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/SpectrumBreaker/blob/main/Image/IMG_0063.jpg)

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/SpectrumBreaker/blob/main/Image/IMG_0055.jpg)

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/SpectrumBreaker/blob/main/Image/IMG_0063.jpg)



