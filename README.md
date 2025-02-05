# homebridge-sengleds

Note: I am trying to get this to work with my Sendled light strips and implement MQTT support

An unoffical [Homebridge](https://github.com/nfarina/homebridge) platform plugin for Sengled accessories.

This plugin uses the existing Sengled Element Home app infrastructure to allow you to control your Sengled accessories that uses zigbee. It'll let you turn on/off the lights and control brightness and color temperature using the Home app.

Provide your username and password and register as a platform, and it will auto-detect the light bulb you have registered.

Note that I only have **Element Classic A19 Kit (Light bulbs + Hub)** to test  
https://us.sengled.com/products/element-classic-kit  

This plugin is still in beta.  
If you encounter anything out of this product. Issue and Pull Request is welcome 🙂.

# Installation

1. Install homebridge using: `npm install -g homebridge`
2. Install this plugin using: `npm install -g homebridge-sengleds`
3. Update your configuration file. See below for a sample.

# Configuration

![](config.png)

Configuration sample:

```
"platforms": [
  {
    "platform": "SengledHub",
    "name": "SengledHub",
    "username": "***",
    "password": "***"
  }
]
```

## Optional parameters

- debug, this will enable more logging information from the plugin

```
"platforms": [
  {
    "platform": "SengledHub",
    "name": "SengledHub",
    "username": "***",
    "password": "***",
    "debug": true
  }
]
```

## Credits

- Inspired by [homebridge-vesync](https://github.com/AlakhaiVaynard/homebridge-vesync) project
