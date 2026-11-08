# ChenFU-CN13

广东石油化工学院 · 机械设计制造及其自动化 · 2027 届本科生

主攻嵌入式软件，兼学硬件设计。主要使用 C，围绕 STM32、ESP32 和 FreeRTOS 做项目。

这里记录项目实现、故障定位和实机验证。复刻项目会标明来源和个人修改，具体实现与验证范围见各仓库说明。

## 项目

| 项目 | 主要内容 | 验证记录 |
| --- | --- | --- |
| [双 MCU OTA 与环境监测终端](https://github.com/ChenFU-CN13/esp32-stm32-ab-ota) | STM32F407 + ESP32-S3；Bootloader、升级协议、外部 Flash 备份回滚、FreeRTOS 与 LVGL | 升级、CRC 拒收、ABORT 和断电恢复等实机记录 |
| [PowerPico 学习复刻](https://github.com/ChenFU-CN13/PowerPico_replica) | STM32F411；ADC/DMA 采样、自动量程、校准，以及 LVGL 页面生命周期问题修复 | 冷启动、采样显示、量程切换等功能的实机记录 |
| [Buck / LDO / Boost 电源学习板](https://github.com/ChenFU-CN13/buck-boost-ldo-power) | 原理图与 PCB 设计、手工焊接、双输入供电与电源转换 | 初版供电测试记录；修订版状态见项目说明 |
| [AC6965A 蓝牙音箱硬件复刻](https://github.com/ChenFU-CN13/AC6965-Bluetooth-Speaker) | 原理图分析、PCB 抄画、0402 焊接和上电调试 | 蓝牙配对、音乐播放及按键控制实测记录 |

OTA 项目采用内部 Bootloader + 单 APP 区 + W25Q128 外部单备份回滚方案。

## 常用技术与工具

| 方向 | 技术与工具 |
| --- | --- |
| 固件开发 | C、STM32、ESP32、STM32 HAL、ESP-IDF、FreeRTOS |
| 显示与通信 | LVGL、UART、I²C、SPI、Modbus RTU |
| 开发与调试 | Keil、STM32CubeMX、GNU Make、ST-Link、串口日志、逻辑分析仪 |
| 硬件学习 | 嘉立创EDA、原理图与 PCB、手工焊接、万用表、示波器 |

持续补齐外设驱动、任务同步和异常恢复方面的基础，把实现过程和调试依据写清楚。
