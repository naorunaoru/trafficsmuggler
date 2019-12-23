# proxy discount meal

One-two-done solution to run on your VPS to provide you with HTTP, SOCKS5 and MTProto proxies. 
Also with a IPSec PSK VPN.

Images used:
- [dannydirect/tinyproxy](https://github.com/monokal/docker-tinyproxy/)
- [dijedodol/simple-socks5-server](https://github.com/dijedodol/simple-socks5-server)
- [telegrammessenger/proxy](https://hub.docker.com/r/telegrammessenger/proxy/)
- [hwdsl2/docker-ipsec-vpn-server](https://github.com/hwdsl2/docker-ipsec-vpn-server)

I do not own or maintain any of the images used in this file, I just set it up for myself.

## usage

- install docker and docker-compose
- clone this repo
- cd into it and run `docker-compose up -d`

## ports to open

- 8123 for http proxy
- 8080 for socks5
- 443 for mtproto
- 4500/udp, 500/udp and 1701 for IPSec stuff

## how to set up

Environment variables should be set in `.env` file.

- set `HTTP_USER` and `HTTP_PASSWORD` to make your HTTP proxy super basic secure.
- set `SOCKS5_USER` and `SOCKS5_PASSWORD` to keep your socks from blowing off.
- run `docker logs tg-proxy` to uncover your MTProto secret.
- set `VPN_IPSEC_PSK`, `VPN_USER` and `VPN_PASSWORD` to do you know what.

## funny stuff

Tinyproxy doesn't like special characters in user/password fields.

I'm not responsible for your conviction or prolapsed anus, this crappy config is provided as is.

