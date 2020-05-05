---
title: "Command line snippets"
date: 2020-04-26T05:22:26+01:00
route: "linux"
autoTitle: false
---

# Useful command line snippets

## Rename file in bash

Renames `foo-bar-baz.txt` to `foo-bar-quux.txt`
Source: https://news.ycombinator.com/item?id=22859935

```bash
mv foo-bar-{baz,quux}.txt
```

## Reduce PDF size

Source: https://askubuntu.com/questions/207447/how-to-reduce-the-size-of-a-pdf-file

```bash
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
```

## Copy directory structure without files

```bash
rsync -av -f"+ */" -f"- *" "$source" "$target"
```

## Make a slideshow with ffmpeg

Source: https://news.ycombinator.com/item?id=22028319
```bash
cat *.jpg *.JPG *.jpeg | ffmpeg -r .5 -i - -vf "scale=w=1280:h=720:force_original_aspect_ratio=2,crop=1280:720" -y slideshow.mp4
```

## Change video speed in browser
```js
setInterval(() => {document.querySelectorAll('video').forEach(v => v.playbackRate = 1.7)}, 10000)
```

## SQL Join two csv files

Source: https://www.johndcook.com/blog/2019/12/31/sql-join-csv-files/
```bash
xsv join ID person.csv ID weight.csv
```

## Conver excel to csv

Source: https://linoxide.com/linux-how-to/methods-convert-xlsx-format-files-csv-linux-cli/

```bash
ssconvert book.xlsx file.csv
```

## Show list of available wifi networks

```bash
nmcli dev wifi
```

## Create new dart package

```bash
stagehand package-simple
```

## Hranoprovod consumed food for a year

```bash
hranoprovod-cli csv -b 2019/01/01 -e 2020/01/01 | awk -F";" '{a[$2]+=$3;}END{for(i in a)print a[i]/10"\t"i;}' | grep 100g| sort -n | less
```

## Restart sound

```bash
pulseaudio -k && sudo alsa force-reload
```

## List input devices

```bash
xinput list
```

## Enable/disable input device

```bash
xinput --disable 11
xinput --enable 11
```

## Vim - create new buffer in vertical split

```vim
:vnew
```

## Sqlite - Show columns

```sql
.headers on
.mode column
```

## Number of files by extension

```bash
find . -type f | sed -n 's/..*\.//p' | sort | uniq -c
```

### Execute a command when a file is created

```bash
inotifywait -r -m /tmp/ | while read a b file; do [[ $b == *CREATE* ]] && echo $a$file && sleep 1 && img2ascii -converter=24bit2x -width=120 "$a$file"; done
```

### Manage python apps

[pipx](https://github.com/pipxproject/pipx) - like apt for pip installable apps
