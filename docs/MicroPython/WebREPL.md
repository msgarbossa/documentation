# WebREPL

webrepl is not enabled by default.  WebREPL is great for remotely managing a MicroPython controller connected to the network without the need for a serial port connection.  Most online documentation says to run import webrepl from a REPL shell and follow the prompts.  This isn't really neccessary as it's better to have more control over the setup process, which can be copied from project to project.

### Create file with webrepl password and upload

```
echo "PASS = 'password'" > webrepl_cfg.py
ampy --port /dev/ttyUSB0 --baud 115200 put webrepl_cfg.py
```
### import webrepl

At the top of main.py with other import statements:

```
import webrepl
```

### start webrepl

Add the following to main.py after WiFi is connected and `print(station.ifconfig())` runs successfully:

```
webrepl.start()
```

### webrepl client tool

The client tool is hosted at http://micropython.org/webrepl/.  It runs locally from the browser.

It's recommended to make a DHCP reservation for the MAC/IP so the IP address can be consistently used for remote connections.