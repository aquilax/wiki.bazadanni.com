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

## Player configuration file syntax

Player configuration is in plain text format in file names [PLAYER_NAME].TXT in the game root directory:

```text
LINE TYPE    DESCRIPTION
1    number  TBD (brain ?)
2    number  number of states(images) - 1
3-11 text    positional name of the item the player looses (filled with SKIN if there are no images for that state)
12-  text    flirts used by the player when they win (first half) or loose (second half)
```

## Files

```sh
$ tree -L 1
.
├── DRIVERS
├── GINA
├── GINAS
├── GRETAS
├── HOLLYS
├── JACKS
├── KAMIS
├── KATHYS
├── LAURAS
├── MORGANS
├── SAMANTHS
├── SNDS
├── BORDERS.VXL
├── CARDTABL.VGX
├── CPANEL.VGX
├── GINA.TXT
├── GINA.VXL
├── GRETA.TXT
├── GRETA.VXL
├── HOLLY.TXT
├── HOLLY.VXL
├── JACK.TXT
├── JACK.VXL
├── KAMI.TXT
├── KAMI.VXL
├── KATHY.TXT
├── KATHY.VXL
├── LAURA.TXT
├── LAURA.VXL
├── LOGO.VGX
├── MENU.VXL
├── MESSAGE.VGX
├── MORGAN.TXT
├── MORGAN.VXL
├── OPPSDD1.TXT
├── OPPSDD1.VXL
├── OPPSDD2.TXT
├── OPPSDD2.VXL
├── OPPSDD3.TXT
├── OPPSDD3.VXL
├── OPPSSP3.TXT
├── PANEL.VGX
├── README.SND
├── SAMANTHA.TXT
├── SAMANTHA.VXL
├── SCARDS.GXL
├── SETSND.BAT
├── STATUS.VXL
├── STITLE.VXL
├── STRIP.BAT
├── STRIPKRX.EXE
└── TRM15.GFT
```

### BORDERS.VXL

GX Library packed PCX images for the UI borders

```sh
W1TOP   .VGX
W1R     .VGX
W1B     .VGX
W1L     .VGX
W2TOP   .VGX
W2R     .VGX
W2B     .VGX
W2L     .VGX
W3TOP   .VGX
W3R     .VGX
W3B     .VGX
W3L     .VGX
```

### CARDTABL.VGX

PCX image with the card board.

### CPANEL.VGX

PCX image with the settings menu.

### GINA.TXT

Configuration file for GINA

### GINA.VXL

GX Library packed PCX images for GINA.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
GINA1   .VGX
GINA2   .VGX
GINA3   .VGX
GINA4   .VGX
GINA5   .VGX
GINA1   .VXW
GINA2   .VXW
GINA3   .VXW
GINA4   .VXW
GINA5   .VXW
```

### GRETA.TXT

Configuration file for GRETA

### GRETA.VXL

GX Library packed PCX images for GRETA.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
GRETA1  .VGX
GRETA1  .VXW
GRETA2  .VGX
GRETA3  .VGX
GRETA4  .VGX
GRETA5  .VGX
GRETA2  .VXW
GRETA3  .VXW
GRETA4  .VXW
GRETA5  .VXW
```

### HOLLY.TXT

Configuration file for HOLLY

### HOLLY.VXL

GX Library packed PCX images for HOLLY.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
HOLLY1  .VGX
HOLLY2  .VGX
HOLLY3  .VGX
HOLLY4  .VGX
HOLLY5  .VGX
HOLLY1  .VXW
HOLLY2  .VXW
HOLLY3  .VXW
HOLLY4  .VXW
HOLLY5  .VXW
```

### JACK.TXT

Configuration file for JACK

### JACK.VXL

GX Library packed PCX images for JACK.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
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
```

### KAMI.TXT

Configuration file for KAMI

### KAMI.VXL

GX Library packed PCX images for KAMI.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
KAMI3   .VGX
KAMI4   .VGX
KAMI5   .VGX
KAMI1   .VGX
KAMI1   .VXW
KAMI2   .VXW
KAMI3   .VXW
KAMI4   .VXW
KAMI5   .VXW
KAMI2   .VGX
```

### KATHY.TXT

Configuration file for KATHY

### KATHY.VXL

GX Library packed PCX images for KATHY.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
KATHY1  .VGX
KATHY2  .VGX
KATHY3  .VGX
KATHY4  .VGX
KATHY5  .VGX
KATHY6  .VGX
KATHY1  .VXW
KATHY2  .VXW
KATHY3  .VXW
KATHY4  .VXW
KATHY5  .VXW
KATHY6  .VXW
```

### LAURA.TXT

Configuration file for LAURA

### LAURA.VXL

GX Library packed PCX images for LAURA.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
LAURA1  .VGX
LAURA1  .VXW
LAURA2  .VXW
LAURA3  .VXW
LAURA4  .VXW
LAURA5  .VXW
LAURA3  .VGX
LAURA2  .VGX
LAURA4  .VGX
LAURA5  .VGX
```

### LOGO.VGX

Logo in PCX format used as a placeholder for missing opponents.

### MENU.VXL

GX Library packed PCX images. Disk selector backgrounds and the More button.

### MESSAGE.VGX

PCX image of the messages background.

### MORGAN.TXT

Configuration file for MORGAN

### MORGAN.VXL

GX Library packed PCX images for MORGAN.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
MORGAN1 .VGX
MORGAN2 .VGX
MORGAN3 .VGX
MORGAN4 .VGX
MORGAN5 .VGX
MORGAN1 .VXW
MORGAN2 .VXW
MORGAN3 .VXW
MORGAN4 .VXW
MORGAN5 .VXW
```

### OPPSDD1.TXT

New line separated list of opponents in Disk 1

### OPPSDD1.VXL

PCX Thumbnails of opponents in Disk 1

```sh
KATHY   .VGX
MORGAN  .VGX
```

### OPPSDD2.TXT

New line separated list of opponents in Disk 2

### OPPSDD2.VXL

PCX Thumbnails of opponents in Disk 2

```sh
JACK    .VGX
SAMANTHA.VGX
```

### OPPSDD3.TXT

New line separated list of opponents in Disk 3

### OPPSDD3.VXL

PCX Thumbnails of opponents in Disk 2

```sh
GINA    .VGX
HOLLY   .VGX
```

### OPPSSP3.TXT

New line separated list of opponents on the Master Disk

### PANEL.VGX

PCX image of the background for the current bets

### README.SND

README for re-setting the sound drivers

### SAMANTHA.TXT

Configuration file for SAMANTHA

### SAMANTHA.VXL

GX Library packed PCX images for SAMANTHA.

*.VGX - big panel image
*.VGW - small panel image

The number suffix represent the loss level

```sh
SAMANTH1.VGX
SAMANTH2.VGX
SAMANTH3.VGX
SAMANTH4.VGX
SAMANTH5.VGX
SAMANTH6.VGX
SAMANTH1.VXW
SAMANTH2.VXW
SAMANTH3.VXW
SAMANTH4.VXW
SAMANTH5.VXW
SAMANTH6.VXW
```

### SCARDS.GXL

GX Library packed PCX images for the card deck faces and backs.

```sh
D6      .C
H8      .C
SA      .C
SK      .C
SQ      .C
SJ      .C
ST      .C
S9      .C
S8      .C
S7      .C
S6      .C
S5      .C
S4      .C
S3      .C
S2      .C
HA      .C
HK      .C
HQ      .C
HJ      .C
HT      .C
H9      .C
H7      .C
H6      .C
CA      .C
CK      .C
CQ      .C
CJ      .C
CT      .C
C9      .C
C8      .C
C7      .C
C6      .C
C5      .C
C4      .C
C3      .C
C2      .C
DA      .C
DK      .C
DQ      .C
DJ      .C
DT      .C
D9      .C
D8      .C
D7      .C
D5      .C
D4      .C
D3      .C
D2      .C
H5      .C
H4      .C
H3      .C
H2      .C
CB      .C
```

### SETSND.BAT

Sound configuration

### STATUS.VXL

PCX mages for the player and the menu.

```sh
YOU1    .VGX
YOU2    .VGX
YOU3    .VGX
YOU4    .VGX
CPANEL  .VGX
MYOU1   .VGX
MYOU2   .VGX
MYOU3   .VGX
MYOU4   .VGX
```

### STITLE.VXL

Splash screen

```sh
STITLE  .VGX
```

### STRIP.BAT

Game launcher

### STRIPKRX.EXE

Main executable

### TRM15.GFT

GEM GDOS font font used in the game

