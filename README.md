![Logo](admin/smappee.png)
# ioBroker.smappee

[![NPM version](http://img.shields.io/npm/v/iobroker.smappee.svg)](https://www.npmjs.com/package/iobroker.smappee)
[![Downloads](https://img.shields.io/npm/dm/iobroker.smappee.svg)](https://www.npmjs.com/package/iobroker.smappee)

[![NPM](https://nodei.co/npm/iobroker.smappee.png?downloads=true)](https://nodei.co/npm/iobroker.smappee/)

An ioBroker adapter for smappee - devices

#### You need to install first ioBroker.MQTT adapter (or use another MQTT-broker) and activate your Smappee's MQTT publishing. Please see the following instructions bevore installing the Smappee adapter.

This adapter brings you realtime (1s-interval) energy  power data, aggregated data for energy and optional sensor consumption data and access to your switches/plugs of your Smappee - Device to ioBroker.

## Instructions
### Installing ioBroker.mqtt - Adapter.
Please add an instance of the ioBroker.mqtt - Adapter:

![ioBMQ](https://github.com/forelleblau/ioBroker.smappee/blob/master/admin/ioBrokerMQTTBroker.PNG)

configure the instance as server/broker. Port 1883 as default is ok, feel free to choose any other working.
Set username and password (you will need this for smappee- and smappee-Adapter configuration:

![ioBMC](https://github.com/forelleblau/ioBroker.smappee/blob/master/admin/ioBrokerMQTTConfig.PNG)

### Activation of Smappee's MQTT publishing.

Open your browser and avigate to the URL: http://X.X.X.X/smappee.html (replace X.X.X.X by Smappee's IP address in your network).
Click the logon/logoff button and use the password "admin" to Logon.

![smplogon](https://github.com/forelleblau/ioBroker.smappee/blob/master/admin/smplogon.png)

Go to the "advanced" section an activate the "Advanced" checkbox in the last field of the table.

![smpadv](https://github.com/forelleblau/ioBroker.smappee/blob/master/admin/smpadv.jpeg)

Then you should be here:

![smpmqt](https://github.com/forelleblau/ioBroker.smappee/blob/master/admin/smpmqt.png)

Enter your ioBroker´s Ip followed by the port you specified for the mqtt-broker (default is 1883), i.e. tcp://192.168.1.111:1883

Enter username & password you specified configuring your mqtt-broker.
Then hit "Apply changes and restart monitor".

And now it´s time to

### Install the smappee-adapter

Create an instance of the smappee-adapter and enter username & password you specified configuring your mqtt-broker.

If you use other than ioBrokers MQTT-Adapter with default settings, you can optionally specifiy the connection to your MQTT Broker (host & port).

Please give the adapter some minutes to read the data from your smappee device.

### Data aggregation or separaion (hourly, daily, yearly,.. values)

Some of smappee's values are 'couters', some are values for a certain period.
For aggregation or separation of data, please use the ioBroker.statistics adapter.




## Changelog
### 0.1.0
  - Gas_Water sensor integrated, 'alwaysOn' integrated. 
### 0.0.5
  - design-bug fixed, Gas_Water Sensor integrated (only raw value).
### 0.0.4
  - credentials - bug fixed, more efficient design, gulp update

### 0.0.3
 - first tested version, bugs in config fixed.

### 0.0.2
 - reads phase config, reports single phase data.

### 0.0.1 Initial version

- inital version, displays realtime power und energy consumption.


## License
The MIT License (MIT)

Copyright (c) 2018 forelleblau marceladam@gmx.ch

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
