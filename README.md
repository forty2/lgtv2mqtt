# lgtv2mqtt

> Interface between LG WebOS Smart TVs and MQTT

### Getting started

* Install

```npm install -g lgtv2mqtt```


* Start 

```lgtv2mqtt --help```  

### Topics subscribed by lgtv2mqtt

Topics and Payloads follow [mqtt-smarthome Architecture](https://github.com/mqtt-smarthome/mqtt-smarthome).

#### lgtv/set/mute

Enable or disable mute. Payload should be one off '0', '1', 'false' and 'true'.

#### lgtv/set/volume

Set volume. Expects value between 0 and 100.

#### lgtv/set/toast

Show a Popup Message. Send Message as plain payload string.

#### lgtv/set/launch

Lauch an app. Send AppId as plain payload string.

#### lgtv/set/media.controls/play

#### lgtv/set/media.controls/pause

#### lgtv/set/system/turnOff


### topics published by lgtv2mqtt

#### lgtv/status/volume

Reports volume changes. Payload is the plain value.

#### lgtv/status/mute

Reports mute changes. Payload is '0' (not muted) or '1' (muted).

#### lgtv/status/foregroundApp

Reports which App is currently in foreground. (example Payloads: 'netflix', 'com.webos.app.livetv', 'com.webos.app.hdmi2')

#### lgtv/status/currentChannel

Reports current channel if foregroundApp is 'com.webos.app.livetv'. Payload is a JSON String, property val contains the
channelNumber, underneath 'lgtv' you will find more properties with detailed information.

## License

MIT © [Sebastian Raff](https://github.com/hobbyquaker)


