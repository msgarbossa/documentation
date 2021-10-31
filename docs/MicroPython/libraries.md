# Libraries

## Note about MicroPython and I2C

In my experience, I've had more issues with multiple devices on a single I2C bus with Micropython than with Arduino.  A lot of forums say additional resistors are needed or blame the hardware or the drivers.  The same hardware configurations worked reliably for almost a year with Arduino before I started flashing microcontrollers with MicroPython.  The easy fix was to just use SoftI2C and put the 2nd I2C device on another software-defined bus.  This could present issues if trying to use more than a few I2C devices, but it has worked reliably.

## mqtt library

```bash
wget https://raw.githubusercontent.com/pycom/pycom-libraries/master/examples/mqtt/mqtt.py
ampy --port /dev/ttyUSB0 --baud 115200 put mqtt.py
```

# SSD1306 OLED library

```bash
wget https://raw.githubusercontent.com/micropython/micropython/master/drivers/display/ssd1306.py
ampy --port /dev/ttyUSB0 --baud 115200 put ssd1306.py
```

# BME280 library

```bash
wget https://github.com/RuiSantosdotme/ESP-MicroPython/blob/master/code/WiFi/HTTP_Client_IFTTT_BME280/BME280.py
ampy --port /dev/ttyUSB0 --baud 115200 put BME280.py
```

# AHT10 library

```bash
wget https://raw.githubusercontent.com/targetblank/micropython_ahtx0/master/ahtx0.py
ampy --port /dev/ttyUSB0 --baud 115200 put ahtx0.py
```
