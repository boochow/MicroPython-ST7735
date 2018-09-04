# MicroPython-ST7735

This is a modified version of [GuyCarver's ST7735.py](https://github.com/GuyCarver/MicroPython/blob/master/lib/ST7735.py) ST7735 TFT LCD driver for MicroPython.

This version is for micropython-esp32.

A font file is necessary for displaying text (some font files are in [GuyCarver's repo](https://github.com/GuyCarver/MicroPython/tree/master/lib)).

Text nowrap option added(default: nowrap=False).

graphicstest.py is a sample code. I wrote this to make it similar to [Adafruit's graphicstest sketch for Arduino](https://github.com/adafruit/Adafruit-ST7735-Library/tree/master/examples/graphicstest). 

If graphicstest.py doesn't work correctly, try replaceing initr() at line 8 to initg() or initb() or initb2(). You can also change rgb(True) to rgb(False) to switch red and blue pixels if your LCD module shows incorrect colors.

Pin connections:

LCD |ESP32-DevKitC
----|----
VLED|3V3
RST |IO17
A0  |IO16(DC)
SDA |IO13(MOSI)
SCK |IO14(CLK)
VCC |3V3
CS  |IO18
GND |GND

[![YouTube image here](https://img.youtube.com/vi/xIy8DPBZsIk/0.jpg)](https://www.youtube.com/watch?v=xIy8DPBZsIk)

tftbmp.py is another sample similar to [Adafruit's tftbmp sketch for Arduino](https://github.com/adafruit/Adafruit-ST7735-Library/blob/master/examples/spitftbitmap/spitftbitmap.ino).

Place bmp file named 'test128x160.bmp' in the file system of MicroPython using file uploading tool such as [ampy](https://github.com/adafruit/ampy), etc.
