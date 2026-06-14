# OpenHAB Configuration | 🏊 Smart Swimming Pool

Discussions: <https://github.com/smart-swimmingpool/smart-swimmingpool.github.io/discussions>

> ⚠️ **Legacy notice**: [Home Assistant MQTT Discovery](https://www.home-assistant.io/integrations/mqtt/#mqtt-discovery)
> is now the **primary** integration path for the Pool Controller (v3.x).
> openHAB remains fully supported via MQTT but requires manual configuration.

Configuration example to use the Smart Swimming Pool system on openHAB.

## Compatibility

| Controller Version | Home Assistant | openHAB |
|-------------------|---------------|---------|
| **2.x** | Limited support | Recommended |
| **3.x** | Native MQTT Discovery | Manual MQTT configuration |

## Precondition

The Smart Swimming Pool project uses Homie 3.0 based MQTT messaging. Therfor you have to install 
an MQTT broker in your environment.

## Raspberry Pi

I use an Raspberry Pi (Model 3) ([Amazon](https://amzn.to/2NnqwDQ)). The latest version of openHAB has an embedded MQTT broker. In this example a seperate broker [Mosquitto](https://mosquitto.org/) on same Raspberry Pi is configured.

### Install Mosquitto

- Install Mosquitto on Raspberry Pi:
  ``` 
  sudo apt-get update
  sudo apt-get upgrade
  sudo apt-get install mosquitto
  ```
- In Paper UI install add-on 'MQTT Binding' from bindings.
- Check `services/mqtt.cfg` for your environment.

## Documentation

see at [https://smart-swimmingpool.github.io/openhab-config/](https://smart-swimmingpool.github.io/openhab-config/)
