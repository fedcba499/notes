## Flight Controller
- SpeedyBee
- Zerodrag (Made in India) https://zerodrag.in/products/zerodrag-nova-f4
- Botlab dynamics (made in India)
- The Dark Matter (https://thedarkmatter.in/)
- Pixhawk
- iflight flight controllers

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
- 




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




