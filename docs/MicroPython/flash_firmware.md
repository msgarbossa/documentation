# Flash Firmware

## Download

https://micropython.org/download/esp32/

Use firmware built with ESP-IDF v4.x

## Erase flash

```bash
$ esptool.py --port /dev/ttyUSB0 erase_flash
esptool.py v3.1
Serial port /dev/ttyUSB0
Connecting........_____....._____.....__
Detecting chip type... ESP32
Chip is ESP32-D0WDQ6 (revision 1)
Features: WiFi, BT, Dual Core, 240MHz, VRef calibration in efuse, Coding Scheme None
Crystal is 40MHz
MAC: 4c:11:ae:73:de:54
Uploading stub...
Running stub...
Stub running...
Erasing flash (this may take a while)...
Chip erase completed successfully in 9.6s
Hard resetting via RTS pin...
```

## Write firmware

```bash
$ esptool.py --chip esp32 --port /dev/ttyUSB0 --baud 460800 write_flash -z 0x1000 ~/Downloads/esp32-20210902-v1.17.bin
0800 write_flash -z 0x1000 ~/Downloads/esp32-20210902-v1.17.bin
esptool.py v3.1
Serial port /dev/ttyUSB0
Connecting........___
Chip is ESP32-D0WDQ6 (revision 1)
Features: WiFi, BT, Dual Core, 240MHz, VRef calibration in efuse, Coding Scheme None
Crystal is 40MHz
MAC: 4c:11:ae:73:de:54
Uploading stub...
Running stub...
Stub running...
Changing baud rate to 460800
Changed.
Configuring flash size...
Flash will be erased from 0x00001000 to 0x00175fff...
Compressed 1527504 bytes to 987584...
Wrote 1527504 bytes (987584 compressed) at 0x00001000 in 22.8 seconds (effective 536.1 kbit/s)...
Hash of data verified.

Leaving...
Hard resetting via RTS pin...
```
