# Greenhouse

![Greenhouse](./img/Greenhouse.jpg)

## Team Members

- Matias Vereecke
- Maxim Govaert
- Emiel Coucke

## Materials

- plc
- 4 temperature sensors(inside/outside)
- 1 or 2 Raspberry Pi 4b (Node Red and MQTT)
- 2 monitors

## Prerequisites

Make sure you install following things on the pi:

For Node Red:

```bash
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
sudo systemctl enable nodered.service
```

For MQTT:

```bash
sudo apt install mosquitto mosquitto-clients
sudo systemctl enable mosquitto
sudo systemctl status mosquitto

apt update
sudo apt install mosquitto-clients
```

```bash
mosquitto_sub -d -u username -P password -t "sensor/temp1"
mosquitto_sub -d -u username -P password -t "sensor/temp2"
mosquitto_pub -d -u username -P password -t "sensor/temp1" -m 10
mosquitto_pub -d -u username -P password -t "sensor/temp2" -m 10
```

## components

see documentation: 
- [mqtt](components/mqtt.md)
- [security webpage](components/webpage.md)
- [Node Red](components/nodered.md)

