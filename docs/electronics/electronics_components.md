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

## What is difference between Linear Regulator vs Buck Converter?
**Linear Regulator** drops voltage by burning the excess as heat. Like LM7805, AMS1117 etc. Easy to use (input, output, and 2 capacitors). Cheap and widely available. Output is clean (low electrical noise) good for sensitive analog circuits.
**Buck Converters** switches input with an inductor & capacitor to step down voltage. Efficiency 80 - 95%. Great for Battery Powered systems.Like LM2596, MP1584, XL4015 etc. Output has more ripple/noise than linear regulators.

## Linear Regulator vs Low Drop Out (LDO) Regulator
Low Drop Out (LDO) Regulator is type of Linear Regulator designed to work with a much smaller voltage difference between Voltage In and Voltage Out. Like RT9080, MIC5205
| Feature | Linear Regulator | Low Drop Out Regulator |
| --- | --- | --- |
| Dropout Voltage | 1 - 2 V | < 0.3V |
| Quiescent Current | mA | uA |
| Use Case | Main powered | Battery Powered |

> Quiescent Current is the current consumed by IC when it is enabled but there is no load, and the device is not switching.

## What is ESD Protection?
ESD Stands for Electro Static Discharge. Sudden spark of static electricity. We dont feel much damage, but microchips can be destroyed instantly. Place a part like LESD5D5.0CT1G or SMF5.0A across VBUS-to-GND. Additonally use it for D+, D-.

## What is Diode?
Diode is one way valve. ex - 1N5819HW 

## Power Conversion 5v / 3.3v

### Buck Converter

- AMS1117 3.3 / 5 LDO (Low Drop Out). It is good to to drop few volts by Advanced Monolithic Systems.AMS1117 is a lower cost clone of LM1117 of Texas Instruments. 800mA power output
- LM1117 is Low Drop Out Linear Regulator by Texas Instruments
- LM2596 Buck Converter Adjustable by Texas Instruments. It can drop more than 5 volts. also available in Fixed 3.3V, 5V & 12V.
- MP1584 Buck Converter Adjustable
- MP2307 Buck Converter (MINI-360) is modern version of LM2596 buck convertor.
> MP Series IC are made by Monolithic Power System (MPS) based in US.
- XL4005 Buck Converter Adjustable (For Heavy Loads. More than 2 Ampere)

### Boost Converter
- XL6009 
> XL Series ICs, buck or boost converters are by XLSemi ( Chinese Company).

### Advanced
- RT9080 Series LDO IC made by Richtek Technology Corportation is a Taiwan based company. 600 mA Power Output.
- AP2112 Series LDO IC made by Diodes Incorporated is a US Company.
- XC6222 series LDO IC made by Torex Semiconductor Ltd is a Japanese company.

## What is the use of enable pin in LDO IC?
The enable (EN) pin on a low-dropout voltage regulator (LDO) acts as an ON/OFF switch to control the regulator's output. It allows a microcontroller or other logic circuit to shut down the LDO to save power or to enable it for a specific application. 

## Connector
- JST Connector 2 Pin for Lipo Battery. JST Stands for Japan Solderless Terminal. JST-PH (2mm), JST-XH (2.54 mm), JST-SH (1mm).

- Screw Terminal (Block Terminal Connector). KF128 (5.08mm pitch), KF301 (5.08mm). Mainly used in AC Current.

## Tips & Tricks
- Cirkit Designer studio for bread board
- Monochrome lcd for ruggedness 2.4 inch
- Use internal pullup resistor to avoid adding resistor to button




