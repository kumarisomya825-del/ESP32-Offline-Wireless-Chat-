ESP32 Offline Wireless Chat

An offline wireless communication project using two ESP32 development boards and nRF24L01 radio modules. The goal is to send messages wirelessly without using the internet.

Project Overview

This project explores wireless communication between two ESP32 boards using nRF24L01 transceiver modules. One ESP32 acts as a transmitter, while the other acts as a receiver.

The project is being developed and tested using Arduino IDE and the RF24 library.

Objectives

- Establish wireless communication between two ESP32 boards.
- Send messages from one ESP32 to another.
- Work without an internet connection.
- Build a low-cost embedded systems communication prototype.
- Explore future phone-based messaging integration.

Components Required

- 2 × ESP32 DevKit boards
- 2 × nRF24L01 PA/LNA radio modules with antennas
- 2 × 47 µF electrolytic capacitors
- Breadboards
- Jumper wires
- USB cables
- Suitable regulated 3.3V power supplies for the radio modules, if required

Software and Libraries

- Arduino IDE
- ESP32 board support package
- RF24 library by TMRh20

Pin Connections

The following pin mapping is used for each ESP32:

nRF24L01 Pin| ESP32 Pin
CE| GPIO 4
CSN| GPIO 5
SCK| GPIO 18
MOSI| GPIO 23
MISO| GPIO 19
VCC| Regulated 3.3V
GND| GND
IRQ| Not connected

Capacitor Connection

Connect a 47 µF capacitor across the nRF24L01 power pins:

- Positive (+) leg to VCC (3.3V)
- Negative (−) leg to GND

Important: Never connect the nRF24L01 VCC pin directly to 5V. PA/LNA modules can require more current than an ESP32 board's 3.3V output can reliably provide. Use a suitable regulated 3.3V supply and a common ground.

How It Works

1. The transmitter ESP32 sends a test message using its nRF24L01 module.
2. The receiver ESP32 listens for messages using its nRF24L01 module.
3. Both modules use the same radio channel, data rate, and address.
4. The receiver prints received messages in the Arduino IDE Serial Monitor.

Setup Instructions

1. Install Arduino IDE.
2. Install ESP32 board support.
3. Install the RF24 library by TMRh20 through Library Manager.
4. Connect the first nRF24L01 module to the transmitter ESP32.
5. Upload "transmitter.ino" to the first ESP32.
6. Connect the second nRF24L01 module to the receiver ESP32.
7. Upload "receiver.ino" to the second ESP32.
8. Open the Serial Monitor at 115200 baud to inspect the output.

Testing Status

Current status: In Progress

The transmitter and receiver sketches have been uploaded to the ESP32 boards. During testing, the Serial Monitor displayed "Radio not detected!".

Wireless communication has not yet been verified. The radio wiring, SPI connections, and regulated 3.3V power supply still need to be checked.

Future Improvements

- Resolve radio detection and power supply issues.
- Verify two-way wireless communication.
- Develop a phone-based chat interface.
- Add message acknowledgements and connection status.
- Improve the enclosure and portability of the prototype.

Learning Outcomes

This project provides practical experience with ESP32 GPIO/SPI connections, wireless transceivers, Arduino programming, embedded debugging, and GitHub-based project documentation.

