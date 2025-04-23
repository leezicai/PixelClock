# PixelClock
Writing Firmware

## Table of Contents

### Install Drivers on Computer
- Windows 10/11 (Win7 not supported, Win10+)
	- Driver Address
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Gitee Download Address (in Driver folder)
		- https://gitee.com/leezicai/PixelClock
	- Github Download Address (in Driver folder)
		- https://github.com/leezicai/PixelClock
- Mac(macOS 14.7)
	- Driver Address
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Gitee Download Address (in Driver folder)
		- https://gitee.com/leezicai/PixelClock
	- Github Download Address (in Driver folder)
		- https://github.com/leezicai/PixelClock

### Download Firmware
- TestPixel_IO06_1024.bin
- PixelClock_Pix25_16_8_2_LR.bin
- https://github.com/leezicai/PixelClock_Firmware

### Firmware Writing Method (Web)
- Access Address
	- https://espressif.github.io/esp-launchpad/
- Steps to flash firmware
	- Click Quick Start
		- Select ESP32-C3
	- Connect ESP32-C3 using a Type-C cable (no need to solder headers here, will solder next time)
	- Click Connect on the webpage
		- It will keep flashing here
		- First long press Boot button
		- Then long press RST button
		- Release RST button
		- Release Boot button
		- It will stop flashing now
		- Select Device Click OK
	- If device is not seen
		- Check if ESP32-C3 is occupied by Arduino, if occupied, temporarily exit Arduino
	- Click DIY
		- Flash Address fill in: 0x0
		- choose File select the downloaded file: TestPixel_1024_I006.bin
		- Finally click: Program, wait for writing to complete
	- Click ESP32-C3 Restart
		- Press the RST button

### PixelClock-Pix25_16_8_2_LR_1.4.1.bin
- Pix25
	- Represents the main control board model
- 16_8_2
	- Represents 16 LEDs long, 8 LEDs high, total 2 boards
- LR
	- Represents the LED arrangement is from left to right

### TestPixel_IO06_1024.bin
- TestPixel
	- Represents testing LEDs (pixels)
- IO06
	- Represents the signal wire is connected to GPIO06
- 1024
	- Represents the maximum number of LEDs that can be tested (1024)