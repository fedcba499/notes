## When to go for designing of PCB?
When component is not readily available. In our case, breakout board of L89HA is readily available, so we use it directly. When breakout boards are not readily available, or when we want to reduce space, as several through hole components occupy greater space than SMD Components.

## When to use seeedstudio XIAO or ESP32 padded Boards?
Always try to use, ESP32 XIAO, But if pin out are required more, then we need to take extra burden of creating code upload circuit, battery management etc. Cost is of not greater concern for our limited quantity over time consumed for creating and planning circuitary.
- When wifi requirement comes, XIAO fails, due to additonal wire for wifi, here on pcb antenna of ESP32 benefits.

## What are most used layer stack in PCB Devkits?
2 Layer stack is widely used on almost on all Devkits except compact or thumb size devkits. Due to cost saving in 2 layer PCB and time saved for production. Below are few websites where opensource hardware schematic, PCB and Gerber files are found.
- Sparkfun.com
- Adafruit.com
- Arduino.com/hardware
- seeedstudio
- oshlab (by EasyEDA/ JLC PCB)
- PCBWay (shared projects)

  

