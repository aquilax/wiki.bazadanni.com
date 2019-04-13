---
title: "Data Hoarder's Handbook"
date: 2019-03-18T05:22:26+01:00
route: "data-hoarder-handbook"
autoTitle: false
---

# Data Hoarder's Handbook

## Tools

### Networking

#### curl

#### wget

#### httrack

#### rsync

#### opendirindexer

#### OpenDirectoryDownloader

OpenDirectoryDownloader is the tool used to give statistics in the [opendirectories subreddit](https://www.reddit.com/r/opendirectories/). The tool was officially open sourced [here](https://www.reddit.com/r/opendirectories/comments/azdgc2/open_directory_indexer_open_sourcedreleased/) and can be found on GitHub. Supports indexing of HTTP/FTP and GDrive resources.

* Repository: https://github.com/KoalaBear84/OpenDirectoryDownloader
* Language: C#, .NET Core
* License: GPL3

#### lftp

#### ipfs

### Text processing

#### urlcat

`urlcat` is a command line utility, allowing you to extract parts of URLs.

* Repository: https://github.com/aquilax/urlcat
* Language: Go
* License: MIT

#### grep

#### wc

#### uniq

#### sort

#### sed

### Other

##### img2ascii

`img2ascii` is tool that allows you to render images in the terminal.
Can be combined with inotify to stream image downloads in a terminal screen like that:

```
inotifywait -r -m /download_dir | while read a b file; do [[ $b == *CREATE* ]] && echo $a$file && sleep 1 && img2ascii -converter=24bit2x -width=80 "$a$file"; done
```

* Repository: https://github.com/aquilax/img2ascii
* Language: Go
* License: MIT

### Online tools

#### Fusker

From [Wikipedia](https://en.wikipedia.org/wiki/Fusker):

> Fusker is a type of website or utility that extracts images from a web page, typically from free hosted galleries.

## Communities

* [The Eye](https://the-eye.eu/)
* [DataHoarder subreddit](https://www.reddit.com/r/DataHoarder/)
* [Opendirectories subreddit](https://www.reddit.com/r/opendirectories/)

## Hardware

### HDD

### NAS

### Tape
