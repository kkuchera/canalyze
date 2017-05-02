# User Guide
General user information and details about the hardware.

## Hardware
<p align="center"><img src="https://raw.githubusercontent.com/kkuchera/canalyze/master/assets/images/canalyze2.jpg" width="500"></p>

1. **reset button** - 
Resets the micro controller when pressed.
2. **DIP switches** - 
Switch 4 (top one) is used to add a 120 ohm termination resistor to the CAN bus. When it is set to the left as in the image, no termination resistor is added. When set to the right, the termination resistor is added. "TERM" is printed between the DIP switches and the DB9 connector to indicate this. Switches 1-3 (bottom ones) are used to select the type of CAN DB9 cable connected. When they are to the right as in the image, a [CiA DS102](http://affon.narod.ru/CAN/DS102.pdf) cable is selected. When they are to the left, a [US style OBD-II to DB9](https://www.sparkfun.com/products/10087) cable is selected. Note the difference in pinout. "CiA DS102" and "OBD" are printed next te the DIP switches to indicate this. It is important that all of these three switches are on the same side and not for example two to the left and one to the right. Only change them when the device is unpowered.
3. **CAN DB9 connector** - 
Connect to the CAN bus using a [CiA DS102](http://affon.narod.ru/CAN/DS102.pdf) or [standard](https://www.sparkfun.com/products/10087) OBD-II to DB9 cable.
4. **boot button** - Sets the micro controller in bootloader mode when used with reset.
5. **USB 2.0 type B male connector** - Powers the device and connects it to the host via full speed USB.

## LED indicators
* green blink - interface down
* green steady - interface up
* red blink - bus error
* red steady - firmware error

## Firmware update
1. download the latest firmware
2. enter bootloader mode
3. flash the firmware

Download the latest version of the [firmware](https://github.com/kkuchera/canalyze-fw/) from github. Make sure to include the third party libraries. Compile it by going into the root directory and typing `make` on the command line. Put the device in bootloader mode by holding the BOOT button and then pressing the RESET button. All the LEDs should be turned off. Then flash the device by typing `make dfu` on the command line. Finally press reset to return the device to application mode.
