# Image Viewer

We download the image file.

![image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/image_viewer_shoob_2.jpeg)

The details on the challenge say; 

> "My friend took this image in a cool place"

So let's take a look and see if there's any Meta data in the image;

```
[jaxigt@MBA image_viewer]$ exiftool shoob_2.jpeg 
ExifTool Version Number         : 12.00
File Name                       : shoob_2.jpeg
Directory                       : .
File Size                       : 11 kB
File Modification Date/Time     : 2020:10:31 01:06:43+00:00
File Access Date/Time           : 2020:10:31 01:06:43+00:00
File Inode Change Date/Time     : 2020:10:31 01:07:18+00:00
File Permissions                : rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
X Resolution                    : 1
Y Resolution                    : 1
Exif Byte Order                 : Big-endian (Motorola, MM)
Make                            : Shoob Phone
Camera Model Name               : Shoob 1
Resolution Unit                 : None
Software                        : MacOs ofc
Artist                          : Shoobs 4 life
Y Cb Cr Positioning             : Centered
Copyright                       : 2020
Exif Version                    : 0231
Date/Time Original              : 2020:09:04 17:09:04
Create Date                     : 2020:09:04 17:08:59
Components Configuration        : Y, Cb, Cr, -
User Comment                    : CORONA
Flashpix Version                : 0100
Owner Name                      : SHOOB
Lens Make                       : Canon 3
Lens Model                      : Shoob
Lens Serial Number              : CYCTF{h3h3h3_1m@g3_M3t@d@t@_v13w3r_ICU}
Image Width                     : 180
Image Height                    : 280
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 180x280
Megapixels                      : 0.050
```

There it is;

## CYCTF{h3h3h3_1m@g3_M3t@d@t@_v13w3r_ICU}
