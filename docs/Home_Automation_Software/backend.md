
# Home Automation Backend


## MQTT

Mosquitto runs great as a container.  Below is a simple script I've used to run Mosquitto as a Docker container on a Raspberry Pi 3B+.  Mosquitto shouldn't need a lot of resources.  Persistent storage is required if running this in a Kubernetes cluster.


```
/export/mosquitto
├── data
│   ├── mosquitto.db
│   └── passwords.txt
├── docker-run.sh
├── log
│   └── mosquitto.log
└── mosquitto.conf
```

mosquitto.conf:
```
per_listener_settings true 
persistence true
persistence_location /mosquitto/data/
log_dest file /mosquitto/log/mosquitto.log
password_file /mosquitto/data/passwords.txt
```

docker-run.sh:
```bash
#!/bin/bash

id mqtt >/dev/null 2>&1
if [[ $? -ne 0 ]]; then
  echo "useradd mqtt"
  useradd mqtt
fi
uid=`id -u mqtt`
gid=`id -g mqtt`

cd /export/mosquitto
chown -R mqtt:mqtt data
chown -R mqtt:mqtt log

docker run -d --restart always --name="mosquitto" -u $uid:$gid -p 1883:1883 -p 9001:9001 -v /export/mosquitto/mosquitto.conf:/mosquitto/config/mosquitto.conf -v /export/mosquitto/data:/mosquitto/data -v /export/mosquitto/log:/mosquitto/log eclipse-mosquitto
```

## Node-RED

The official site has a number of options for setting up Node-RED:
https://nodered.org/docs/getting-started/

Once setup, drop in an `mqtt in` block and add the MQTT server connection parameters.

## Prometheus

TBD
