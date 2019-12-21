# proxy discount meal

## usage
- install docker and docker-compose
- clone this repo
- run `docker-compose up -d`

## ports
- 8123 for http proxy
- 8080 for socks5
- 443 for mtproto

## authentication

HTTP proxy authentication is provided with `HTTP_USER` and `HTTP_PASSWORD` environment variables.

socks5 proxy autheitication is provided with `SOCKS5_USER` and `SOCKS5_PASSWORD` environment variables.
