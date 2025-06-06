> **this project is a work in progress, more updates will be posted here as time goes on, 3d models and code will be posted on project completion**

**My take on a smartwatch, built because i don't like the apple watch**

![Render](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/render.jpg)
## Features

- **Dynamic App System** - Runtime app switching with automatic memory management
- **Power Optimization** - Three sleep modes with wake interrupts
- **Hardware Acceleration** - DMA display rendering
- **Professional UI** - LVGL integration with smooth animations
- **Error Recovery** - Robust exception handling with diagnostic display
- **Wifi/Bluetooth connectivity** - Supporting Wifi 4, Bluetooth 5 and most derivatives

## Hardware

![Real photos](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/photos.jpg)
current version is v6, these are some of the previous iterations

## Current specs:

| Component          | Model       | Interface | Purpose          |
| ------------------ | ----------- | --------- | ---------------- |
| MCU                | ESP32       | -         | 240MHz dual-core |
| Display            | 240×240 TFT | SPI + DMA | Main interface   |
| Touch              | CST816S     | I2C       | User input       |
| Accelerometer      | BMA400      | I2C       | Motion detection |
| RTC                | DS3231      | I2C       | Timekeeping      |
| Battery management | TBD         | TBD       |                  |

## Firmware overview (beta)

![Os architecture1](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/os1.jpeg)
![Os architecture2](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/os2.jpeg)

## Roadmap

![Oled pic](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/oled.jpg)
A new version is being developed, with much improved electronics and a new much bigger edge to edge (and brighter) OLED display

- [x] Apps
- [x] Sleep modes
- [x] DMA
- [ ] Oled Screen
- [ ] Bluetooth LE Notifications
- [ ] OTA updates
- [ ] File system (SPIFFS/LittleFS)
- [ ] Health monitoring sensors

## License

GPL 3.0 - See [LICENSE](https://github.com/angelogerminario/Potato-watch/blob/main/LICENSE) for details.