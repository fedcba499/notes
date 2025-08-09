## Which company make custom boards? 
- Sparkfun 
- Adafruit
- Smartelex ( copy of sparkfun robu.in)
- 7semi ( copy of sparkfun evelta.com)
- Waveshare
- Dfrobot
- Elecrow
- Seeed Studio

## What is difference between Arduino Boards and ESP32 Boards?
- Esp 32 - 32 bit processor (good for projects which requires high computation power, power management issues)
- Arduino - 8 bit processor (good for small projects, quick power settings with 9v battery, low computation power)

## Why use Prototype Board / Pref Board than making Custom PCB?
For our use case, where modifications

Cirkit Designer studio for bread board

Integrated Circuit Programming (IC Programming)
I²S (Inter-IC Sound) - PWM - Pulse Width Modulation sound transfer 

Monochrome lcd for ruggedness 2.4 inch

Mircro Controllers
Instead of purchasing entire board use 
esp32 S3 Chip - Built in Wifi and bluetooth
AT Mega 328 Chip - more popular, easy to program
STM32 - powerful and andvanced (Arm Cortex Chips)
AT Tiny 85

Castellated edges half circle on edge

ESP32 Cam Module has inbuilt SD Card reader
( Thus removing complexity of 6 Wire)
TP 4056 power supply module to provide stable 5v power supply to esp32-cam module.

switch on +ve wire from 4056 to esp32 cam

(Serial Peripheral Interface) SPI Communication protocal for communication with sd card

The U2RXD pin on the ESP32 refers to UART2 Receive Data (RX), which is a pin designated for receiving data via the UART (Universal Asynchronous Receiver-Transmitter) protocol

Use internal pullup resistor to avoid adding resistor to button

TP4056 - designed for charging lipo battery ( not for providing constant power supply to ESP32 Cam)
TP5100 - designed to provide constant 5 v supply ( which is ideal for esp32 cam like devices, which needs constant 5 v supply)

Esp32 c3 mini
Esp32 c6 mini
Esp32 s3 mini

DC DC step up converter ( Boost Converter)
MT3608 ( 2 Amphere )
XL6009E1 ( 3 Amphere )

MHCD 42 - (Charging + 5V boost)
0.96 inch oled display ( size - 128 x 64 Pixels)
based on SSD 1306

Wire library in Arduino IDE is used for communication with I2C ( Inter Integrated Circuit) like OLED Display, Sensors, EEPROM.

Bitmap Image

OLED Display Pin
3.3 V input
Gnd
SDA ( Serial Data ) Line  is used for  transfering data between  master and slave device. It is bi directional. 
SCL ( Serial Clock ) Line is used to synchronise the data transfer between the master & slave device. Direction controlled by Master Device which generates the clock pulses to co-ordinate the timing of data transmission.

Using PROGMEM to store bitmap images in flash memory instead of ram, thus saving ram for cruicial processing tasks

fs.h - to handle file system and read, write to sd card
spi.h - serial pheripheral interface protocol to interact with multiple serial monitor using master esp32 with all sensors like gps, touch etc.

Hardware Serial
Hardware serial uses the built-in UART (Universal Asynchronous Receiver-Transmitter) module(s) of the microcontroller. These are hardware peripherals dedicated to handling serial communication.  Use HardwareSerial when possible for better performance and reliability.

Software Serial
Software serial uses bit-banging to emulate serial communication in software on any GPIO pins of the microcontroller. When you need to communicate with multiple serial devices and the hardware UARTs are occupied.

Remove SD Card while uploading code to esp32 cam

in C, C++ Variable ends with semicolon

