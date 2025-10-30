wokwi link:
https://wokwi.com/projects/446222210776588289

//Documentation//

⚙️ Project Overview

This project detects short and long button presses using an ESP32.

A short press toggles the LED ON/OFF.

A long press (more than 1.5 seconds) activates the buzzer.

The OLED display shows the button press status (short or long press).

🧩 Apparatus Used
Component	Quantity	Description
ESP32 DevKit V4	1	Microcontroller board
OLED Display (SSD1306, I2C)	1	128×64 pixel display
LED (Magenta)	1	Indicates short press
Push Button (Grey)	1	Used for press detection
Buzzer	1	Beeps on long press
Resistor	1	(≈420Ω) for LED current limiting
Jumper Wires	—	For circuit connections
🔌 Pin Connections
Component	Pin No.	Function	Color / Type
Button	GPIO 25	Input	⚪ Grey Button
LED	GPIO 5	Output	💜 Magenta LED
Buzzer	GPIO 18	Output (Tone)	🔊 Buzzer
OLED SDA	GPIO 21	I2C Data	
OLED SCL	GPIO 22	I2C Clock	
OLED VCC	3.3V	Power	
OLED GND	GND	Ground	
🔄 Working Summary

At startup → OLED shows “Ready…”.

When the button is pressed, the ESP32 records the press time.

When the button is released, it measures the press duration:

Short Press (<1.5 sec):

LED toggles ON/OFF.

OLED shows “Short Press → LED Toggle”.

Long Press (>1.5 sec):

Buzzer turns ON briefly.

OLED shows “Long Press → Buzzer”.

The OLED continuously updates to reflect the latest action.