# ampy

## install

Make sure user is in the dialout group to have write permissions to the /dev/ttyUSB0 device.


Install Python modules for ampy (can use Python virtualenv or install globally since it shouldn't conflict with anything else)

```bash
pip3 install adafruit-ampy
pip3 install rshell
```

## upload

```bash
ampy --port /dev/ttyUSB0 --baud 115200 put boot.py
ampy --port /dev/ttyUSB0 --baud 115200 put main.py
ampy --port /dev/ttyUSB0 --baud 115200 put ssd1306.py
```

## download

```bash
ampy --port /dev/ttyUSB0 --baud 115200 get boot.py > boot.py.bak
```

## list files

```bash
ampy --port /dev/ttyUSB0 --baud 115200 ls
```

## remove

```bash
ampy --port /dev/ttyUSB0 --baud 115200 rm BME280.py
```

## run local script on microcontroller

```bash
ampy --port /dev/ttyUSB0 --baud 115200 run main.py
```
