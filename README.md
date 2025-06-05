# Potato Watch

![ESP32](https://img.shields.io/badge/ESP32-000000?style=flat&logo=espressif&logoColor=white) ![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white) ![LVGL](https://img.shields.io/badge/LVGL-8.2.0-blue) ![License](https://img.shields.io/badge/License-GPL3.0-green)

**My take on a smartwatch, built because i don't like the apple watch**

FULL CODE COMING SOON

![Render](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/render.jpg)
## Features

- **Dynamic App System** - Runtime app switching with automatic memory management
- **Power Optimization** - Three sleep modes with wake interrupts
- **Hardware Acceleration** - DMA display rendering
- **Professional UI** - LVGL integration with smooth animations
- **Error Recovery** - Robust exception handling with diagnostic display
## Hardware

![Real photos](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/photos.png)

| Component          | Model       | Interface | Purpose          |
| ------------------ | ----------- | --------- | ---------------- |
| MCU                | ESP32       | -         | 240MHz dual-core |
| Display            | 240×240 TFT | SPI + DMA | Main interface   |
| Touch              | CST816S     | I2C       | User input       |
| Accelerometer      | BMA400      | I2C       | Motion detection |
| RTC                | DS3231      | I2C       | Timekeeping      |
| Battery management | TBD         | TBD       |                  |

## Architecture

![Os architecture1](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/os1.jpeg)
![Os architecture2](https://raw.githubusercontent.com/angelogerminario/potato-watch/refs/heads/main/images/os2.jpeg)
## Code Structure Examples

```cpp
// Dynamic app management
void runNewApp(std::string name) {
    delete runningApp;
    runningApp = new HomeScreen();
    runningApp->initUI();
}

// Global system state
struct Data {
    std::string runAppString;
    int sleep;                // NO_SLEEP, LIGHT_SLEEP, DEEP_SLEEP
    RTC_DS3231 rtc;
    BMA400 bma;
};
```

## Roadmap

- [ ] Oled Screen
- [ ] Bluetooth LE Notifications
- [ ] OTA updates
- [ ] File system (SPIFFS/LittleFS)
- [ ] Health monitoring sensors

## License

GPL 3.0 - See [LICENSE](https://claude.ai/chat/LICENSE) for details.