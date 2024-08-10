---
title: "Artworx Strip Poker Professional"
date: 2024-08-10T02:58:26+01:00
route: "artworx-strip-poker"
---

The images are stored in the *.VXL files e.g. JACK.VXL as GX Library format.
Can use [this tool](https://www.ctpax-x.org/index.php?goto=files&show=104&lang=en) to unpack them.
The archive incudes the c source which compiles on Linux too.

```shell
$ LC_ALL=C ./trid JACK.VXL
TrID/32 - File Identifier v2.24 - (C) 2003-16 By M.Pontello
Definitions found:  18084
Analyzing...

Collecting data from file: JACK.VXL
100.0% (.GXL/GX) Genus Graphics Library archive (50000/1)

$ unzip unpcxgx.zip

$ gcc unpcxgx.c -o unpcxgx

$ ./unpcxgx JACK.VXL

PCX/GX Library unpacker v1.3

GX Library format detected

JACK1   .VGX
JACK2   .VGX
JACK3   .VGX
JACK4   .VGX
JACK5   .VGX
JACK1   .VXW
JACK2   .VXW
JACK3   .VXW
JACK4   .VXW
JACK5   .VXW

done

$ file JACK1.VGX
JACK1.VGX: PCX ver. 3.0 image data bounding box [30, 10] - [442, 337], 8-bit colour, 640 x 480 dpi, RLE compressed
```
