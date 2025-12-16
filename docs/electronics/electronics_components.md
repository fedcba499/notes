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

## Linear Voltage Regulator 

### 1 Gen (1995 - 2000) : Bi-Polar Technology

LM1117 Famliy, LM317, LM2596, 78xx Series. In 1995 Texas Instruments released LM1117 IC. With General Characteristics as under
- Low Dropout Regulator
- 800 mA Output Current
- 1.2 V Dropout Voltage
- Input Voltage upto 15 V
- Quienscent current (Iq) : 5mA / 5000uA
- Dropout Voltage : 1.2 V, 1200 mV

Various Companies made equivalent IC, such as
- AMS1117 by Advanced Monolithic Systems
- LD1117 by STMicroelectronics
- NCP1117 by ON Semi

Cons
- The Regulator stops working when VIN drops below VOUT + 1.2V. For 3.3 V VOUT we need minimum 3.3 V + 1.2 V = 4.5 V Minimum VIN. Hence not recommended for LiPo or Li-ion battery (max voltage is 4.2 V)
- High Quiescent Current (5mA). Burns 5mA continously, even MCU is sleeping.
- High Heat Disipation.
- Output Noise - 200uVrms

Pros
- Excellent for USB Powered devices (5 V). 
- Extreamly Cheap

### 2 Gen (2000 - 2010) CMOS Revoltution
XC6206, MCP1700, MP1584, MO2307 
- Low Quienscent current (Iq) : 1uA
- Dropout Voltage : 250mV
- Output Current : 200 mA
- Battery Range : 3.25 V to 6 V

### 3 Gen (2010 - Present) Performance boost 
AP2112K, RT9013, TPS7A0233, MAX38903. Enable Pin.
- Quienscent current (Iq) : 55 uA
- Dropout Voltage : 250mV
- Output Current : 600 mA
- Output Noise : 50 uVrms
- Battery Range : 3.25 V to 6 V


### Comparision Table for ESP32

| LDO Model | Company | Output | Iq | Drop V | Examples | Remarks |
| --- | --- | ---| --- | --- | --- |--- |
| RT9080 | Richtek | 600 mA | 2 uA | 100 mV  | Sparkfun ESP32 C3, C6, S3 | Dual Rail |
| MIC5528 | Microchip | 500 mA | 55 uA | 275 mV | Adafruit Feather ESP32-S3 | Widely Used  | 
| AP2127K | Diodes Inc | 1 A | 55 uA | 280 mV | -  | High Current |
| MAX38903 | Analog Devices | 300 mA | 5.5 uA | 140mV  | - | - |
| TLV75533 | Texas Instruments | 500 mA | 19 uA | 305 mV | - | - |
| XC6220B | Torex | 1 A | 80 uA | 250 mV | Xiao C3 | High Current |
| RT9013 | Richtek | 500 mA | 20 uA | 240 mV |  - |Popular |
| MIC5504 | Microchip | 300 mA | 38 uA | 90 mV | - | - |
| ME6211 | Microne/ Nanjing | 300 mA | 40 uA | 100 mV | C3 Super Mini|Cheap |
| XC6206P | Torex | 200 mA | 1 uA | 250 mV | - | Maximum Bty Life |
| MCP1700 | Microchip | 250mA | 2 uA | 625 mV | - | - |

> Chienese Dev kit maker like Espressif, seeedstudio, drobot, waveshare, etc uses chinese Voltage regulator like ME6211 (ESP32 C3 Super Mini), SGM2212 (ESP32 C3 Devkit C-02) etc.

## Transistor
Transistor are like switches or amplifiers (if we pass small current or voltage, it will let large current flow through it.). There are mainly 2 types of transistor.

### BJT
- BJT stands for Bipolar Junction Transistor.
- It's of 2 Types NPN & PNP. 
- Current is applied to open gate. Less efficient due to power consumption.
- Suitable for small power. 100 - 200 mA Max
- 2N222, BC547, BC557, TIP120

### MOSFET
- MOSFET stands for Metal Oxide Semiconductor Field Effect Transistor.
- It's of 2 types N Channel, P Channel. 
- Voltage is applied to open gate. More efficient as it does not draw current. 
- Suitable for large Power consumption devices.  upto 100A. 
- IRLZ44N, IRF5305, IRF520
- MOSFET Driver - TC4420, TC4428, IR2113
> IR stands for International Rectifier is a American Company.

### Logic Level Mosfet
These can open gate with 3.3v or 5v supply. It is denoted by L in IRL such as IRLZ44N, IRL540N, 2N7000. These are easier to configure with Micro Controllers.

Use MOSFET than BJT, Due to Its efficiency


## Relay
Relay Modules are electro mechanical type switches. It is good for AC load. Creates Isolation between controller and load.


## What is the use of enable pin in LDO IC?
The enable (EN) pin on a low-dropout voltage regulator (LDO) acts as an ON/OFF switch to control the regulator's output. It allows a microcontroller or other logic circuit to shut down the LDO to save power or to enable it for a specific application. 

## Connector
- JST Connector 2 Pin for Lipo Battery. JST Stands for Japan Solderless Terminal. JST-PH (2mm), JST-XH (2.54 mm), JST-SH (1mm).

- Screw Terminal (Block Terminal Connector). KF128 (5.08mm pitch), KF301 (5.08mm). Mainly used in AC Current.

## Tips & Tricks
- Cirkit Designer studio for bread board
- Monochrome lcd for ruggedness 2.4 inch
- Use internal pullup resistor to avoid adding resistor to button




