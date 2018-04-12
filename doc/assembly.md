# Final Assembly Steps

The assembly files included in _../Fabrication_and_Assembly_Files_ are populated with nearly all of the compoents for the full board.
A few additional components need to be hand soldered (or added to the pick and place data).

### Board as recieved from PCB Assembly House
![PCB_Board](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/assembled.jpg)

#### Add 8-way headers
The header pins (Farnell item 1593441), used to select the output current, need to be soldered into these spaces:

![header_slot](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/header-slot.jpg)

![header](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/8way-header.jpg)

#### Output connectors
Output connectors (2.54mm pitch) can be soldered into:

![outputs](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/output-slot.jpg)

#### Arduino socket
2 rows of 12 pins (2.54mm pitch) need to be soldered in to allow the Arduino to connect. Any standard 2.54mm socket should be fine. The Arduino could be soldered directly in, but if it becomes damaged, it will be difficult to replace. 

![arduino_slot](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/arduino-socket.jpg)

#### On/off switch

I used a stock Altium footprint for a switch, but haven't found a suitable switch which matches (I'm sure one will be available from Farnell). In the meantime, I used a 4 pin switch we already had (Farnell 2435325) and snipped off 2 of the legs to fit it in.

![switch_slot](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/switch-slot.jpg)

![switch](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/switch.jpg)

### Finished board
![Finished_Board](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/finished.jpg)
