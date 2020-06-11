# Gyroscope

[connect](https://tutorials-raspberrypi.com/measuring-rotation-and-acceleration-raspberry-pi/) a [GY-521 gyroscope](https://www.lazada.com.ph/catalog/?q=gyroscope+GY-521) to the Pi 

## Installation

Activate I2C
```
sudo raspi-config
```
Choose 
```
 5 Interfacing Options  Configure connections to peripherals   
 
 P5 I2C         Enable/Disable automatic loading of I2C kernel module 
```
and select <Yes>
 
then 
```
 sudo nano /etc/modules
```
insert the 2 lines
```
i2c-bcm2708
i2c-dev
```

reboot the Pi
```
sudo reboot
```

install i2c-tools and libi2c-dev
```
sudo apt-get install i2c-tools
sudo apt-get install libi2c-dev
```

## test the installation

Execute
```
sudo i2cdetect -y 1
```
you should see
```
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:          -- -- -- -- -- -- -- -- -- -- -- -- --
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
60: -- -- -- -- -- -- -- -- 68 -- -- -- -- -- -- --
70: -- -- -- -- -- -- -- --
```
