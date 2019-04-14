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

[Curl](https://curl.haxx.se/) is widely used tool for making network requests.

Use cases:

##### Debug request:

```
$ curl -v -s http://www.example.com > /dev/null
* Rebuilt URL to: http://www.example.com/
*   Trying 93.184.216.34...
* TCP_NODELAY set
* Connected to www.example.com (93.184.216.34) port 80 (#0)
> GET / HTTP/1.1
> Host: www.example.com
> User-Agent: curl/7.58.0
> Accept: */*
>
< HTTP/1.1 200 OK
< Accept-Ranges: bytes
< Cache-Control: max-age=604800
< Content-Type: text/html; charset=UTF-8
< Date: Sat, 13 Apr 2019 03:36:14 GMT
< Etag: "1541025663+gzip"
< Expires: Sat, 20 Apr 2019 03:36:14 GMT
< Last-Modified: Fri, 09 Aug 2013 23:54:35 GMT
< Server: ECS (dcb/7EC9)
< Vary: Accept-Encoding
< X-Cache: HIT
< Content-Length: 1270
<
{ [1270 bytes data]
* Connection #0 to host www.example.com left intact
```

##### Check if URL exists

```
$ curl -I http://www.example.com
HTTP/1.1 200 OK
Content-Encoding: gzip
Accept-Ranges: bytes
Cache-Control: max-age=604800
Content-Type: text/html; charset=UTF-8
Date: Sat, 13 Apr 2019 03:36:55 GMT
Etag: "1541025663"
Expires: Sat, 20 Apr 2019 03:36:55 GMT
Last-Modified: Fri, 09 Aug 2013 23:54:35 GMT
Server: ECS (dcb/7F3B)
X-Cache: HIT
Content-Length: 606

```

#### wget

#### httrack

#### rsync

#### opendirindexer

[opendirindexer](https://github.com/aquilax/opendirindexer) is a command line tool for indexing open directories. The tool crawls the server and returns list of URLs.

Example usage:

```
$ opendirindexer http://localhost:8000
http://localhost:8000/4.txt
http://localhost:8000/test1/1.txt
http://localhost:8000/test2/3.txt
http://localhost:8000/test1/test1.1/1.txt
```

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
