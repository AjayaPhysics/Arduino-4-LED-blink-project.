# Arduino-4-LED-blink-project.
# Arduino 4 LED Blink Project

## Overview
This project demonstrates how to control 4 LEDs with an Arduino to blink them in sequence and simultaneously. It is designed for beginners to learn multi-pin control and LED operations.

---

## Components
| **Component**        | **Quantity** | **Description**                           |
|-----------------------|--------------|-------------------------------------------|
| Arduino Uno           | 1            | Microcontroller board                     |
| LEDs                  | 4            | For blinking (any colour)                 |
| Resistors (220Ω)      | 4            | To limit the current through the LEDs     |
| Breadboard (optional) | 1            | For easier wiring                         |
| Jumper Wires          | Several      | For making connections                    |

---

## Connections
| **Arduino Pin**    | **Component**          | **Connection**                              |
|---------------------|------------------------|---------------------------------------------|
| Pin 2 (Digital)     | LED 1 anode (+)       | Through a 220Ω resistor to LED 1 anode     |
| Pin 3 (Digital)     | LED 2 anode (+)       | Through a 220Ω resistor to LED 2 anode     |
| Pin 4 (Digital)     | LED 3 anode (+)       | Through a 220Ω resistor to LED 3 anode     |
| Pin 5 (Digital)     | LED 4 anode (+)       | Through a 220Ω resistor to LED 4 anode     |
| GND                 | LED cathodes (-)      | All LED cathodes connected to GND          |

---

## Arduino Code

Below is the code to make the 4 LEDs blink sequentially and simultaneously:

```cpp
// Define LED pins
#define LED1 2
#define LED2 3
#define LED3 4
#define LED4 5

void setup() {
  // Set LED pins as output
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
}

void loop() {
  // Turn LEDs on and off sequentially
  digitalWrite(LED1, HIGH);
  delay(500);
  digitalWrite(LED1, LOW);
  
  digitalWrite(LED2, HIGH);
  delay(500);
  digitalWrite(LED2, LOW);
  
  digitalWrite(LED3, HIGH);
  delay(500);
  digitalWrite(LED3, LOW);
  
  digitalWrite(LED4, HIGH);
  delay(500);
  digitalWrite(LED4, LOW);

  // Turn all LEDs on and off simultaneously
  digitalWrite(LED1, HIGH);
  digitalWrite(LED2, HIGH);
  digitalWrite(LED3, HIGH);
  digitalWrite(LED4, HIGH);
  delay(500);
  
  digitalWrite(LED1, LOW);
  digitalWrite(LED2, LOW);
  digitalWrite(LED3, LOW);
  digitalWrite(LED4, LOW);
  delay(500);
}

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
