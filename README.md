# UINIO-Logic-24MHz Logic Analyzer

[**UINIO-Logic-24MHz**](https://gitee.com/uinika/UINIO-Logic-24MHz) is a logic analyzer circuit design based on Infineon's (formerly Cypress) [**CY7C68013A**](https://www.infineon.com/cms/en/product/universal-serial-bus-usb-power-delivery-controller/peripheral-controllers/ez-usb-fx2lp/cy7c68013a-56ltxit/) `USB 2.0` controller and the [**sigrok**](https://sigrok.org/) open-source firmware. It provides a `24 MHz` sampling rate and **8** input channels.

![](./Images/PCB-3D-1.png)

## Design Overview

1. Uses a **USB Type-C** connector and a `10-pin` shrouded header.
2. The **CY7C68013A** USB controller uses a compact `QFN-56` package.
3. The **AT24C64** EEPROM from Microchip uses a compact `TSSOP-8` package.
4. Includes an onboard `24 MHz` passive SMD crystal; all SMD resistors and capacitors use the compact `0402` package.
5. Adds a **74HC245** eight-channel bus transceiver with **tri-state outputs** for more reliable signal acquisition.
6. The low-dropout regulator can use an **LDO** such as the `ME6211C33M5G` or `A6303AE5R-33A` in an `SOT-23-5` package.
7. Adds a set of TVS diodes for transient-voltage protection at the **USB Type-C** connector.

## Notes

- LED `D2` is connected to the **CY7C68013A** `PA0` pin, while `D3` is connected to `PA1`.
- Use the [sigrok-firmware-fx2lafw](https://github.com/wuxx/sigrok-firmware-fx2lafw) open-source firmware with the [PulseView](https://sigrok.org/wiki/Downloads) desktop application.

## Technical Documentation

[UinIO.com Electronics Technology Lab](http://uinio.com/) provides the following technical resources for the open-source **UINIO-Logic-24MHz** project:

- [UINIO-Logic-24MHz Core Board Schematic](http://uinio.com/my/works/UINIO-Logic-24MHz/UINIO-Logic-24MHz-Schematic.pdf)
- [Interactive BOM and PCB Layout Preview](http://uinio.com/archives/BOM/UINIO-Logic-24MHz.html)
- [UINIO-Logic-24MHz Logic Analyzer Quick Start Guide](http://uinio.com/Project/UINIO-Logic-24MHz/)
