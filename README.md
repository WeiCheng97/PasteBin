# PasteBin

An simple PasteBin uses pygments to generate html and Flask as background.

Demo https://icpc.cczu.edu.cn/paste

## Run

### With Docker

```sh
sudo docker run --restart=always --name pastebin -p 127.0.0.1:80:80 -v /var/pastebin:/pastebin/data weicheng97/pastebin:2.0
```

### Directly

Do not try to just use app.run. Flask has serious problem on performance.

```sh
gunicorn -w 4 -b 0.0.0.0:80 PasteBinWeb:app
```

## Useage

Just open it and enjoy pasting.

### View all files

visit http://pastebinpath/all to find all files ordered by newest pasted time.

### Use post method to paste

Post to root URL and server receive two parameters [syntax,content], quite easy.
