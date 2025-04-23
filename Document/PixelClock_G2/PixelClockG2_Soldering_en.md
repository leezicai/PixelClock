# PixelClock
Soldering

## Table of Contents

### Information before Soldering
- Open windows
- Wear a mask 😷
- Soldering iron temperature
	- Medium temperature solder paste 240°C
	- Solder wire high temperature 300°C
	- Pressing nuts 300°C or 350°C

### Soldering and gluing the photoresistor component to the back cover
- Strip wires (strip one end of the wire)
- Wrap the wire around the photoresistor pin
- Apply solder paste, solder 2 wires to the photoresistor component
- Cut off part of the photoresistor component pin
- Apply a little 706 glue for protection

### Buttons
- Solder wire (medium or high temperature solder paste is also okay)
- 3 * 12mm high head buttons
	- Screw on the nuts (so they don't roll when soldering)
	- Only solder the 2 wires on the button side
- 1 * 16mm round illuminated flat button
	- ![16mm Button Image](../../Imags/PixelClockG2-16mm.jpg)
	- From this perspective, white-left, red-right, black-middle, yellow-bottom

### Pressing in Nuts
- Place the shell on the nut pressing stand
	- Stand
- Screw on the screws and copper nuts
	- ![Screw into Nut Image](../../Imags/螺丝拧入螺母.jpg)
	- Keep the longest end of the screw just inside the nut
- Soldering iron 350°C
- ![Pressing Nut Image](../../Imags/压入螺母.jpg)
- Fasten the PCB to the back cover, then successively press in the 4 nuts (5mm long M1.6 screw, 3mm high M1.6 nut)
- The two nuts for fixing the main board are done the same way (4mm long M1.6 screw, 2mm high M1.6 nut)

### Soldering ESP32C3 Pins
- Place the pins on the main board PCB
- Place the ESP32 C3 on the pins
- Solder with solder paste (or add flux first, then solder with solder)

### Soldering LEDs
- Medium temperature solder paste (or high temperature solder paste)
- Two methods
	- Manually apply solder paste to the LED board PCB
	- Stencil
- Place LEDs
	- The "1" in the upper left corner should align with the notch on the LED also in the upper left corner
	- ![LED Placement Direction](../../Imags/灯珠摆放位置.jpg)
- Place on the heating station
	- Remove when completely melted
- Test the LED board
	- Need to flash the firmware for testing LED beads
	- Use Dupont wires (male to female, 15CM length)
	- ![Testing LED - Dupont Wire Connection Method](../../Imags/测试灯珠-杜邦线接法.jpg)
	- Connect to ESP32-C3 GND, 5V, IO06
	- LED board GND, VCC, IN
- If LEDs don't light up
	- Check if the unlit LED and the LED before it have solder bridges or cold joints
- Connect the LED board and test again
	- Connect the LED board
	- Connect the LED board and ESP32-C3

### Main Board PCB
- 5.1k resistors
	- Add solder paste to the positions of the 2 SMD resistors
	- Place on the heating station (soldering iron can also be used)
- 10k resistor
	- Add solder paste to the position of the 1 SMD resistor
	- Solder with soldering iron
- Type-C connector
	- The notch on the connector faces outwards
	- Add a little flux
	- Just solder the pins
- Solder power connector
- Solder 3 button connectors
- Solder 1 photoresistor connector
- Solder two ESP32-C3 female headers
	- Start by inserting the female headers, add a little flux
	- Just solder
	- Solder the GND pin
- Passive Buzzer
	- The "+" (positive) sign is on the left
	- Solder to the PCB
- Microphone module
	- Insert diagonally into the female header
	- Solder the female header first
	- Then solder the pins on the microphone module
- Whether to buy the module from Taobao
	- Yes, Taobao clock module
		- Straighten the pins, insert into the main board and solder
	- No, make it yourself
		- Connect the clock link and the female header together
		- Insert into the main board and solder
- AMS1117 area
	- No soldering required