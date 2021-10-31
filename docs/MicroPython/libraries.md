# Libraries

There are multiple versions of these libraries available from different sources.  The ones listed below are ones that worked for me.

## Note about MicroPython and I2C

In my experience, I've had more issues with multiple devices on a single I2C bus with Micropython than with Arduino.  A lot of forums say additional resistors are needed or blame the hardware or the drivers.  The same hardware configurations worked reliably for almost a year with Arduino before I started flashing microcontrollers with MicroPython.  The easy fix was to just use SoftI2C and put the 2nd I2C device on another software-defined bus.  This could present issues if trying to use more than a few I2C devices, but it has worked reliably.

## mqtt library

https://raw.githubusercontent.com/pycom/pycom-libraries/master/examples/mqtt/mqtt.py

# SSD1306 OLED library

https://raw.githubusercontent.com/micropython/micropython/master/drivers/display/ssd1306.py

# BME280 library

https://github.com/RuiSantosdotme/ESP-MicroPython/blob/master/code/WiFi/HTTP_Client_IFTTT_BME280/BME280.py

# AHT10 library

https://raw.githubusercontent.com/targetblank/micropython_ahtx0/master/ahtx0.py

# MH-Z19B library

I can't find where I found this, but it's one of the simpler ones.  It just reads raw values instead of using the automatic calibtration.  I've had problems with the automatic calibration because it assumes the sensor is running continuously for long periods of time.

https://github.com/msgarbossa/micropython-room-co2/blob/master/mhz19b.py
