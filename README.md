# USB to UART TTL Converter (FT232RL)

When I started designing my own custom ESP32 and STM32 boards, I quickly realized one thing:
no project moves forward without a reliable way to program and debug.

I had a few cheap USB-to-UART adapters lying around, but they often gave me unstable connections, messy wiring, or missing signals. So, instead of relying on them, I decided to design my own converter board — something compact, robust, and dependable for daily use.

This board is built around the FT232RL chip and has since become one of the most useful tools on my bench.

---

## 📷 Hardware Preview
<p align="center">
  <img src="Assets\photo_2025-09-28_22-46-26.jpg" width="620"/>
</p>

---

## ✨ Features
- ✅ Based on **FTDI FT232RL** USB-to-Serial IC  
- ✅ Standard **USB Micro-B connector** for host connection  
- ✅ Breakout pins for **TX, RX, VCC (5V/3.3V), GND, RTS, DTR**  
- ✅ Onboard power regulation & filtering capacitors for signal stability  
- ✅ Compact and easy-to-use design for prototyping and programming custom boards  
- ✅ Works with **Windows, Linux, and macOS** (drivers available from FTDI)  

---

## 🔌 Pinout
The breakout exposes the following signals:

| Pin  | Function                        |
|------|---------------------------------|
| VCC  | 3.3V / 5V Output (configurable) |
| GND  | Ground                          |
| TXD  | UART Transmit                   |
| RXD  | UART Receive                    |
| RTS  | Request To Send                 |
| DTR  | Data Terminal Ready             |

---

## 🛠️ Getting Started
1. **Connect the board** to your PC using a USB cable (Micro-USB).  
2. **Install FTDI drivers** (if required):
   - [FTDI Drivers Download](https://ftdichip.com/drivers/)  
3. **Connect TX, RX, GND** to your target board (cross TX↔RX).  
4. (Optional) Use **RTS/DTR** for auto-reset and bootloader functions with ESP32/ESP8266.  
5. Open a serial monitor (e.g., Arduino IDE, PuTTY, or PlatformIO) and communicate with your target board.  

---

## ⚡ Applications
- Programming ESP32/STM32/AVR custom boards  
- Debugging UART logs from embedded systems  
- General USB-to-TTL serial communication  

---
## Behind the Build

I built this board because I wanted a reliable programmer and debug tool for my custom ESP32/STM32 designs. Many cheap adapters had poor soldering or unstable connectors, so I decided to make one myself.

- Fabrication Experience:
The fine-pitch pads of the FT232RL were a challenge, but PCBWay’s tight tolerance and smooth ENIG finish made soldering much easier, even by hand. The black solder mask also gave it a professional look, even though it’s just a small utility board.

- Service Choices:
2-layer board.
ENIG surface finish for solderability.


---

## 🎉 Special Thanks to PCBWay


<p align="center">
  <a href="https://www.pcbway.com/" target="_blank">
    <img src="https://github.com/AvishkaVishwa/12V-DC-Motor-Speed-Controller-PCB-Design-using-KiCAD/blob/0191b6e02eeb30e176867d2a93ebec854536829a/Images/pcbwaylogo.jpg" alt="PCBWay" width="200"/>
  </a>

</p>

I would like to give a huge shoutout and sincere thanks to **[PCBWay](https://www.pcbway.com/)** for sponsoring the PCB fabrication of this project!
 
With the **fine-pitch FT232RL IC**, pad accuracy and **ENIG finish** were crucial for easy soldering  and PCBWay’s work exceeded expectations.  
I the finish quality gave it a professional look far beyond a typical DIY tool.

This project wouldn’t have been possible without their generous support. If you’re looking to manufacture professional-grade PCBs at an affordable price, I highly recommend checking them out.