# MicroPython-ST7735

This is a modified version of [GuyCarver's ST7735.py](https://github.com/GuyCarver/MicroPython/blob/master/lib/ST7735.py).

This version is for micropython-esp32.

Any font file is necessary for displaying text (some font files are in [GuyCarver's repo](https://github.com/GuyCarver/MicroPython/tree/master/lib)).

Text nowrap option added(default: nowrap=False).

graphicstest.py is a sample code. I wrote this to make it similar to [Adafruit's graphicstest sketch for Arduino](https://github.com/adafruit/Adafruit-ST7735-Library/tree/master/examples/graphicstest). 

Replace initr() at line 8 to initg() or initb() if your LCD module doesn't work correctly. You can also change rgb(True) to rgb(False) to switch red and blue pixels if your LCD module shows incorrect colors.

Pin connection list:

LCD |ESP32-DevKitC
----|----
VLED|3V3
RST |IO17
A0  |IO16(DC)
SDA |IO13(MOSI)
SCK |IO14(CLK)
VCC |3V3
CS  |IO5
GND |GND

[![YouTube image here](https://img.youtube.com/vi/xIy8DPBZsIk/0.jpg)](https://www.youtube.com/watch?v=xIy8DPBZsIk)

