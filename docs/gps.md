## What brand of GPS to be used and Why?
**Ublox** is go to GPS solution, because od its non chinese origin. We can use UCenter to make changes to GPS Configuration. UBlox is of Swiss Origin.

## What are Satelite Bands and in which does Navic operates?
L1, L2 and L5 frequencies. L1 - GPS / Glonass. Navic works on L5 and S band. S band prone for interference with cellular and wifi networks. As Navic operates at 35000m height. Signal strength week.
> Navic-01 developed by isro ( which is L1, L5 and S frequencies receivers)
So any receivers of L5 frequencies can get navic signal.
> Gagan - geo stationary satellite for accuracy ( Satellite based Augumenation System) especially used for aircrafts. For ionosphere correction 

## What is Satelite Bases Augmentation System (SBAS)?
SBAS (Satellite-Based Augmentation System) → Uses satellites like GAGAN (India), WAAS (USA), EGNOS (Europe) to send free correction data. It uses geostationary satellite to send corection data.

## What is RTCM?
RTCM 3.x Corrections from a Local Base Station → If you have a nearby base station (e.g., ZED-F9P, CORS network), you can send RTCM corrections over UART or Bluetooth for better accuracy. (Both modules can use this). Rtcm support dgnss modules ublox are as under
- Neo m8p
- Zed f9p
- Zed f9r ( includes imu )
- Neo f9p
- Neo m9n

## What is CORS Network?
CORS stands for Continously Operating Reference Station. Surevey of India operates more than 1500 Station for weather an GPS corrections. Using these corrections we can improve location accuracy. It is transmitted through internet. so we need to add IP address of CORS network to our UCenter software, to do live corrections.
> https://cors.surveyofindia.gov.in/index.php

## What are various types of Antenna?
- Hellical
- Patch type
- Multi stacked patch ceramic antenna (square size of path decides which frequency it is designed for
better for compact)
- Dome antenna ( external flying saucer antenna) better for multiband
- Thin film type
- Circular plate type
- Rod type
> Taoglas has good collection of gps antennas in various form factor and type ( pcb, flex, patch type, ceramic type etc )

## What are major technologies used in GPS location?
- Carrier Phase Measurement. Very Accurate. Used in Real Time Kinematics and Post Processing Kinematics.
- Pseudo Random Code. Low Cost GPS

![Carrier Wave Measurement vs Pseudo Random Code](images/gps_wave.png)

*Carrier Wave Measurement vs Pseudo Random Code*













