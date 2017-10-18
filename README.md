# NGINX reverse proxy Docker image for Raspberry Pi
This is a clone of https://github.com/lroguet/rpi-nginx-proxy

The nginx template used in this version does not use the new `http2` keyword
that is supported in newer versions of Nginx.

## Description
lroguet/rpi-nginx-proxy sets up a container running NGINX and [docker-gen](https://github.com/jwilder/docker-gen). docker-gen generates reverse proxy configurations for NGINX and reloads NGINX when containers are started and stopped. lroguet/rpi-nginx-proxy is a **Raspberry Pi** compatible version of [jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy).

See [Nginx reverse proxy, Docker and a Raspberry Pi](https://fourteenislands.io/nginx-reverse-proxy-docker-and-a-raspberry-pi/) for a more detailed explanation.

## Usage
```
$ docker run -d -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock:ro lroguet/rpi-nginx-proxy
```

## Resources
* [Docker Hub](https://hub.docker.com/r/lroguet/rpi-nginx-proxy/)
* [In action](https://fourteenislands.io/nginx-reverse-proxy-docker-and-a-raspberry-pi/)
