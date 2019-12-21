# proxy discount meal

One-two-done solution to run on your VPS to provide you with HTTP, SOCKS5 and MTProto proxies. 

Images used:
- [dannydirect/tinyproxy](https://github.com/monokal/docker-tinyproxy/)
- [dijedodol/simple-socks5-server](https://github.com/dijedodol/simple-socks5-server)
- [telegrammessenger/proxy](https://hub.docker.com/r/telegrammessenger/proxy/)

I do not own or maintain any of the images used in this file, I just set it up for myself.

## usage

- install docker and docker-compose
- clone this repo
- cd into it and run `docker-compose up -d`

## ports

- 8123 for http proxy
- 8080 for socks5
- 443 for mtproto

## how to set up

- set `HTTP_USER` and `HTTP_PASSWORD` to make your HTTP proxy super basic secure.
- set `SOCKS5_USER` and `SOCKS5_PASSWORD` to keep your socks from blowing off.
- run `docker logs tg-proxy` to uncover your MTProto secret.

## funny stuff

Tinyproxy doesn't like special characters in user/password fields.
