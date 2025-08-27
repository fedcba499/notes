## What are ESP32 series modules that include an on-chip USB-to-serial (UART) converter?
- ESP32-C3
- ESP32-C6
- ESP32-S3
- ESP32-H2

These modules do not require an external USB-to-UART bridge (like CP2102 or CH340) for flashing and debugging, as they have a built-in USB interface that supports both serial communication and firmware updates via USB CDC (Communication Device Class).

## ESP32 Cam
ESP32 Cam Module has inbuilt SD Card reader.(Thus removing complexity of 6 Wire). TP 4056 power supply module to provide stable 5v power supply to esp32-cam module. switch on +ve wire from 4056 to esp32 cam. (Serial Peripheral Interface) SPI Communication protocal for communication with sd card.
> The U2RXD pin on the ESP32 refers to UART2 Receive Data (RX), which is a pin designated for receiving data via the UART (Universal Asynchronous Receiver-Transmitter) protocol.

> Remove SD Card while uploading code to esp32 cam

