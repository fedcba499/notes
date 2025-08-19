## Flashing MicroPython onto ESP32
ESP32 boards normally come blank or with the Arduino Bootloader. To run Python, we need to flash MicroPython Firmware (.bin file). We used esptool.py to erase flash and then write the MicroPython Firmware.
```shell
python -m esptool --chip esp32 --port COM3 erase_flash
python -m esptool --chip esp32 --port COM3 --baud 460800 write_flash -z 0x1000 esp32-20230426-v1.20.0.bin
```
## Pycharm Setup with MicroPython Tools Plugin by Lukas Kremla
Adds a MicroPython Tools panel at the Left Bottom to Pycharm IDE. Lets PyCharm connect directly to ESP32 over USB/COM. Provides a **File System View** so we can see nd manage files stored on the ESP32.

## Connecting the Board
File > Settings > Languages & Frameworks > MicroPython Tools. Enable MicroPython Support.

## MicroPython Stubs
PyCharm didnt recognize special MicroPython Modules (machine, Pin, network etc) Stubs helps in linting and code completion.

## Upload Code
Right click on main.py, upload to MicroPython Device. It copies main.py to ESP32 Flash Storage

## Running Code
Micropython run two special files automatically. boot.py and main.py
