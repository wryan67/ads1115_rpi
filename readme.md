# ADS1115 Raspberry Pi Library

This app will read the values on a0-a3 and print them on the screen, reference voltage can be set on the command line

Copyright (c) 2019 Wade Ryan


## Requirements
On your Raspberry Pi, please use the raspi-config program to enable the I2C interface.
Then use the gpio command to make sure your i2c devices can be found.  The default address 
for an ADS1115 chip is 0x48.  

	$ sudo raspi-config
	$ gpio i2cd


## Install

To compile this library, navigate into the src folder and use the make utility to compile 
and install the library.

    $ cd [project folder]
    $ cd src
    $ make && sudo make install


## Compiling
Complie your applications using these command line arguments: -lwiringPi -lwiringPiADS1115rpi

## Example
To run the example program, nagaviate into the example folder and use make to compile the program.  

    $ cd ../example
    $ make 
    $ ./knobtest
    $ $ accessing ads1115 chip on i2c address 48
    $ Timestamp       delta       A0       A1       A2       A3
    $ 1575219689268      44     1.73     3.91     0.00     0.00
