## About
CANalyze is an open source, native CAN interface for Linux that can be built entirely using open source tools. It enables you to monitor and transmit CAN frames using [can-utils](https://github.com/linux-can/can-utils). Start hacking cars by connecting to the OBD-II port.

<p align="center"><img src="https://raw.githubusercontent.com/kkuchera/canalyze/master/assets/images/canalyze1.jpg" width="250"></p>

## Installation
1. [build](https://github.com/kkuchera/canalyze-fw) or [buy](https://www.tindie.com/products/Muted/canalyze/) a CANalyze
2. `$ sudo apt-get install can-utils`
3. start hacking

You also need a [USB 2.0 type A male to type B male cable](https://www.amazon.com/AmazonBasics-USB-2-0-Cable-Male/dp/B00NH11KIK/) and an OBD-II to DB9 cable. Both a [CiA DS102-2](http://mouser.com/ProductDetail/EasySync/OBD-M-DB9-F-ES/?qs=pLQRQR43dtrcAQQLCUAIxA%3D%3D) or [standard](https://www.sparkfun.com/products/10087) OBD-II cable will work.

## Getting started
Bring up CAN interface
```shell
$ sudo ip link set can0 up type can bitrate 500000
```
Sniff CAN messages
```shell
$ cansniffer -c can0
```
or dump all CAN messages
```shell
$ candump can0
```
Send a CAN message
```shell
$ cansend can0 666#01020304
```

## More info
Don't know what's next? Check out
* [Open Garages' videos](https://www.youtube.com/playlist?list=PLBqtCp9s_lnEOtf6I1DDMEANIzJJLXRhe)
* [Car Hacker's Handbook](http://opengarages.org/handbook/)
* [Car hacking papers](http://illmatics.com/carhacking.html)

or subscribe to the Open Garages' [mailing list](https://groups.google.com/forum/?fromgroups#!forum/open-garages).

## Sources
* [firmware](https://github.com/kkuchera/canalyze-fw)
* [hardware](https://github.com/kkuchera/canalyze-hw)
