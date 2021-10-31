Satconv is free software and is GPLv3+ licensed.

---Satconv asset list file format---

s4 directory: Reads all the .bmp images in the named directory and outputs a
              palette .spr file. All files must be in numerical order starting
              at 0.

sr directory: Reads all the .bmp images in the named directory and outputs an
              RGB .spr file. All files must be in numerical order starting
              at 0.

m41 map.tmx: Converts map.tmx (Tiled XML) to a .map file (4bpp graphics and SCL_PN_10BIT format)
m42 map.tmx: Converts map.tmx (Tiled XML) to a .map file (4bpp graphics and 2 word format)
m81 map.tmx: Converts map.tmx (Tiled XML) to a .map file (8bpp graphics and SCL_PN_10BIT format)
m82 map.tmx: Converts map.tmx (Tiled XML) to a .map file (8bpp graphics and 2 word format)

t0 file.bmp: Converts file.bmp to a framebuffer graphics file
t1 file.bmp: Converts file.bmp to a .tle file (8x8 tile size)
t2 file.bmp: Converts file.bmp to a .tle file (16x16 tile size)

---palette spr file format---
4 bytes: 0x0000
4 bytes: number of palettes
n bytes: palette data
4 bytes: number of sprites
--- each sprite entry ---
4 bytes: sprite x size
4 bytes: sprite y size
4 bytes: sprite palette number
n bytes: sprite tile data

---rgb spr file format---
4 bytes: 0x0001
4 bytes: number of sprites
--- each sprite entry ---
4 bytes: sprite x size
4 bytes: sprite y size
n bytes: sprite tile data

---map file format---
4 bytes: map x size
4 bytes: map y size
n bytes: map data

---tle file format---
4 bytes: palette length
n bytes: palette
4 bytes: image size
n bytes: image data 

All numbers are big-endian and unsigned.

Used libraries:

=====EzXML=====
Copyright 2004-2006 Aaron Voisine <aaron@voisine.org>
Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

=====QDBMP=====
Copyright (c) 2007 Chai Braudo (braudo@users.sourceforge.net)
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.