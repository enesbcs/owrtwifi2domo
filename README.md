Be a patron at [Patreon](https://www.patreon.com/enesbcs)

This is a Domoticz Python plugin for receiving MQTT data from OpenWRT using the following script:
https://github.com/dersimn/owrtwifi2mqtt

MQTT parts based on heavily on the [zigbee2mqtt] project (https://github.com/stas-demydiuk/domoticz-zigbee2mqtt-plugin) 
big thanks for it!

## Prerequisites

Tested and works with Domoticz v4.x.

If you do not have a working Python >=3.5 installation, please install it first! ( https://www.domoticz.com/wiki/Using_Python_plugins )

If you do not have an MQTT server yet, install Mosquitto for example:
http://mosquitto.org/blog/2013/01/mosquitto-debian-repository/

## Installation

1. Clone repository into your domoticz plugins folder
```
cd domoticz/plugins
git clone https://github.com/enesbcs/owrtwifi2domo.git
```
2. Restart domoticz
3. Go to "Hardware" page and add new item with type "owrtwifi2domo"
4. Set your MQTT server address and port to plugin settings
5. Remember to allow new devices discovery in Domoticz settings

Once plugin receive any MQTT message to 'owrtwifi/status/' path it will try to create appropriate device.

## Plugin update

1. Stop domoticz
2. Go to plugin folder and pull new version
```
cd domoticz/plugins/owrtwifi2domo
git pull
```
3. Start domoticz

