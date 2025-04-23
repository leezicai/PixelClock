# PixelClock 像素時鐘
寫入韌體

## 目錄

### 電腦安裝驅動程式
- Windows 10/11 (Win7 不支援, Win10+)
	- 驅動程式地址
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Gitee下載地址 (Driver資料夾下)
		- https://gitee.com/leezicai/PixelClock
	- Github下載地址 (Driver資料夾下)
		- https://github.com/leezicai/PixelClock
- Mac(macOS 14.7)
	- 驅動程式地址
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Gitee下載地址 (Driver資料夾下)
		- https://gitee.com/leezicai/PixelClock
	- Github下載地址 (Driver資料夾下)
		- https://github.com/leezicai/PixelClock

### 下載韌體
- TestPixel_IO06_1024.bin
- PixelClock_Pix25_16_8_2_LR.bin
- https://github.com/leezicai/PixelClock_Firmware

### 寫入韌體方式 (Web)
- 訪問地址
	- https://espressif.github.io/esp-launchpad/
- 刷入韌體步驟
	- 點擊 Quick Start
		- 選擇 ESP32-C3
	- 使用 Type-C 線連接 ESP32-C3 (這裡無需焊接排針，下期會焊接)
	- 點擊網頁上 Connect
		- 這裡會一直閃爍
		- 先長按 Boot 鍵
		- 再長按 RST 鍵
		- 松開 RST 鍵
		- 松開 Boot 鍵
		- 這樣就不閃了
		- 選擇 裝置 點擊 確定
	- 如果未看到裝置
		- 檢查 ESP32-C3 沒有被 Arduino 佔用，如果佔用就暫時退出 Arduino
	- 點擊 DIY
		- Flash Address 填寫: 0x0
		- choose File 選擇下載的檔案: TestPixel_1024_I006.bin
		- 最後點擊: Program, 等待寫入完成
	- 點擊 ESP32-C3 重啟
		- 按下 RST 按鈕

### PixelClock-Pix25_16_8_2_LR_1.4.1.bin
- Pix25
	- 代表主控制板型號
- 16_8_2
	- 代表長16燈珠 高8燈珠 共2塊
- LR
	- 代表燈珠排列方式是從左到右

### TestPixel_IO06_1024.bin
- TestPixel
	- 代表測試燈珠 (像素)
- IO06
	- 代表信號線接 GPIO06
- 1024
	- 代表最多能測試1024個燈珠