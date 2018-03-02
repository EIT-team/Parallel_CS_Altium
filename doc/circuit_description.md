## Top level schematic
The design uses Altium's hierarchical sheet setup to replicate the CS block six times
Additional sheets are used for the Power Supply/USB/Buttons and for the Arduino connector and clock source
![TOP](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/top_level.PNG)

## Arduino Connector
A footprint for an Arduino Pro Micro/Pro Mini is included, which is used for sending SPI signals to the DDS chips. Each of the six current sources has its own FSYNC line.
The Arduino will need to be programmed once using the Arduino IDE, after which the frequencies are stored on board and it can be powered by the batery input.
![ARDUINO](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/Arduino.png)

## Clock source
LTC6900 is used to generate a 10MHz clock signal for the DDS chips.  The clock speed is set by the resitor R17.
![CLOCK](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/Clock.png)

##Negate voltage generator
The op amps used in the single ended to differential convertor and the Howland Current Pump require a negative voltage. The LTC1044 generates this, from either the battery input or the USB line.
![VOLTAGE](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/Negative_voltage_converter.png)

## Battery and USB charger
Power can be supplied to the cirucit (including the Arduino) from a battery, or from the USB line. Switch S1 connects the battery, powering up the circuits. The on board LiPo charger can be used to charge the battery over USB.
![BATTERY](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/battery.png)

## DDS and analog filter
AD9833 generates a 10-bit sine wave with 0.6V amplitude, the frequency is programmed over SPI from the Arduino. Op-amps U3A/U3B impement an image filter to reduce the higher frequency components on the sharp edges of the DDS signal.
![DDS](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/AD9833.PNG)

## Single ended to differential conversion
The signal from the DDS/Filter block is single ended (reference to ground), but for parallel injection, differential signals are needed. These can be generated _either_ by the U9A/U9B op amp configuraiton _or_ the AD8476 IC. The AD8476 is a more expensive compoent, but is a simpler solution.
![DIFF](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/single_to_diff.PNG)

## Howland Current Pump
A differntial input Improved HCP circuit converts the DDS voltage signal to an output current. 4 output resistors are included to allow for selection of the output current, by using the header connections P2/P3 (both headers should be set to the same value).

![HCP](https://github.com/EIT-team/Parallel_CS_Altium/blob/master/doc/images/HCP.PNG)
