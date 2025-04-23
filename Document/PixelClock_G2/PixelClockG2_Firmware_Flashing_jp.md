# PixelClock ピクセルクロック
ファームウェアの書き込み

## 目次

### コンピュータにドライバをインストールする
- Windows 10/11 (Win7 非対応, Win10+)
	- ドライバのアドレス
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Giteeダウンロードアドレス (Driverフォルダ内)
		- https://gitee.com/leezicai/PixelClock
	- Githubダウンロードアドレス (Driverフォルダ内)
		- https://github.com/leezicai/PixelClock
- Mac(macOS 14.7)
	- ドライバのアドレス
		- https://www.wch.cn/downloads/category/67.html?feature=USB%E8%BD%AC%E4%B8%B2%E5%8F%A3&product_name=CH347
	- Giteeダウンロードアドレス (Driverフォルダ内)
		- https://gitee.com/leezicai/PixelClock
	- Githubダウンロードアドレス (Driverフォルダ内)
		- https://github.com/leezicai/PixelClock

### ファームウェアのダウンロード
- TestPixel_IO06_1024.bin
- PixelClock_Pix25_16_8_2_LR.bin
- https://github.com/leezicai/PixelClock_Firmware

### ファームウェア書き込み方法 (Web)
- アクセスアドレス
	- https://espressif.github.io/esp-launchpad/
- ファームウェア書き込み手順
	- Quick Start をクリック
		- ESP32-C3 を選択
	- Type-Cケーブルを使用してESP32-C3を接続します (ここではピンヘッダのハンダ付けは不要です、次回ハンダ付けします)
	- Webページ上の Connect をクリック
		- ここで点滅し続けます
		- まず Boot ボタンを長押し
		- 次に RST ボタンを長押し
		- RST ボタンを離す
		- Boot ボタンを離す
		- これで点滅しなくなります
		- デバイスを選択して OK をクリック
	- デバイスが表示されない場合
		- ESP32-C3がArduinoによって使用されていないか確認してください、使用されている場合は一時的にArduinoを終了してください
	- DIY をクリック
		- Flash Address に 0x0 を入力
		- choose File でダウンロードしたファイルを選択: TestPixel_1024_I006.bin
		- 最後に Program をクリックし、書き込み完了を待つ
	- ESP32-C3の再起動をクリック
		- RST ボタンを押す

### PixelClock-Pix25_16_8_2_LR_1.4.1.bin
- Pix25
	- メインコントロールボードのモデルを表す
- 16_8_2
	- 長さ16個のLED、高さ8個のLED、合計2枚を表す
- LR
	- LEDの配列が左から右へであることを表す

### TestPixel_IO06_1024.bin
- TestPixel
	- LED(ピクセル)のテストを表す
- IO06
	- 信号線がGPIO06に接続されていることを表す
- 1024
	- テスト可能な最大LED数(1024個)を表す