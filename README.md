# Waveshare42B
corrected driver &amp; demo for the Waveshare 4.2inch e-Paper Module
Model : https://www.waveshare.com/wiki/4.2inch_e-Paper_Module_(B)

![WaveShare Module](https://www.waveshare.com/w/thumb.php?f=4.2inch-e-paper-module-b-3.jpg&width=300)


## Raspberry installation

Be sure to activate SPI & I2C interface in raspi-config

to use this screen on a rasberry, you need to install these modules : python-dev, pillow, spidev

Be sure you have installed libjpeg-dev before pillow installation :
`sudo apt-get install libjpeg-dev`

```
sudo apt-get install python-dev pillow
sudo apt-get install python-smbus python-serial
sudo pip install spidev
```

## Screen Connection

|e-Paper|Raspberry Pi 3B|
|---|---|
|3.3V   |   3.3V - Pin 17   |
|GND  |     GND  - Pin 20 |  
|DIN   |    MOSI - Pin 19  | 
|CLK    |   SCLK - Pin 23   |
|CS    |    CE0  - Pin 24   |
|DC  |      GPIO 25 - Pin 22|   
|RST    |   GPIO 17 - Pin 11  | 
|BUSY   |   GPIO 24 - Pin 18   |

## changed from the Waveshare version
avoid floats using integer when needed in epd4in2b.py
correct importing Pillow

## Links

https://www.waveshare.com/wiki/4.2inch_e-Paper_Module_(B)
https://www.waveshare.com/wiki/Pioneer600#Libraries_Installation_for_RPi
