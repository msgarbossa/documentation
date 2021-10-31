
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

- [room temp sensor](https://github.com/msgarbossa/micropython-room)
- [room temp sensor with CO2](https://github.com/msgarbossa/micropython-room)
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
- [doorbell](https://github.com/msgarbossa/esp32-doorbell) - replacement for standard doorbell chime with do-not-disturb settings, MQTT notifications, and indoor motion sensor
- [plant water](https://github.com/msgarbossa/esp32-plant-water)

## Home Automation Software

- [Backend](./Home_Automation_Software/backend.md) - MQTT, NodeRed, and Prometheus (TBD)
- [Dashboard](./Home_Automation_Software/dashboard.md) - Grafana (TBD)
- [Alerts](./Home_Automation_Software/alerts.md) - Slack, NodeRed, Prometheus AlertManager (TBD)
- [MQTT buttons](./Home_Automation_Software/mqtt_buttons.md) - NodeRed, Home Assistant (TBD)
- [Zwave](./Home_Automation_Software/zwave.md) - NodeRed and ZWave-JS (TBD)
- [Tasmota](./Home_Automation_Software/tasmota.md) - Tasmota and NodeRed (TBD)

## Ansible

- [port_scan_facts](https://github.com/msgarbossa/port_scan_facts) - Ansible role to test TCP port connectivity and return the results as Ansible facts
- [chrony](https://github.com/msgarbossa/chrony) - Ansible role to install and configure chrony for NTP time synchronization
- [auto_patch](https://github.com/msgarbossa/auto_patch) - Ansible role sets up a cron job to automatically apply updates and optionally reboot if required
- [k8s-cluster-setup](https://github.com/msgarbossa/k8s-cluster-setup) - Ansible playbooks to setup a Kubernetes cluster

### Other Python projects

- [prom-sudo-events](https://github.com/msgarbossa/prom-sudo-events) - Prometheus exporter written in Python that tails journald to generate metrics (sudo chosen for testing)
- [perf-linux](https://github.com/msgarbossa/perf-linux) - One of my first Python projects to grab detailed performance data for 1 minute and create a report on system performance with built in analysis for certain conditions
