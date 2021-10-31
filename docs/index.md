
## MicroPython

### Reference

Basic steps to get started with MicroPython:

1. [Flash MicroPython](./MicroPython/flash_firmware.md) firmware on ESP32 microcontroller
2. Upload code with [ampy](./MicroPython/ampy.md)
3. Monitor from [serial console](./MicroPython/serial_console.md)

Use [WebREPL](./MicroPython/WebREPL.md) for remote serial connectivity

### Tutorials

- [blink](https://github.com/msgarbossa/micropython-blink) - "hello world" for MicroPython
- [LED dimming with PWM](https://github.com/msgarbossa/micropython-leds) - 
- [mqtt](https://github.com/msgarbossa/micropython-mqtt)
- [SSD1306 OLED](https://github.com/msgarbossa/micropython-oled)
- [motion- HC-SR501](https://github.com/msgarbossa/micropython-motion)

### Projects

- room temp sensor - TBD
- room temp sensor with CO2 - TBD
- bucket mouse trap with motion sensor - TBD

## Arduino

### Reference

- Flash firmware - TBD
- PlatformIO - TBD
- OTA updates - TBD

### Projects

- [leak sensor](https://github.com/msgarbossa/esp32-leak-sensor)
- [room temp sensor](https://github.com/msgarbossa/esp32-room-sensor)
- [garage manager](https://github.com/msgarbossa/esp32-garage-manager)
- [doorbell](https://github.com/msgarbossa/esp32-doorbell) - smart doorbell with do-not-disturb settings and MQTT notifications
- [plant water](https://github.com/msgarbossa/esp32-plant-water)

## Home Automation Tools

- MQTT - TBD
- NodeRed - TBD
- Prometheus - TBD
- Grafana - TBD
- Home Assistant - TBD
- FreeCAD - TBD

## Ansible

- [port_scan_facts](https://github.com/msgarbossa/port_scan_facts) - Ansible role to test TCP port connectivity and return the results as Ansible facts
- [chrony](https://github.com/msgarbossa/chrony) - Ansible role to install and configure chrony for NTP time synchronization
- [auto_patch](https://github.com/msgarbossa/auto_patch) - Ansible role sets up a cron job to automatically apply updates and optionally reboot if required
- [k8s-cluster-setup](https://github.com/msgarbossa/k8s-cluster-setup) - Ansible playbooks to setup a Kubernetes cluster

### Other Python projects

- [prom-sudo-events](https://github.com/msgarbossa/prom-sudo-events) - Prometheus exporter written in Python that tails journald to generate metrics (sudo chosen for testing)
- [perf-linux](https://github.com/msgarbossa/perf-linux) - One of my first Python projects to grab detailed performance data for 1 minute and create a report on system performance with built in analysis for certain conditions
