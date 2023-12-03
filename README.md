# Songguo PTS200 

PTS-200 soldering iron firmware, forked from Eddddddddy/Songguo-PTS200. With some bugfixes and customization.

- Bugfix: https://github.com/Eddddddddy/Songguo-PTS200/issues/19
- Bugfix: https://github.com/Eddddddddy/Songguo-PTS200/issues/13
- Always show measured temp, even at startup. Never show "000" as temp, which can be dangerous
- I modified the large fonts on the two main screens, as I didn't like the original ones
- Totally modified the "Big number" screen: Set temp in the top-left, input voltage in the top-right, status is shown by different icons
- Adjusted temp calculation. Now it is much closer to the measured real temp, with TS-100 tips
- Adjusting temp on the main screen is temporary. It won't save as Default temp


## Introduction
1. PD3.0 and QC3 fast charge protocol

2. 20V 5A 100W maximum power
<!-- 内置IMU，用于休眠检测 -->
3. Built-in IMU for sleep detection
<!-- PD协议芯片使用CH224K -->
4. PD protocol chip uses CH224K
<!-- MOSFET支持30V 12A -->
5. MOSFET supports 30V 12A
<!-- MCU使用ESP32 S2 FH4 -->
6. MCU uses ESP32 S2 FH4
<!-- 电源输入使用功率加强的USB-C接口 -->
7. The power input uses a power-enhanced USB-C interface
<!-- 定制的4欧姆内阻的烙铁头 -->
8. Customized soldering tip with 4 ohm internal resistance. It can be powered by 20V with 100W.
<!-- 128x64 OLED screen -->
9. 128x64 OLED screen
<!-- 3个按键，中间的按键与GPIO0相连 -->
10. 3 buttons, the middle button is connected to GPIO0
<!-- MSC 模式的固件升级，闪存盘模式 -->
11. MSC firmware upgrade, flash disk mode
<!-- 带有便携式的尖端保护盖 -->
12. With a portable tip cap

<!-- 构建方法 -->
## Build method
<!-- Arduino with ESP32 环境 -->
1. Arduino with ESP32 environment
<!-- 安装依赖库 -->
2. Install dependent libraries: Button2, U8g2, QC3Control, ESP32AnalogRead, PID_v1, SparkFun_LIS2DH12
<!-- 从U8G2库中替换u8g2_fonts.c文件 -->
3. Replace the u8g2_fonts.c file from the U8G2 library
<!-- 在Arduino 中选择Tools- USB CDC On Boot- Enable -->
4. In Arduino, select Tools-USB CDC On Boot-Enable
<!-- 在Arduino 中选择Tools-Upload Mode- Internal USB -->
5. In Arduino, select Tools-Upload Mode-Internal USB
<!-- 点击上传 -->
6. Click Upload