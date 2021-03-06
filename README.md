# bit-plane-slice-gui
A GUI tool to export selected bitplanes of an image. Based on Python tk container.

### Background
[What is Bit plane ? (Wikipedia)](https://en.wikipedia.org/wiki/Bit_plane)
![bitplane demo](https://upload.wikimedia.org/wikipedia/commons/4/48/Lichtenstein_bitplanes.png)

### Prerequests
1. Python
2. numpy & opencv-python

### Usage
Run `bit-plane-slice-gui.py`, on the prompt window:
![gui window](https://github.com/tanido/bit-plane-slice-gui/blob/master/readme.jpg)
1. Input bitplanes(0~7) you want to keep, in format like `0,3,4`. Unselected bitplane will be purged as 0
2. Select the image file to process
3. Select the export directory, exported file name is regulated as `original filename + bitplane number .jpg`

### Example 1
Extract bitplane[0] (the MSB of bitplanes) of the image `./input/rgb.png` :
![gui window](readme.jpg)

Original image:

![rgb](https://github.com/tanido/bit-plane-slice-gui/blob/master/input/rgb.png)

|  Bitplane[0]  |  Bitplane[2] & [4] complex  |
| ------------- | --------------------------- |
| ![rgb0](https://github.com/tanido/bit-plane-slice-gui/blob/master/output/rgb_png_plane%5B'0'%5D.jpg) | ![rgb24](https://github.com/tanido/bit-plane-slice-gui/blob/master/output/rgb_png_plane%5B'2'%2C%20'4'%5D.jpg) |

### Example 2
This example is more convincing. </br>
A horizontal ramp grayscale image, features evenly increase in (R,G,B) value (while R = G = B) from left to right, visually presents as a dark to bright trasition.
Slice every bitplane of this image makes it easier to understand bitplane concept.

Original image:

![hramp](/input/grayscale_horizontal_ramp_256.png)

Bitplane [0] ~[7]:

<img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'0'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'1'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'2'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'3'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'4'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'5'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'6'%5D.jpg" width="100" height="100"> <img src="https://github.com/xukinser/bit-plane-slice-gui/blob/master/output/grayscale_horizontal_ramp_256_png_plane%5B'7'%5D.jpg" width="100" height="100">
