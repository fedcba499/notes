## RP2350 vs ESP32
| Item        | RP2350                                                    | ESP32                         |
|-------------|-----------------------------------------------------------|-------------------------------|
| Processor   | Arm Cortex M33 (Industry Std) used in STM32, nRF53 Family | Xtensa ( Only used in ESP32 ) |
| Micropython | Natively Supported ( official support )                   | does not accept all libraries |
| Security    | Arm Trust Zone                                            | Basic ( difficult to setup )  |
| PIO         | Suppports Programmable IO                                 | no support                    |

- Use Arduino than micropython, because arduino.h is easier to use, with pinMode, digitalRead, and digitalWrite function, which makes it very easier to use.

- Use Raspberry Pi Pico. It is designed for maker by maker. Its focus on easy to use Microcontroller. It supports Micropython Natively.

- Limit MCU to Micropython. so that it is eaiser to build. limit to esp8266 ( due to its 2mm pin pitch) and ESP32 Varients.

- Use easyeda it is very simple, it does satisfy our use case. easyeda is like python, it has limitation, but it can make development fast. kicad or altium is like c++ professional, but not suited for beginner.

- Use development board to make prototype, with final code.

- Use Fritzing for breadboard diagram. It is easy to use, and has good library support.