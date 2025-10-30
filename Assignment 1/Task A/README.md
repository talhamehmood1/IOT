wokwi link:
https://wokwi.com/projects/446221188689421313
 
 // documentation//

 ⚙️ Project Overview

The project controls three LEDs, an OLED display, and a buzzer using two push buttons.

The OLED shows the current mode of operation.

Each button changes the behavior of LEDs or resets the system.

There are 4 modes:

Both OFF

Alternate Blink

Both ON

PWM Fade (Brightness control using analogWrite)

🧩 Apparatus Used
Component	Quantity	Description
ESP32 DevKit V4	1	Microcontroller board
OLED Display (SSD1306, I2C)	1	128×64 pixel display
LED (Red)	1	LED1
LED (Purple)	1	LED2
LED (Green)	1	LED3 (PWM)
Push Button (Yellow)	1	Mode change button
Push Button (Black)	1	Reset button
Buzzer	1	For sound feedback
Resistors	3	(≈420Ω) for LED current limiting
Connecting Wires	—	For circuit connections
🔌 Pin Connections
Component	Pin No.	Function	Color / Type
LED1	GPIO 2	Output	🔴 Red
LED2	GPIO 4	Output	🟣 Purple
LED3 (PWM)	GPIO 5	PWM Output	🟢 Green
Button 1 (Mode)	GPIO 26	Input (Mode change)	🟡 Yellow Button
Button 2 (Reset)	GPIO 27	Input (Reset system)	⚫ Black Button
Buzzer	GPIO 15	Output (Tone)	🔊 Buzzer
OLED SDA	GPIO 21	I2C Data	
OLED SCL	GPIO 22	I2C Clock	
OLED VCC	3.3V	Power	
OLED GND	GND	Ground	
🔄 Working Summary

On startup → shows “Initializing…” animation and beeps.

Mode Button (Yellow):

Cycles through 4 modes.

Each mode changes LED behavior and updates OLED text.

Reset Button (Black):

Turns all LEDs OFF, shows “Reset to OFF” on OLED, and plays a low beep.

Buzzer: gives short tones as feedback when changing modes.