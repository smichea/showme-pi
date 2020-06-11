# Gyroscope

[connect](https://tutorials-raspberrypi.com/measuring-rotation-and-acceleration-raspberry-pi/) a [GY-521 gyroscope](https://www.lazada.com.ph/catalog/?q=gyroscope+GY-521) to the Pi 

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

install i2c-tools
```
sudo apt-get install i2c-tools
```
