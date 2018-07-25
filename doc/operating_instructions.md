# Operating Instructions

### Programming the Arduino
Currently the board has a 3.3V Arduino Pro Micro.

The Pro Micro isn't included in the default set of Arduino boards. Follow the steps here to setup:

https://learn.sparkfun.com/tutorials/pro-micro--fio-v3-hookup-guide/installing-windows#windows_boardaddon

Once connected, open the Adruino code from the _src/DUE_DAC_ folder. The operating frequencies of the 6 current sources can be set by editing _frequencies.h_.

**Upload settings**

If the boards have been updated successfully, select Tools->Boards->Sparkfun Pro Micro.

Once programmed, the usb lead is no longer needed and can be disconected.

<br><br>

### Setting output current
The banks of 2x4 headers on the board are used to set the output current, by connecting a jumper between sets of pins.

![HEADERS](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/output-jumper.jpg)

The values of gain resistor on the board are 50k (12uA) , 20k (30uA), 10k (60uA) and 5k (120uA), but these could be replaced if different values are needed. 

**NOTE: The silkscreen text is the wrong way round! The leftmost set of jumpers is the lowest current, and the rightmost is the highest**

Each CS has two sets of headers (there are two op amps used in the output stage), which should be set to the same value.

<br><br>

### Starting stimulation

**Conenct output leads and 3.7V LiPo battery**

**Start/stop stimulation with push button**

The push button turns on/off power to the Arduino and current sources. Assuming the Arduino has been programmed, once powered up the CS should start outputting after a few seconds.

<br><br>

### Charging battery
There is a LiPo charging circuit built into the board. Attaching a USB Micro lead will charge a connected battery.
