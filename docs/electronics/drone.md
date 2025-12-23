## Flight Controller
- SpeedyBee
- Zerodrag (Made in India) https://zerodrag.in/products/zerodrag-nova-f4
- Botlab dynamics (made in India)
- The Dark Matter (https://thedarkmatter.in/)
- Pixhawk
- iflight flight controllers

- caux

## Firmware
- Betaflight
- INAV (Matak, F4, F7)
- Ardupilot

> Start with ardupilot as it is good with stability of drone, then switch to inav, inav is very easy to configure, then move to betaflight, its is best in class firmware.

> for gps features, like hold, hover etc inav is much better than betaflight, as betaflight comes with minimum configuration with respect to gps functionality.



## Program Control
Dronekit-Python - Communicating with drone with mavlink.
MAVLink is a light weight messaging library for messaging between drone and ground control station.

Skybrush for Drone light show. Drone light show require 2 cm level accuray, which require rtk corrections. Skybrush live, skybrush server, skybrush blender addon. Mavlink through wifi router messaging with ground control station (GCS) ie laptop. this mavlink protocol is used for sending RTK Corrections.



## FPV Camera Analog

## GPS Modules
- HGLRC M100-5883 GPS
- Botlab Dynamics https://www.botlabdynamics.store/products/botnavigator-gnss-v1-module

## Drone Battery Packs
Lithium Ion Battery pack is good for normal drones, (18650 Cells)

Lithium Polymer battery pack is good for faster drones, where power discharge required is maximum.

Volatage Range - 2S to 6S (S stands for Series), 1 Cell has 3.0 to 4.2 Volts. 

Capacity - 6000 mAh, capacity increses with parallel connection group.

4S 1P Battery Pack. 4S 2P stands for 4 cells in series and another 4 Cells in parallel group.

Current Rating - 25 A, how many amps does application pulling.
Higher discharge good for racing drone. 

if we connect in parallel, it doubles amphere or current rating.

Higher current density (capacitance), lesser discharge rate or current rating.

Nickel strips for cell soldering.

Build parallel group first, and then connect in series. parallel group in series.

Imedence matching, resistance matching.


## Radio Controller
Radiomaster Pocket Crush

## Radio Receiver
2.4 G Hz Radio single frequency is good for training purposes.
> Radiomaster pocket - elrs and cc2500 versions

> Radiomaster pocket crush -  comes only in ELRS version.

Radiomaster pocket is powered by 18650 battery cells, instead like Flysky uses AA cells.


### ELRS 
ExpressLRS is opensource radio link based on esp32 or STM32. It supports 900 MHz and 2.4 GHz Frequency.

## ESC
Electronic speed controllers comes with 2 processing power 8 bit processor and 32 bit processor. AM32 is a opensource firmware designed to handle 32 bit powered ESC with STM32 chips.

## Camera
Analog Camera are low cost with little lag but offers low latency
CADDXFPV brand 

dji air 3

## Frames
Carbon fibre frames are good with stability than platic frame drones.

Carbon fibre frames comes in 5 inch, 7 inch and 10 inch sizes.

Speedybee BEE35 - 

SpeedyBee BEE25

dead cad frame is not symmetrical and x frame is symmetrical

unibody carbon fiber frame or one-piece carbon fiber frame generally 2 mm

dont go after unibody frame, it is difficult to find (as there is so much wastage of carbon fiber sheet), go for mark4 5 inch, 7 inch, 10 inch. for beginning go for 7 inch.

7 inch good for smooth moving


## Rotors
> Rotor has 2 components, 1. Stator (static and fixed to arm), 2. Rotor (outer moving part). Configuration of rotor has 6015 stands for 60mm diameter of rotor and 15 mm height. magnets are in rotor. 

> Heavier drone requires lower kv motor, lighter requires higher kv motor.

> KV not stands for kilo volt, it stands for number of rotations per minute, if we supply 1 v power, with no load attached.

> If we take larger kv motor, with smaller propeller for heavier drone, it might burn out motor. it is better to take smaller kv motor with larger propeller, so that it is easier for motor to carry weight.

> Higher kv motor are designed for faster fpv, where speed is more important than weight carrying capacity.

- Readytosky 920kv motor is suited for larger propeller, aimed at stabitly at lower rpm. it is suited with 3s or 4s battery.
- GEPRC 2105.5
- speedybee 
- EMAX ECO II Series - aimed at smaller and faster drones
- VectorTechnics (Made in India Motor) - Generally Large Drones
- 2212 920kv
- TMotor High Quality




## Propellers
Two sided propellers are better than 3 sided propellers as 3 sided propellers moves very fast difficult to control by beginners

7×4.5 2-blade prop (polycarbonate, good brand). Or as a slightly safer/milder option: 7×4 2-blade (less pitch = less aggressive).

braided wires to protect motor wires from propeller short circuiting.



## Simulation training software
freefly software in steam program.

## Onlinestores
Quadkart

micropack pcb bangalore

indian drone parts

## Tips & Tricks

Pitch and Roll stick should auto center, similarly throttle stick should never auto centered.

**Roll / Aileron**	Moves your drone left or right in the air, literally “rolling” your drone.

**Pitch / Elevator**	Tilts your drone forward or backward.

**Yaw / Rudder**	Rotates your drone clockwise or counterclockwise, allowing you to make circles or patterns in the air.

**Throttle / Throttle**	Controls the amount of power sent to your drone, which makes the drone go faster or slower.


Reverse throttle.	Menu -> Settings -> Throttle-> Reverse & Similarly do pitch reverse
Gear.	Menu -> Settings -> Aux -> Gear.

## Flight modes 

**Heli mode** - 3 flights mode are possible, To use this set Auxilary Channel 5 to Gear - > Pitch Curve to 0, 50, 100

**Acro Mode** - 6 Flight Mode are Possible. Set Auxilary Channel 5 to Gear, Set Flight mode channel to 6 in Mission Planner, Use Mix 1, 2, 3 to Program Mix Switch. Mix Switch has 3 Positions, these are Normal, ID 1 and ID 2. Uprate is value when Gear switch is up, Downrate is value when Gear Switch is Down. Master channel is Gyr, Slave channel is flr.

Pixhawk main pins and axillary pins doesn't have power. We must supply power us in ESC. I one of the pins get power rest all pins get power they are interconnected.
To assign any task to any pins (ie main pins 1-8 : RC 1-8 and auxiliary pins 1-6 : RC 9-14) go to configuration user params assign specific task to specific pin. 
If you assigned RCIN8 to RC9 which means Radio controller in pin 8 assigned to Auckland pin 1.


## 1 Kg Payload
- Frame : Tarot - 650, 690 dependending on wheel base -SKU: 1578673
- Flight Controller : caux v5+  - CUAV V5+ Flight Controller | Drone Autopilot PX4 APM
- motor - Tarot 4114/320KV - SKU: 1357457, emax EMAX MT3515
new tarot - SKU: 1318850
- esc - ready to sky, emax - 60 A
- 
- 
UAVCAN standard protocol neo 3 pro, uart serial protocol in neo 3

| Category | Item | SKU | Price | Remarks |
| --- | --- | --- | --- | --- |
| Flight Controller | Cauv VX6 | 1590285 | 29,709| Latest Generation |
| Flight Controller | Cauv X7+ | 1504857 | 28,926 | Upgrade to V5+ |
| Flight Controller | Cauv V5+ |  1504856 | 35,119 | Old Model |
| GPS | Cauv Neo 3 Pro |  1504855 | 16,969 | CAN Bus Protocol |
| GPS | Cauv Neo 3 |  1504853 | 10,028 | UART / Serial Protocol |
| GPS Mount | Tarot TL8x005 GPS Mount |  R111342 | 328 | - |
| Frame | Tarot TL65B01 Iron Man 650 | 1578673 | 8,999 | - |
| Motor | T-Motor Navigator MN4014 330KV | 1392063 | 8,499 | Below Anti gravity series Navigator |
| Motor | Tarot 4114 320 KV | 1318850 | 4,641 | Good Quality |
| Motor | Tarot 4008 330 KV | 1578669 | 3661 | Budget alternate to T Motor Navigator MN4014 330KV |
| Motor | EMAX MT3515 650 KV | 29116 (CCW) / 29128 (CW) | 3,589 | 2 Types Motors, Repairability issue|
| Propellers | Tarot TL100D04 15 inch | 1357456 | 1,133 | compatible with 15 inch |
| Propellers | Tarot TL2829 1355 | R111171 | 827 | 13 inch |
| Propellers | 1555 Carbon Fiber Propellers |  RKI-1492 | 864 | 1655, 1855 not suited with Tarot 650 Frame |
| power Distribution board | 
| ESC | T Motor Air 40A Esc | 1092910 | 3,459 | Budget T Motor ESC | PDB-XT60 with BEC 5V and 12V | 57854 | 289 | p |
| ESC | Emax SimonK 60A | 29149 | 1,774 | - |
| Camera | Skydroid C12 | R151313 | 50,751 | 3 axis gimbel |
| Camera | Sydroid C10 | R150076 | 10,200 | 2 axis Base Camera |
| Camera + Remote | Skydroid | RKI-7265 | 77,160 | C12 + H12 Pro |
| Remote | Skydroid H12 | 1871159 | 28,562 | Inbuilt Android Screen |
| Remote | Skydroid T12 | 1619564 | 16,551 | No Screen |
| Battery | Ornage 10000 mAh 6S 25C | 1125089 | 13,388 | - |

