# proxy discount meal

## usage
- install docker and docker-compose
- clone this repo
- run `docker-compose up -d`

## ports
- 8080 for http proxy
- 8123 for socks5
- 443 for mtproto

socks5 credentials are provided with `SSS_USERNAME` and `SSS_PASSWORD` environment variables, you can create a .env file with them.
