# PixelClock像素时钟  
  写入固件

## 目录

### 电脑安装驱动
- Windows 10/11 (Win7 不支持, Win10+)
	- 驱动地址
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Gitee下载地址(Driver文件夹下)
		- https://gitee.com/leezicai/PixelClock
	- Github下载地址(Driver文件夹下)
		- https://github.com/leezicai/PixelClock
- Mac(macOS 14.7)
	- 驱动地址
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Gitee下载地址(Driver文件夹下)
		- https://gitee.com/leezicai/PixelClock
	- Github下载地址(Driver文件夹下)
		- https://github.com/leezicai/PixelClock

### 下载固件
- TestPixel_IO06_1024.bin
- PixelClock_Pix25_16_8_2_LR.bin
- https://github.com/leezicai/PixelClock_Firmware

### 写入固件方式 (Web)
- 访问地址
	- https://espressif.github.io/esp-launchpad/
- 刷入固件步骤
	- 点击Quick Start
		- 选择ESP32-C3
	- 使用Type-C线连接ESP32-C3（这里无需焊接排针，下期会焊接）
	- 点击网页上 Connect
		- 这里会一直闪
		- 先长按Boot键
		- 再长按RST键
		- 松开RST键
		- 松开Boot键
		- 这样就不闪了
		- 选择 设备 点击确定
	- 如果未看到设备
		- 检查ESP32-C3没有被Arduino占用, 占用就暂时退出Arduino
	- 点击DIY
		- Flash Address填写:  0x0
		- choose File选择下载的文件: TestPixel_1024_I006.bin 
		- 最后点击: Program, 等待写入完成
	- 点击ESP32-C3重启
		- 按下RST按钮

### PixelClock-Pix25_16_8_2_LR_1.4.1.bin
- Pix25
	- 代表主控制板型号
- 16_8_2
	- 代表长16灯珠 高8灯珠 共2块
- LR
	- 代表灯珠排列方式是从左到右

### TestPixel_IO06_1024.bin
- TestPixel
	- 代表测试灯珠(像素)
- IO06
	- 代表信号线接GPIO06
- 1024
	- 代表最多能测试1024个灯珠
