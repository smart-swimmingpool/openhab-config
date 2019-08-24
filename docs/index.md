# OpenHAB Configuration | 🏊 Smart Swimmingpool 

**🏊 The Homie 3.0 compatible Smart Swimmingpool Controller 🎛️**

Configuration example to use the Smart Swimming Pool system on openHAB

Configuration sources: [https://github.com/smart-swimmingpool/openhab-config](https://github.com/smart-swimmingpool/openhab-config)

# Mobile App (openHAB iOS)

| Overview |  Temperature Chart |
: ---------:--------------------:
| ![openHAB Pool Automation overview](openhab-pool-automation-overview.png) | ![openHAB Pool Automation temperature](openhab-pool-automation-temparature.png) |

| Settings | Settings |
:----------:----------:
| ![openHAB Pool Automation settings](openhab-pool-automation-settings-1.png) | ![openHAB Pool Automation settings](openhab-pool-automation-settings-2.png) |



# Precondition

The Smart Swimming Pool project uses Homie 3.0 based MQTT messaging. Therfor you have to install 
an MQTT broker in your environment.

## Raspberry Pi

I use an Raspberry Pi (Model 3) ([Amazon](https://amzn.to/2NnqwDQ)). The latest version of openHAB has an embedded MQTT broker. In this example a seperate broker [Mosquitto](https://mosquitto.org/) on same Raspberry Pi is configured.

## Install Mosquitto

- Install Mosquitto on Raspberry Pi:
  ``` 
  sudo apt-get update
  sudo apt-get upgrade
  sudo apt-get install mosquitto
  ```
- In Paper UI install add-on 'MQTT Binding' from bindings.
- Check `services/mqtt.cfg` for your environment.
