# Arduino-4-LED-blink-project.
Here’s how you can connect 4 LEDs to an Arduino and write code to blink them.
Components Needed:
Arduino board (e.g., Arduino Uno)
4 LEDs
4 resistors (220Ω)
Jumper wires
Breadboard
Connection Setup:
Place the 4 LEDs on the breadboard, aligning the anode (longer leg) of each LED to different digital pins on the Arduino.
Connect the cathode (shorter leg) of each LED to the ground (GND) through a 220Ω resistor.
The anodes of the LEDs will be connected to these Arduino pins:
LED 1 to pin 2
LED 2 to pin 3
LED 3 to pin 4
LED 4 to pin 5
Connect the GND pin of the Arduino to the GND rail of the breadboard.
Explanation:
The setup() function configures pins 2, 3, 4, and 5 as output to control the LEDs.
The loop() function contains two sequences:
Each LED is turned on and off one by one with a 500 ms delay.
All LEDs are turned on and off simultaneously with a 500 ms delay.
You can upload this code to your Arduino using the Arduino IDE, and the LEDs will blink according to the sequence described.
