## Which company make custom boards? 
- Sparkfun 
- Adafruit
- Smartelex ( copy of sparkfun robu.in)
- 7semi ( copy of sparkfun evelta.com)
- Waveshare
- Dfrobot
- Elecrow
- Seeed Studio

## Websites to Buy Electronics Components
- robu.in
- rees52
- techiesms.com
- robokit.com
- sharvielectronics.com
- lioncircuits.com
- tanotis.com
- techdelivers.com




## What is difference between Arduino Boards and ESP32 Boards?
- Esp 32 - 32 bit processor (good for projects which requires high computation power, power management issues)
- Arduino - 8 bit processor (good for small projects, quick power settings with 9v battery, low computation power)

## Why use Prototype Board / Pref Board than making Custom PCB?
For our use case, where modifications are very frequent, and less time for development, designing and printing costs money and 7 - 10 days of time. Better use prototype board with AWG22 wire for soldering connections.

## What is AWG22?
AWG stands for American Wire Guage. For general purpose connection AWG22 is good, for heavier power supply like servo motors etc thicker wire AWG20 or AWG18 or AWG16. As number decreses thickness increses.

## List of widely uses Micro Controllers
- ESP32 S3 Chip - Built in Wifi and bluetooth
- AT Mega 328 Chip - more popular, easy to program
- STM32 - powerful and andvanced (Arm Cortex Chips)
- AT Tiny 85

## Castellated Edges
Catellated Edges are plated through holes on a PCB which are cut in half. Typically, these are applied to the outer edges of a board, and are used to solder one board on top of another.

## What is Serial Monitor?
Serial Monitor can be used as a debugging tool, testing out concepts or to communicate directly with the Arduino board.
> Using print tool to test where does code getting stuck.

## What is difference between Harware Serial vs Software Serial?
Hardware serial uses the built-in UART (Universal Asynchronous Receiver-Transmitter) module(s) of the microcontroller. These are hardware peripherals dedicated to handling serial communication.  Use HardwareSerial when possible for better performance and reliability.

Software serial uses bit-banging to emulate serial communication in software on any GPIO pins of the microcontroller. When you need to communicate with multiple serial devices and the hardware UARTs are occupied.

## Major Electronics Components
| Module | Functionlity |
| --- | --- |
| TP4056 | designed for charging lipo battery ( not for providing constant power supply to ESP32 Cam) |
| TP5100 | designed to provide constant 5 v supply ( which is ideal for esp32 cam like devices, which needs constant 5 v supply) |
| MT3608 | 2 Amphere DC DC step up converter ( Boost Converter) |
| XL6009E1 | 3 Amphere DC DC step up converter ( Boost Converter) |
| MHCD 42 | Charging + 5V boost |
| 0.96 inch oled display | size - 128 x 64 Pixels based on SSD 1306 |

## OLED Display Pin
3.3 V input, Gnd

**SDA (Serial Data)** Line  is used for  transfering data between  master and slave device. It is bi directional. 

**SCL (Serial Clock)** Line is used to synchronise the data transfer between the master & slave device. Direction controlled by Master Device which generates the clock pulses to co-ordinate the timing of data transmission.

## Tips & Tricks
- Cirkit Designer studio for bread board
- Monochrome lcd for ruggedness 2.4 inch
- Use internal pullup resistor to avoid adding resistor to button


